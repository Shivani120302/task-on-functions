#include<iostream>
using namespace std;
int prime(int );
int main()
{
  int num ,i, check=0;
  cout<<"enter a positive number.... ";
  cin>>num;
  for(i=1;i<=num/2;i++)
  {
    if(prime(i))
    {
      if(prime(num-i))
      cout <<num<<"="<<i<<"+"<<num-i<<endl;
   check=1;
    }
  }
  if(check==0)
      cout<<num<<" can't be written as sum of two prime numbers...! :("<<endl;  
}
int prime(int n)
{
  int i, div=0;
  for(i=1;i<=n;i++)
  {
    if(n%i==0)
    div++;
  }
  if(div==2)
  return 1;
  else
  return 0;
};
