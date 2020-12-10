#include <bits/stdc++.h>

using namespace std;

int main(){
    ios::sync_with_stdio(0);
    cin.tie(0);
    string test; cin >> test;
    size_t found = test.find('*');
    string rvr ="";
    for(int n=test.size()-1;n>=0;--n){
        rvr.push_back(test[n]);
    }
    size_t foundr = rvr.find('*');
    int t; cin >> t;
    while(t--){
        string text; cin >> text;
        string txtr = "";
        for(int n=text.size()-1;n>=0;--n){
            txtr.push_back(text[n]);
        }
        bool condition = false;
        bool cont1 = text.substr(0, found) == test.substr(0, found);
        bool cont2 = txtr.substr(0, foundr) == rvr.substr(0, foundr);
        if(cont1 && cont2)
            condition = true;
        if(condition)
            cout << text << "\n";
    }
}
