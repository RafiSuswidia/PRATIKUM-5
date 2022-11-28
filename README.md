# PRATIKUM-5

Tugas : Praktikum 5

Membuat dictionary data

Membuat menu pilihan (A)dd (E)dit (D)elete (S)earch (L)ist (Q)uit

A. Untuk pilihan A meninput Nama, Nim, Tugas, Uts dan Uas. jika nilai nama, nim, tugas, uts, dan uas kosong maka program ValueError dan meminta untuk input ulang. dan untuk data yg sudah di tambahkan menggunakan key nama.

Kode Program :

    elif c.lower() == 'a':
        print ("\nMasukan Data Mahasiswa")

        while (True):
            nama = input("NAMA : ")
            if nama == '':
                print ('Nama tidak boleh kosong')
            else:
                break
        while (True):
            try:
                nim  = int(input("NIM  : "))
                if nim == '':
                    print ('Masukan Nim dengan Angka')
            except ValueError:
                print ('Masukan Nim dengan Angka')
            else:
                break
        while (True):
            try:
                tugas  = int(input("TUGAS  : "))
                if tugas == '':
                    print ('Masukan TUGAS dengan Angka')
            except ValueError:
                print ('Masukan TUGAS dengan Angka')
            else:
                break
        while (True):
            try:
                uts  = int(input("UTS  : "))
                if uts == '':
                    print ('Masukan UTS dengan Angka')
            except ValueError:
                print ('Masukan UTS dengan Angka')
            else:
                break
        while (True):
            try:
                uas  = int(input("UAS  : "))
                if uas == '':
                    p('Masukan UAS dengan Angka')
            except ValueError:
                print ('Masukan UAS dengan Angka')
            else:
                break
        akhir = round((float(tugas) * 0.3)+(float(uts) * 0.35)+(float(uas) * 0.35),2)
        data[nama] = [nama,nim,tugas,uts,uas,akhir]
Hasli program :

![Screenshot (49)](https://user-images.githubusercontent.com/115480539/204200578-1df28556-bd18-44a8-a46d-932882e238a1.png)


B. untuk pilihan E berfungsi untuk edit data yg sudah ada denagan nama sebagai key pencarian data, jika tidak sesuai maka data tidak di temukan. Lalu input pembaruan data dengan sesuai, jika ada yg kosong maka program ErorValue dan program meminta input ulang, dan jika sudah data sudah di perbarui

Kode Program :

 elif c.lower() == 'e':
        nama = input("Masukan nama untuk edit data : ")

        if nama in data.keys():
            del data[nama]
            print ("\nMasukan Pembaruan Data")

            while (True):
                nama = input("NAMA : ")
                if nama == '':
                    print ('Nama tidak boleh kosong')
                else:
                    break
            while (True):
                try:
                    nim = int(input("NIM  : "))
                    if nim == '':
                        print ('Masukan Nim dengan Angka')
                except ValueError:
                    print ('Masukan Nim dengan Angka')
                else:
                    break
            while (True):
                try:
                    tugas = int(input("TUGAS  : "))
                    if tugas == '':
                        print ('Masukan TUGAS dengan Angka')
                except ValueError:
                    print ('Masukan TUGAS dengan Angka')
                else:
                    break
            while (True):
                try:
                    uts = int(input("UTS  : "))
                    if uts == '':
                        print ('Masukan UTS dengan Angka')
                except ValueError:
                    print ('Masukan UTS dengan Angka')
                else:
                    break
            while (True):
                try:
                    uas = int(input("UAS  : "))
                    if uas == '':
                        print ('Masukan UAS dengan Angka')
                except ValueError:
                    print ('Masukan UAS dengan Angka')
                else:
                    break
            akhir = round((float(tugas) * 0.3) + (float(uts) * 0.35) + (float(uas) * 0.35), 2)
            data[nama] = [nama, nim, tugas, uts, uas, akhir]

        else:
            print (" ________________________")
            print ("| Data {} tidak ditemukan |".format(nama))
            print (" ‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾")
        print ("\n    (A)dd       (E)dit      (D)elete     (S)earch      (L)ist     (Q)uit   ")
Hasil Program :

Data tersedia


![Screenshot (51)](https://user-images.githubusercontent.com/115480539/204200670-c7ee8398-ff23-4227-b7d8-8f863e48ca67.png)
