#include<iostream>
using namespace std;

int main(){
int arr[20],i,j,size,temp,min,loc;

cout<<"Enter the size of array"<<"\n";
cin>>size;

cout<<"Enter the array elements"<<"\n";
for(i=0;i<size;i++){
cin>>arr[i];
}

for(i=0;i<(size-1);i++){
min=arr[i];
loc=i;
for(j=i+1;j<size;j++){
if(arr[j]<min){
 min=arr[j];
 loc=j;
}
}


 temp=arr[i];
arr[i]=arr[loc];
arr[loc]=temp;
}


cout<<"sorted array"<<"\n";
for(int i=0;i<size;i++){
cout<<arr[i]<<" ";
}
cout<<"Top five are"<<"\n";
for(int i=size-1;i>size-5;i--){
 cout<<arr[i]<<"\n";
}
}
