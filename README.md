# contekan
	#include <iostream>
	#include <stdlib.h>
	using namespace std;

	void informatika();
	void ilmu_komputer();
	void sistem_informasi();


	int main(){

		informatika();
	}

	void informatika(){
		int jml_mhs;
		cout << "Masukan jumlah mahasiswa yang akan diinput nilainya :";
		cin >> jml_mhs;
		string matkul[4] = {"Dasar Pemrograman","Struktur Data","Algoritma Pemrograman","Rekayasa Perangkat Lunak"};
		string mahasiswa[jml_mhs][2];
		int nilai[jml_mhs][5];


		cout << endl;
		for(int i = 0; i<jml_mhs; i++){
			cout << "Masukan data mahasiswa ke - " << i+1 << endl;
			cout << "NIM: ";
			cin >> mahasiswa[i][0];
			cout << "Nama :";
			cin >> mahasiswa[i][1];
			cout << endl;

			cout << "Masukan nilai skala 0-100" << endl;
			for(int j = 0; j<4; j++){
				cout << matkul[j] << ": ";
				cin >> nilai[i][j];
				}
			cout << endl;
			}

		for(int i = 0; i<jml_mhs; i++){
			int hasil = 0;
			for(int j = 0; j<4; j++){
				hasil += nilai[i][j];
				nilai[i][4] = hasil;
			}
		}

		cout << endl;
		for(int i = 0; i<jml_mhs; i++){
			cout << "Data Mahasiswa ke- " << i+1 << ":" << endl;
			cout << "NIM :" << mahasiswa[i][0] << endl;
			cout << "Nama :" << mahasiswa[i][1] << endl;

			for(int j = 0; j<4; j++){
				cout << matkul[j] << " : " << nilai[i][j] << endl;
			}
			cout << "Rata Rata Nilai : " <<  nilai[i][4] / 4 << endl;

			cout << endl;
		}


	}
