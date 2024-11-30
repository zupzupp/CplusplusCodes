#include <bits/stdc++.h>
using namespace std;

typedef long long ll;
typedef vector <long long> v;
int main(){

  ll height, input;

  cin>>input;

  v input_men;
  v input_women;
  v output_men;
  v output_women;

  for (ll i=0; i<input; i++){
    cin>>height;
    input_men.push_back(height);
  }

  for (ll i=0; i<input; i++){
    cin>>height;
    input_women.push_back(height);
  }

  sort (input_women.begin(), input_women.end());
  sort (input_men.begin(), input_men.end());

  v men_height_picked (input,0);
  v women_height_picked (input,0);

  for (ll m=input-1; m>-1; m--){
    for (ll w=input-1; w>-1; w--){
      if (men_height_picked[m]==0 && women_height_picked[w]==0){
        if (input_men[m]>=input_women[w]){
          output_men.push_back(input_men[m]);
          output_women.push_back(input_women[w]);
          men_height_picked[m]=1;
          women_height_picked[w]=1;
        }
      }
    }
  }

  for (ll o=0; o<output_women.size(); o++){
    cout<<output_men[o]<<" "<<output_women[o]<<endl;
  }
  
  return 0;
}
