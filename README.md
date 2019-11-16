#include<iostream>
using namespace std;
void isPair(int arr[],int n,int sum)
{
    int H[sum+1] = {0};
    for(int i=0;i<n;i++)
    {
        if(H[sum-arr[i]]!=0)
        {
            printf("%d + %d = %d\n",arr[i],sum-arr[i],sum);
        }
        H[arr[i]]++;
    }
}
int main()
{
    int sum=10;
    int arr[]={1,2,8,3,7};
    isPair(arr,sizeof(arr)/sizeof(arr[0]),sum);
    return 0;
}
