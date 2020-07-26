#include<iostream>
using namespace std;

class grade
{
	public:
        int mark[5],i;
        float sum=0,avg;
    public:
	void getmarks()
	{
	    cout<<"****Enter Marks in 5 subjects****\n";
        for(i=0; i<5; i++)
        {
            cout<<"\nEnter Marks[ "<<i+1<<" ] :: ";
            cin>>mark[i];
            sum=sum+mark[i];
        }
    }
    void getgradesandpercentage()
    {
        avg=sum/5;
        cout<<"\nPercentage: "<<avg<<" %" <<endl;
        
        if(avg>85)
        {
            cout<<"Your grade is => A\n";
        }
        else if(avg<85 && avg>=75)
        {
            cout<<"Your grade is => B\n";
        }
        else if(avg<75 && avg>=50)
        {
            cout<<"Your grade is => C\n";
        }
        else if(avg<50 && avg>=30)
        {
            cout<<"Your grade is => D\n";
        }
        else 
        {
            cout<<"Fail";
        }
   }
};
int main()
{
	grade obj1;
    obj1.getmarks();
    obj1.getgradesandpercentage();
}
