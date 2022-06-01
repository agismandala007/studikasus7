#include <iostream> 
#include <string>
#include <conio.h>
using namespace std;

class Data {
    public:
        void input();
        void urut();
        void mencari();
        void output();


    private:
        int nim[6], no_telp[50], banyak, ketemu=0, cari, pilih, tmp;
        string nama[50], prodi[20];
};

void Data::input(){
    cout<<"Masukan banyaknya mahasiswa : ";cin>>banyak;

    for (int i=1;i<=banyak;i++){
        cout << "Masukkan data mahasiswa ke-"<<i<<endl;
        cout<<"NIM       : ";cin>>nim[i];cin.ignore();
        cout<<"Nama      : ";getline(cin, nama[i]);
        cout<<"Prodi     : ";getline(cin, prodi[i]);
        cout<<"No.Telp   : ";cin>>no_telp[i];
        cout<<endl;
    }
}

void Data::urut(){
    int n1m[50];

    for(int i=1; i<=banyak; i++){
        n1m[i]=nim[i];
    }

    cout<<"1. Ascending"<<endl;
    cout<<"2. Descending"<<endl;
    cout<<"Pilih cara mengurutkan Data : ";cin>>pilih;
  
    if(pilih==1){
        cout<<"Mengurutkan data secara Ascending : "<<endl;
        for(int x=1; x<banyak; x++){
            for(int y=x+1; y<=banyak; y++){
                if(n1m[x]>n1m[y]){
                    tmp=n1m[x];
                    n1m[x]=n1m[y];
                    n1m[y]=tmp;
                }
            }
        }
        for(int i=1; i<=banyak; i++){
            cout<<i<<". "<<n1m[i]<<endl;
        }
    }
  
    else if (pilih==2){
        cout<<"Mengurutkan data secara Descending : "<<endl;
        for(int i=1; i<banyak; i++){
            for(int z=i+1; z<=banyak; z++){
                if(n1m[i]<n1m[z]){
                    tmp=n1m[i];
                    n1m[i]=n1m[z];
                    n1m[z]=tmp;
                }     
            }
        }
        for(int i=1; i<=banyak; i++){
            cout<<i<<". "<<n1m[i]<<endl;
        }
    }
}

void Data::mencari(){
    cout<<"Masukan NIM yang ingin dicari : ";cin>>cari;

    for(int i=1; i<=banyak; i++){
        if(cari==nim[i]){
            cout<<"Nim      : "<<nim[i]<<endl;
            cout<<"Nama     : "<<nama[i]<<endl;
            cout<<"Prodi    : "<<prodi[i]<<endl;
            cout<<"No.Telp  : "<<no_telp[i]<<endl;
        }
    }
    
}
int main() {
    int a;
    Data x;

    x.input();
    do{
        cout<<"1. Mencari Mahasiswa    : "<<endl;
        cout<<"2. Mengurutkan Mahasiswa : "<<endl;
        cout<<"3. Exit"<<endl;
        cout<<"Pilih : ";cin>>a;

        if(a==1){
            x.mencari();
            getch();
            cout<<endl;
        }
        else if(a==2){
            x.urut();
            getch();
            cout<<endl;
        }
        cout<<endl;
    }while(a!=3);
}
