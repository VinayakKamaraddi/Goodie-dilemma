# Goodie-dilemma
Goodie-dilemma program
#include <bits/stdc++.h>
using namespace std;

int main() {
	int o;
	std::vector<int> v;
	cout<<"Goodies and Prices"<<endl;
	cout<<"Fitbit Plus: ";
	cin>>o;
	v.push_back(o);
	cout<<"IPods: ";
	cin>>o;
	v.push_back(o);
	cout<<"MI Band: ";
	cin>>o;
	v.push_back(o);
	cout<<"Cult Pass: ";
	cin>>o;
	v.push_back(o);
	cout<<"Macbook Pro: ";
	cin>>o;
	v.push_back(o);
	cout<<"Digital Camera: ";
	cin>>o;
	v.push_back(o);
	cout<<"Alexa: ";
	cin>>o;
	v.push_back(o);
	cout<<"Sandwich Toaster: ";
	cin>>o;
	v.push_back(o);
	cout<<"Microwave Oven: ";
	cin>>o;
	v.push_back(o);
	cout<<"Scale: ";
	cin>>o;
	v.push_back(o);

	cout<<endl;

	int n = v.size();
	int num_of_testcases;
	cout<<"Enter no.of test cases:";
	cin>>num_of_testcases;
	for(int l=0; l<num_of_testcases; l++){   
	int m;
	cout<<"Number of the employees:";
    cin>>m;
    cout<<endl;

    int arr[n];
    for (int i = 0; i < n; i++) {
        arr[i] = v[i];
    }

	sort(arr, arr+n);//sorting the array
	
	int mi = INT_MAX;
	int sindex;//to keep track of start index
	int eindex;//and end index
	
	for(int i=0; i<n-m+1; i++){
	    if(mi>(arr[i+m-1]-arr[i])){
	        sindex = i;
	        eindex = i+m-1;
	        mi = arr[i+m-1]-arr[i];
	    }
	}

cout<<"Here the goodies that are selected for distribution are:"<<endl;
	
	for(int i=sindex; i<=eindex; i++){
    
    if(arr[i] == 7980)
        cout<<"Fitbit Plus: "<<arr[i]<<endl;
    else if(arr[i] == 22349)
        cout<<"IPods: "<<arr[i]<<endl;
    else if(arr[i] == 999)
        cout<<"MI Band: "<<arr[i]<<endl;
    else if(arr[i] == 2799)
        cout<<"Cult Pass: "<<arr[i]<<endl;
    else if(arr[i] == 229900)
        cout<<"Macbook Pro: "<<arr[i]<<endl;
    else if(arr[i] == 11101)
        cout<<"Digital Camera: "<<arr[i]<<endl;
    else if(arr[i] == 9999)
        cout<<"Alexa: "<<arr[i]<<endl;
    else if(arr[i] == 2195)
        cout<<"Sandwich Toaster: "<<arr[i]<<endl;
    else if(arr[i] == 9800)
        cout<<"Microwave Oven: "<<arr[i]<<endl;
    else if(arr[i] == 4999)
        cout<<"Scale: "<<arr[i]<<endl;
}

cout<<endl<<"And the difference between the chosen goodie with highest price and the lowest price is "<<mi<<endl;

}
return 0;
}
