CEZAR:

#include <iostream>
#include <cstring>
#include <string>
using namespace std;

int main(int argc, char*argv[]) {
  setlocale(LC_ALL, "Rus");
  string name = " ";
  cout << "введите на сколько переносить : ";
  int f;
  cin >> f;
  for (int i = 1; i < argc; i++) {
    name += argv[i];
    name += " ";
  }
  for (int i = 0; i < name.size(); i++) {
    if(name[i] == ' '){
      continue;
    }
    if((name[i] >= 97) and (name[i] <= 122)){
      for (int j = 0; j < f; j++) {
          if(int(name[i]) == 122){
            name[i] = 96;
          }
          name[i] = name[i] + 1;
      }
    }
    else if((name[i] >= 65) and (name[i] <= 90)){
      for (int j = 0; j < f; j++) {
          if(int(name[i]) == 90){
            name[i] = 64;
          }
          name[i] = name[i] + 1;
      }
    }
  }
  cout << '\n' + name + '\n';
  return 0;
}

ANTI_CEZAR:
#include <iostream>
#include <cstring>
#include <string>
using namespace std;

int main(int argc, char*argv[]) {
  setlocale(LC_ALL, "Rus");
  string name = " ";
  cout << "введите на сколько переносить : ";
  int f;
  cin >> f;
  for (int i = 1; i < argc; i++) {
    name += argv[i];
    name += " ";
  }
  for (int i = 0; i < name.size(); i++) {
    if(name[i] == ' '){
      continue;
    }
    if((name[i] >= 97) and (name[i] <= 122)){
      for (int j = 0; j < f; j++) {
          if(int(name[i]) == 97){
            name[i] = 123;
          }
          name[i] = name[i] - 1;
      }
    }
    else if((name[i] >= 65) and (name[i] <= 90)){
      for (int j = 0; j < f; j++) {
          if(int(name[i]) == 65){
            name[i] = 91;
          }
          name[i] = name[i] - 1;
      }
    }
  }
  cout << '\n' + name + '\n';
  return 0;
}
