#labpy08
praktikum 8

soal:
Buat program sederhana dengan mengaplikasikan penggunaan class. buatlah class untuk menampilkan daftar nilai mahasiswa, dengan ketentuan: 
1. Method tambah() untuk menambah data
2. Method tampilkan() untuk menampilkan data
3. Method hapus(nama) untuk menghapus data berdasarkan nama
4. Metode ubah(nama) untuk mengubah data berdasarkan nama

 KODE PYTHON
 

            class DaftarNilaiMahasiswa:
            def _init_(self):  
            self.mahasiswa = {}

            def tambah(self, nama, nilai):
            """Menambah data mahasiswa."""
            self.mahasiswa[nama] = nilai
            print(f"Data {nama} dengan nilai {nilai} berhasil ditambahkan.")

            def tampilkan(self):
            """Menampilkan semua data mahasiswa."""
            if not self.mahasiswa:
            print("Tidak ada data mahasiswa.")
            else:
            print("Daftar Nilai Mahasiswa:")
            for nama, nilai in self.mahasiswa.items():
            print(f"Nama: {nama}, Nilai: {nilai}")

        def hapus(self, nama):
        """Menghapus data mahasiswa berdasarkan nama."""
        if nama in self.mahasiswa:
        del self.mahasiswa[nama]
        print(f"Data {nama} berhasil dihapus.")
        else:
        print(f"Data {nama} tidak ditemukan.")

        def ubah(self, nama, nilai_baru): 
        """Mengubah data mahasiswa berdasarkan nama."""
        if nama in self.mahasiswa:
        self.mahasiswa[nama] = nilai_baru
        print(f"Data {nama} berhasil diubah menjadi nilai {nilai_baru}.")
        else:
        print(f"Data {nama} tidak ditemukan.")

        def main():
        daftar = DaftarNilaiMahasiswa()

        while True:
        print("\nMenu:")
        print("1. Tambah Data")
        print("2. Tampilkan Data")
        print("3. Hapus Data")
        print("4. Ubah Data")
        print("5. Keluar")

    pilihan = input("Pilih menu: ")

    if pilihan == '1':
        nama = input("Masukkan nama mahasiswa: ")
        try:
            nilai = int(input("Masukkan nilai mahasiswa: "))
            daftar.tambah(nama, nilai)
        except ValueError:
            print("Nilai harus berupa angka.")
    elif pilihan == '2':
        daftar.tampilkan()
    elif pilihan == '3':
        nama = input("Masukkan nama mahasiswa yang ingin dihapus: ")
        daftar.hapus(nama)
    elif pilihan == '4':
        nama = input("Masukkan nama mahasiswa yang ingin diubah: ")
        try:
            nilai_baru = int(input("Masukkan nilai baru: "))
            daftar.ubah(nama, nilai_baru)
        except ValueError:
            print("Nilai harus berupa angka.")
    elif pilihan == '5':
        print("Keluar dari program.")
        break
    else:
        print("Pilihan tidak valid. Silakan coba lagi.")

    if _name_ == "_main_":
    main()


PENJELASAN KODE PYTHON:

1. Tambah Data: Menyimpan nama dan nilai mahasiswa ke dalam dictionary.
  
2. Tampilkan Data: Menampilkan semua data mahasiswa dalam format daftar.
 
3. Hapus Data: Menghapus data mahasiswa berdasarkan nama berdasarkan nama.
 
4. Ubah Data: Mengupdate nilai mahasiswa berdasarkan nama.
 
Program menyediakan menu interaktif berbasis teks untuk pengguna, berjalan dalam loop hingga memilih opsi Keluar.


PENJELASAN DIAGRAM CLASS:

Atribut: mahasiswa: Dictionary untuk menyimpan data mahasiswa (nama sebagai key, nilai sebagai value). Metode:

1.init(): Menginisialisasi atribut mahasiswa sebagai dictionary kosong.

2tambah(nama, nilai): Menambahkan data mahasiswa.

3.tampilkan(): Menampilkan semua data mahasiswa.

4.hapus(nama): Menghapus data berdasarkan nama.

5.ubah(nama, nilai_baru): Memperbarui nilai mahasiswa.


