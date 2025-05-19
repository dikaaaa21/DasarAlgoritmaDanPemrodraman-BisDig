STUDI KASUS PERTAMA

# Penjelasan Fungsi dan Rekursi dalam Menghitung Faktorial

## Studi Kasus
Program ini menghitung faktorial dari sebuah bilangan yang dimasukkan pengguna dengan menggunakan metode rekursif.

## Manfaat Penggunaan Fungsi

**Modularitas**  
  Fungsi `faktorial` mengemas logika perhitungan faktorial dalam satu bagian kode yang terpisah. Ini membuat program lebih terstruktur dan mudah dipahami.

**Penggunaan Ulang**  
  Fungsi dapat dipanggil berkali-kali dengan input berbeda tanpa menulis ulang kode.

**Pemeliharaan Mudah**  
  Jika ada perubahan cara menghitung faktorial, cukup ubah di fungsi ini tanpa perlu mengubah bagian lain program.

**Meningkatkan Keterbacaan**  
  Kode menjadi lebih ringkas dan jelas karena fungsi memiliki tugas spesifik.

## Cara Kerja Rekursi dalam Fungsi Faktorial

Rekursi adalah teknik pemrograman di mana sebuah fungsi memanggil dirinya sendiri untuk menyelesaikan masalah yang lebih kecil hingga mencapai kondisi dasar (base case).

### Penjelasan Kode:

def faktorial(n):
if n == 0 or n == 1: # Base case
return 1
else:
return n * faktorial(n - 1) # Recursive case

**Base Case**  
  Saat `n` adalah 0 atau 1, fungsi mengembalikan nilai 1. Ini mencegah rekursi berjalan terus tanpa henti.

**Recursive Case**  
  Jika `n` lebih besar dari 1, fungsi memanggil dirinya sendiri dengan nilai `n-1`, lalu mengalikan hasilnya dengan `n`.

### Contoh Perhitungan Faktorial 4!

- faktorial(4) = 4 × faktorial(3)
- faktorial(3) = 3 × faktorial(2)
- faktorial(2) = 2 × faktorial(1)
- faktorial(1) = 1 (base case)

Kemudian hasil dihitung mundur:

- faktorial(1) = 1
- faktorial(2) = 2 × 1 = 2
- faktorial(3) = 3 × 2 = 6
- faktorial(4) = 4 × 6 = 24

## Kesimpulan

- Fungsi membuat kode lebih terorganisir dan mudah digunakan kembali.  
- Rekursi memecah masalah faktorial menjadi bagian yang lebih kecil, menyelesaikannya secara bertahap hingga kondisi dasar.  
- Pendekatan ini sesuai dengan definisi matematis faktorial dan membuat kode lebih elegan dan mudah dipahami.

**Contoh Output Program:**
Masukkan angka untuk dihitung faktorialnya: 21
21! = 51090942171709440000

undefined

STUDI KASUS KEDUA

# Penjelasan Penggunaan Perulangan dan Array dalam Sistem Input Nilai Siswa dan Mencari Nilai Tertinggi

## Deskripsi Kasus
Seorang guru ingin membuat program yang dapat menerima input nilai dari 5 siswa, kemudian menentukan nilai tertinggi beserta siswa yang mendapatkannya.

## Penggunaan Perulangan (Loop)
**Apa itu perulangan?**  
  Perulangan adalah proses menjalankan satu bagian kode secara berulang-ulang. Dalam kasus ini, perulangan digunakan untuk meminta input nilai dari setiap siswa satu per satu.

**Fungsi perulangan dalam program ini:**  
  Program menggunakan `for i in range(5):` untuk mengulang proses input sebanyak 5 kali, yaitu untuk 5 siswa.  
  Setiap kali perulangan berjalan, program:  
  1. Meminta nilai siswa ke-`i+1`.  
  2. Menyimpan nilai tersebut ke dalam sebuah list.

**Keuntungan:**  
  Dengan perulangan, kita tidak perlu menulis kode input nilai siswa secara berulang-ulang, sehingga kode menjadi lebih singkat dan mudah dikelola.

## Penggunaan Array (List)
**Apa itu list?**  
  List adalah struktur data yang dapat menyimpan banyak nilai dalam satu variabel secara berurutan.

**Fungsi list `nilai_siswa` dalam program:**  
  List ini digunakan untuk menyimpan semua nilai siswa yang diinput.  
  Setiap nilai yang dimasukkan akan ditambahkan ke dalam list menggunakan `append()`.

**Manfaat list:**  
  Dengan menyimpan nilai dalam list, kita bisa dengan mudah melakukan operasi seperti mencari nilai tertinggi menggunakan fungsi `max()` dan mengetahui posisi siswa yang mendapat nilai tertinggi dengan `index()`.

## Cara Kerja Program Secara Singkat
1. Program meminta input nilai 5 siswa secara berulang menggunakan perulangan.  
2. Nilai yang dimasukkan disimpan dalam list `nilai_siswa`.  
3. Program mencari nilai tertinggi dari list tersebut.  
4. Program mencari indeks (nomor) siswa yang mendapatkan nilai tertinggi.  
5. Program menampilkan nilai tertinggi dan nomor siswa yang mendapatkannya.

## Kesimpulan
**Perulangan** memudahkan pengambilan input nilai secara berulang tanpa menulis kode berulang.  
**List** memungkinkan penyimpanan dan pengelolaan nilai siswa secara efisien agar mudah diolah dan dicari nilai tertingginya.

Dengan cara ini, program menjadi lebih rapi, efisien, dan mudah dipahami.


STUDI KASUS KETIGA

# Sistem Pemberian Diskon di E-Commerce

## Deskripsi
Program ini menghitung total pembayaran pelanggan setelah diberikan diskon berdasarkan total belanja. Pelanggan akan mendapatkan diskon sebesar 10% jika total belanja mereka lebih dari Rp500.000.

## Cara Kerja Program

1. Program meminta input berupa total belanja dari pengguna.
2. Program memeriksa apakah total belanja lebih dari Rp500.000.
3. Jika ya, program menghitung diskon 10% dari total belanja dan mengurangi total belanja dengan diskon tersebut.
4. Jika tidak, program tidak memberikan diskon dan total bayar sama dengan total belanja.
5. Program menampilkan informasi apakah pelanggan mendapatkan diskon atau tidak, serta total yang harus dibayar.

## Struktur Kontrol Percabangan

Program menggunakan struktur `if-else` untuk menentukan apakah pelanggan berhak mendapatkan diskon:

**Kondisi `if`**:  
  Jika `total_belanja > 500000`, maka diskon 10% diberikan.  
  Program menghitung dan menampilkan diskon serta total bayar setelah diskon.

**Kondisi `else`**:  
  Jika `total_belanja` kurang dari atau sama dengan Rp500.000, maka tidak ada diskon.  
  Program menampilkan pesan bahwa diskon tidak diberikan dan total bayar tetap sama.

## Contoh Penggunaan

Masukkan total belanja Anda (Rp): 1000000
Selamat! Anda mendapatkan diskon 10% sebesar Rp100,000.
Total yang harus dibayar: Rp900,000


## Kesimpulan

Struktur percabangan `if-else` sangat berguna untuk membuat keputusan dalam program berdasarkan kondisi tertentu. Dalam kasus ini, percabangan memudahkan program menentukan apakah pelanggan berhak mendapatkan diskon atau tidak sesuai dengan aturan bisnis yang berlaku.
