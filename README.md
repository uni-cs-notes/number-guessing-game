# number-guessing-game
```
#include <iostream>
#include <string>
#include <cstdlib>
#include <ctime>
using namespace std;

void numG();
void exitG();
int main(){
    
    cout<<"\tnumber guessing game between 1 to 10 "<<endl;

    int options;
    cout<<"\t\t\tpress '1' to play !!!"<<endl;
    cout<<"\t\t\tpress '2' for exit !!"<<endl;
    cin >>options;
    switch (options){
        case 1: numG();
        break;
        case 2: exitG();
        break;
        default: cout<<"invaild key plzz enter the right key!!!!";
        break;
    }  
}
 
void numG()
{
    
    int number = 1 + rand() % 10;                // its generating the same number again & again (issue)
    int guess;
    int guesschance=0;

    while (number!= guess){

    
         cout<<"Player  Enter a number: "<<endl;
         cin>>guess;

        if (guess < number)
        {
            cout<<" The number is too low."<<endl;
        }
        else if (guess > number)
        {
            cout<<" The number is too high."<<endl;
        }
        else
        {
            cout<<" You are correct! Congratulations!"<<endl;
        }

        guesschance++;
    }

    cout<<" you made "<<guesschance<<" Attemps!"<<endl;
}
    
void exitG(){
    cout<< "you have exited the game";
}


```
