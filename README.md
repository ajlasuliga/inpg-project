#include <iostream>
#include <stdio.h>
#include <stdlib.h>
#include <fstream>
#include <string>
 
using namespace std;
 
int a,b,c,d;
int wynik;
char tn;
 
float zestaw(int suma);
 
int main()
{
    for(;;)
    {
        cout<<"Witaj w kreatorze cen zestawow firmy LEGO!"<<endl<<endl;
        cout<<"----------------->>MENU<<-----------------"<<endl;
        cout<<"1. Stworz wlasny zestaw."<<endl;
        cout<<"2. Wczytaj zapisany projekt."<<endl;
        cout<<"3. Ponoc."<<endl;
        cout<<"4. Wyjscie."<<endl;
        cout<<"=========================================="<<endl;
        cout<<"Wybierz opcję: ";
        cin>>a;
 
        switch(a)
        {
        case 1:
        {
            string napis;
            cout<<"Podaj nazwe zestawu: ";
            cin.ignore();
            getline (cin,napis);
            cout<<"Ilu bohaterow pierwszoplanowych na byc w zestawie?: ";
            cin>>b;
            cout<<"Ilu bohaterow drugoplanowych ma byc w zestawie?: ";
            cin>>c;
            cout<<"Ile bedzie specjalnych klockow w zestawie?: ";
            cin>>d;
            cout<<"Wynik = "<<zestaw(wynik)<<endl;
            cout<<"Czy zapisac wynik? [t/n]: ";
            cin>>tn;
            if (tn=='t')
            {
                fstream plik;
                plik.open("Zestawy.txt",ios::out | ios::app);
                plik<<"Zestaw: "<<napis<<":"<<endl;
                plik<<"Dodano "<<b<<" pierwszoplanowych postaci."<<endl;
                plik<<"Dodano "<<c<<" drugoplanowych postaci."<<endl;
                plik<<"Dodano "<<d<<" specjalnych klockow."<<endl;
                plik<<"Tyle bedzie kosztowal caly zestaw."<<zestaw(wynik)<<" PLN"<<endl;
                plik.close();
                cout<<"Zapis wykonany pomyślnie!\n Wcisnij ENTER";
            }
            else
                system ("clear");
 
        }
        break;
        case 2:
            cout<<"b";
            break;
        case 3:
            cout<<"c";
            break;
        case 4:
        {
            cout<<"Do zobaczenia!";
            exit(0);
        }
        break;
        }
