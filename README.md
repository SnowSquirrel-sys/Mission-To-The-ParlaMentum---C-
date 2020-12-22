# Mission-To-The-ParlaMentum-C++


//this mission created for show what am i know about:     C++    in the other i will show you what am i know about Java.

#include <iostream>
using namespace std;
int main()
{//now we want to create the first 6 numbers
    int vec1[6]{ 0 }, vec2[6]{ 0 },  tmp = 0;
    //
    cout << "enter first 6 numbers:"<<endl;
    for (int i = 0, tmp = 0; i < 6; i++)
    {
        cin >> tmp;
        while (tmp <= 0)
        {//we just check if this is not 0 or lower
            cout << "ERROR" << endl;
            cin >> tmp;
        }
        vec1[i] = tmp;
    }
    //
    cout << "enter next 6 numbers:" << endl; //now we want to create the last 6 numbers
    for (int i = 0,tmp = 0; i < 6; i++)
    {
        cin >> tmp;
        while (tmp <= 0)
        {//we check here agian if this is not 0 or lower
            cout << "ERROR" << endl;
            cin >> tmp;
        }
            vec2[i] = tmp;
    }
    for (int i = 0; i < 6; i++) //now we want to check if there is any diffrent
    {
        for (int j = 0; j < 6; j++)
        {
            if(vec1[i]==vec2[j])
            {
                vec1[i] = 0;
            }
        }
    }
    cout << "set difference is:" << endl;
    tmp = 0;
    for (int i = 0; i < 6; i++) //and the other one
    {
        if (vec1[i] != 0)
            cout << vec1[i] << ' ';
        else
        {
            tmp++;
        }
    }
    if (tmp == 6)
    {//if there is not diffrent let's print "empty"
        cout << "empty" << endl;
    }
