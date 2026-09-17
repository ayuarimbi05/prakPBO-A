# Praktikum PBO - Rekening Bank

## Deskripsi

Project ini adalah tugas Praktikum Pemrograman Berorientasi Objek (PBO).

Program yang dibuat adalah program sederhana tentang rekening bank menggunakan Java dan PHP. Di dalam program terdapat beberapa proses seperti membuat rekening, setor uang, tarik uang, menghitung bunga, dan memotong biaya administrasi.

## Isi Project

```text
pertemuan2/
├── Main.java
├── RekeningBank.java
├── main.php
└── RekeningBank.php
```

## Fitur

Beberapa fitur yang ada di program ini:

- Membuat rekening
- Menambahkan saldo
- Mengurangi saldo
- Mengecek jumlah rekening
- Menghitung bunga tahunan
- Memotong biaya administrasi
- Memberikan batas pada penarikan
- Melakukan validasi pada saldo dan transaksi

## Konsep PBO

### Class dan Object

Class `RekeningBank` digunakan untuk membuat objek rekening.

Contoh:

```java
RekeningBank a = new RekeningBank("111", "Ani", 1_000_000);
```

### Constructor

Constructor digunakan saat membuat objek rekening untuk memberikan nilai nomor rekening, nama pemilik, dan saldo awal.

Program juga memiliki constructor sederhana yang otomatis menggunakan saldo awal 0.

### Constructor Delegation

Constructor sederhana menggunakan `this` untuk memanggil constructor yang memiliki saldo awal.

Contoh:

```java
public RekeningBank(String nomor, String pemilik) {
    this(nomor, pemilik, 0);
}
```

### Static Member

`static` digunakan untuk menghitung jumlah rekening yang sudah dibuat.

Contoh:

```java
private static int jumlahRekening = 0;
```

### Constant

Constant digunakan untuk menyimpan nilai tetap yang digunakan dalam program.

Contohnya adalah bunga tahunan:

```java
public static final double BUNGA_TAHUNAN = 0.025;
```

Selain bunga tahunan, terdapat juga biaya administrasi dan batas penarikan.

### Encapsulation

Data pada rekening seperti nomor rekening, nama pemilik, dan saldo dibuat `private`. Untuk mengambil data tersebut digunakan method seperti `getSaldo()` dan `getNomor()`.

### Validasi

Program juga memiliki validasi agar transaksi yang dilakukan sesuai. Misalnya saldo awal tidak boleh negatif, setoran harus lebih dari 0, dan penarikan tidak boleh melebihi saldo atau batas yang sudah ditentukan.

## Cara Menjalankan Java

Buka terminal pada folder `pertemuan2`, kemudian compile program dengan:

```powershell
javac RekeningBank.java Main.java
```

Setelah berhasil, jalankan dengan:

```powershell
java Main
```

## Cara Menjalankan PHP

Pastikan PHP sudah terpasang. Kemudian jalankan:

```powershell
php main.php
```

## Contoh Program

Program membuat tiga rekening:

- Ani dengan saldo awal Rp1.000.000
- Budi dengan saldo awal Rp0
- Citra dengan saldo awal Rp250.000

Setelah itu dilakukan beberapa operasi, seperti setor Rp500.000 ke rekening Ani, mencoba melakukan penarikan, memotong biaya administrasi Budi, dan menghitung bunga tahunan dari saldo Ani.

## Author

Nama: Ayu Arimbi  
NPM: 4525210140