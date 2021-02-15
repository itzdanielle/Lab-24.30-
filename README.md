# Lab-24.30-
#include <iostream>
using namespace std;
double findHighTemp (int temp[], int& numberOfTemp) {
  int max;
  max = temp[0];
  for (int i = 0; i < numberOfTemp; i++) {
    if (temp[i] > max)
    max = temp[i];
  }
  cout << "The highest temperature is " << max << endl;
  return max;
}
double findLowTemp (int temp[], int& numberOfTemp) {
  int min;
min = temp[0];
for (int i = 0; i < numberOfTemp; i++) {
    if (temp [i] < min)
    min = temp[i];
  }
  cout << "The lowest temperature is " << min << endl;
  return min;
}
double findAverage (int temp [], int& numberOfTemp) {
  int sum = 0, i;
  for (int i = 0; i < numberOfTemp; i++) {
    cout << "Temperature " << i+ 1 << " is " << temp[i] << endl;
    sum = sum + temp [i];
  }
  double average = sum/numberOfTemp;
  cout << "The average temperature is " << average << endl;
  return average;
}
int main() {
const int MAX_TEMP = 50;
int temp [MAX_TEMP];
int numberOfTemp;
int pos, min, max;
pos = 0;
cout << "Please input a temperautre from 1 to 100, (or -999 to stop)" << endl;
cin >> temp[pos];
while (temp[pos] != -999){
  pos ++;
  cin >> temp[pos];
}
numberOfTemp = pos;
findHighTemp(temp,numberOfTemp);
findLowTemp(temp,numberOfTemp);
findAverage(temp,numberOfTemp);
}
