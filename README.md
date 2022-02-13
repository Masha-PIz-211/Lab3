/* ******************** *
* Власова Мария
* Программирование циклов с ветвлением
* Вариант 2
* *********************** /

#include <iostream>
#include <cmath>

using namespace std;
 
int main() 
{
  setlocale(0, "");
  float c[6]={8,7.5,7,6,4,2};
  float d=0.000063, h=2.5, c0=8.2, cp=1.7, t, i;
  cout << "Интенсивность нестационарного массообмена хим. вещества \n";
  for (int j=0; j<6; j++) 
  {
  	t=sqrt(2)/M_PI*(c0-cp)/(c0-c[j]); 
  	if (t>2)
  	  i=sqrt(2)*d*t/(h*h)*(c0-cp);
  	else
  	  i=0.25*d*M_PI*M_PI/(h*h)*(c0-cp);
  	printf(" t = %9.6f   i = %.6f \n",t,i); 
  }
  system("pause"); 
  return 0;
}
