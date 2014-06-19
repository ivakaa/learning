#include "stdafx.h"
using namespace std;
#include <iostream>
#include <stdlib.h>
#include <conio.h>
//Декларация на клас Student
class Student{
private:
char Ime[21];
char FakNom[7];
short Kurs;
short Ocenki[10];//-оценките по 10 дисциплини
public:
void getData();//-декларация на член-функцията getData
// Дефиниция на вградената член-функция display
void Student::display(){
cout<<"Име: "<<Ime<<endl;
cout<<"Факултетен номер: "<<FakNom<<endl;
cout<<"Курс: "<<Kurs<<endl;
cout<<"Оценки: ";
for (int i=0; i<10; i++) cout<<Ocenki[i]<<' ';
cout<<endl;
}
};
// Дефиниция на член-функция getData
void Student::getData(){
cout<<"Въведете име: "; cin.getline(Ime,20);
cout<<"Въведете фак. номер: "; cin>>FakNom;
cout<<"Въведете курс: "; cin>>Kurs;

cout<<"Въведете 10 оценки\n";
for (int i=0; i<10; i++){
cout<<i<<"-а оценка: "; cin>>Ocenki[i];
}
}
// Главна функция
void main(){
system("chcp 1251");
Student A,B;
cout<<"\nВъвеждане на член-данните на обекта A\n"; A.getData();
cout<<"\nИзвеждане на член-данните нa обекта A:\n"; A.display();
B=A; //Присвояване стойността на А на обекта В
cout<<"\nИзвеждане на член-данните на обекта В:\n"; B.display();
cout<<endl;
getch();
}
