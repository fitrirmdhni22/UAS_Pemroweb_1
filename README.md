### Nama: Fitri Ramadhani
### NIM: 312410085
### Kelas: TI.24.A.1
### Mata Kuliah: Pemograman Web 1 (UAS)
### Dosen Pengampu: Agung Nugroho, S.Kom., M.Kom.

### Link Youtube: https://youtu.be/HWcQx_8NyvQ?si=Hbpnwy2-Og6yTglS

# 📱 Sistem Manajemen Barang

[![PHP Version](https://img.shields.io/badge/PHP-7.4%2B-777BB4?logo=php&logoColor=white)](https://www.php.net/)
[![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3-7952B3?logo=bootstrap&logoColor=white)](https://getbootstrap.com/)
[![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?logo=mysql&logoColor=white)](https://www.mysql.com/)

Sistem Manajemen Barang adalah aplikasi web berbasis PHP yang dirancang untuk mengelola data barang dan pengguna dengan antarmuka yang responsif dan mudah digunakan. Aplikasi ini dibangun dengan arsitektur modular yang memisahkan antara logika bisnis, tampilan, dan data.

Sistem Manajemen Barang adalah aplikasi web untuk mengelola data barang dan pengguna dengan antarmuka yang responsif dan mudah digunakan.

## 🌟 Fitur Utama

### 1. Manajemen Pengguna
- **Sistem Autentikasi**
  - Login/Logout aman dengan session management
  - Validasi form di sisi klien dan server
  - Proteksi terhadap serangan SQL Injection dan XSS
  - Session timeout otomatis untuk keamanan

- **Manajemen Profil**
  - Update data pribadi
  - Ganti password dengan konfirmasi
  - Upload foto profil
  - Riwayat aktivitas

- **Hak Akses Berbasis Peran**
  - Level Admin: Akses penuh ke semua fitur
  - Level User: Akses terbatas (hanya melihat dan mengedit profil sendiri)
  - Middleware otorisasi di setiap halaman

### 2. Manajemen Barang
- **Operasi CRUD**
  - Tambah barang baru dengan validasi data
  - Edit informasi barang yang ada
  - Hapus barang dengan konfirmasi
  - Pencarian real-time dengan AJAX

- **Fitur Tambahan**
  - Upload gambar produk
  - Kategori dan subkategori barang
  - Stok dan notifikasi stok minimum
  - Riwayat perubahan data

### 3. Antarmuka Pengguna
- **Desain Responsif**
  - Tampilan optimal di semua perangkat (mobile, tablet, desktop)
  - Navigasi yang mudah digunakan
  - Loading cepat dengan optimasi aset

- **Komponen UI Modern**
  - Form dengan validasi real-time
  - Tabel dengan pagination dan sorting
  - Notifikasi toast untuk feedback aksi
  - Modal dialog untuk konfirmasi

- **Pengalaman Pengguna**
  - Tampilan yang konsisten di semua halaman
  - Feedback visual untuk setiap interaksi
  - Pesan error yang informatif
  - Tema gelap/terang (opsional)

## 🛠️ Teknologi yang Digunakan

### Frontend
- **HTML5 & CSS3**
  - Semantic HTML untuk aksesibilitas
  - CSS3 dengan variabel untuk theming
  - Animasi dan transisi halus
  - Flexbox dan Grid untuk layout responsif

- **Framework & Library**
  - **Bootstrap 5.3** - Framework CSS untuk tampilan responsif
  - **Font Awesome 6** - Ikon vektor berkualitas tinggi
  - **jQuery 3.6+** - Library JavaScript untuk manipulasi DOM
  - **DataTables** - Plugin tabel interaktif
  - **Chart.js** - Visualisasi data dalam bentuk grafik
  - **SweetAlert2** - Modal dialog yang indah

### Backend
- **PHP 7.4+**
  - OOP (Object-Oriented Programming)
  - PDO untuk koneksi database yang aman
  - Prepared statements untuk mencegah SQL injection
  - Error handling yang baik

- **MySQL 8.0**
  - Relational database management system
  - Optimasi query untuk performa tinggi
  - Foreign key constraints untuk integritas data
  - Indexing untuk pencarian cepat

- **Keamanan**
  - Proteksi CSRF
  - Input validation dan sanitization
  - Password hashing dengan password_hash()
  - Proteksi terhadap XSS (Cross-Site Scripting)
  - Secure session management

### Alat Pengembangan
- **XAMPP/WAMP**
  - Lingkungan pengembangan lokal
  - PHP, MySQL, dan Apache dalam satu paket
  - phpMyAdmin untuk manajemen database

- **Version Control**
  - Git untuk pelacakan perubahan kode
  - GitHub/GitLab/Bitbucket untuk penyimpanan remote
  - Git Flow untuk manajemen cabang

- **Alat Bantu**
  - Composer untuk manajemen dependensi
  - VS Code dengan ekstensi PHP
  - Browser DevTools untuk debugging
  - Postman untuk pengujian API

## 🚀 Panduan Instalasi Lengkap

### 1. Persyaratan Sistem
#### Server
- **PHP 7.4 atau lebih baru** dengan ekstensi berikut:
  - PDO MySQL
  - OpenSSL
  - JSON
  - MBString
  - Fileinfo
  - GD Library (untuk manipulasi gambar)
  - cURL (untuk integrasi eksternal)

- **Database**
  - MySQL 8.0 atau MariaDB 10.4+
  - Minimal 100MB ruang disk
  - User dengan hak akses lengkap ke database

- **Web Server**
  - Apache 2.4+ dengan mod_rewrite
  - Atau Nginx dengan konfigurasi PHP-FPM
  - Direkomendasikan: Apache dengan PHP sebagai modul

### 2. Langkah-langkah Instalasi

#### 2.1. Persiapan Awal
```bash
# Clone repository (jika menggunakan Git)
git clone [repo-url]
cd uas_web

# Atau download dan ekstrak file ZIP
# Pastikan semua file ada di direktori web server (biasanya htdocs atau www)
```

#### 2.2. Konfigurasi Database
1. Buat database baru di MySQL/MariaDB
2. Import file SQL yang tersedia (jika ada)
   ```sql
   mysql -u username -p nama_database < database/backup.sql
   ```
3. Atau jalankan skrip inisialisasi database (jika tersedia)

#### 2.3. Konfigurasi Aplikasi
1. Salin file konfigurasi contoh
   ```bash
   cp config/database.example.php config/database.php
   ```

2. Edit file konfigurasi database
   ```bash
   nano config/database.php
   ```
   Sesuaikan dengan detail koneksi database Anda:
   ```php
   return [
       'host' => 'localhost',
       'dbname' => 'nama_database',
       'username' => 'user_database',
       'password' => 'password_aman',
       'charset' => 'utf8mb4'
   ];
   ```

3. Atur hak akses folder
   ```bash
   chmod -R 755 ./
   chmod -R 777 gambar/  # Folder upload
   chmod 644 config/database.php
   ```

#### 2.4. Konfigurasi Web Server
**Untuk Apache:**
Pastikan mod_rewrite diaktifkan dan file `.htaccess` berfungsi dengan menambahkan konfigurasi berikut di `httpd.conf` atau `.htaccess`:

```apache
<IfModule mod_rewrite.c>
    RewriteEngine On
    RewriteBase /uas_web/
    RewriteCond %{REQUEST_FILENAME} !-f
    RewriteCond %{REQUEST_FILENAME} !-d
    RewriteRule ^(.*)$ index.php?page=$1 [L,QSA]
</IfModule>
```

**Untuk Nginx:**
Tambahkan konfigurasi berikut di blok server:

```nginx
location / {
    try_files $uri $uri/ /index.php?$query_string;
}
```

### 3. Verifikasi Instalasi
1. Buka browser dan akses `http://localhost/uas_web`
2. Jika melihat halaman login, artinya instalasi berhasil
3. Login dengan kredensial default:
   - Admin: admin / admin123
   - User: user / user123

### 4. Troubleshooting
- **Error koneksi database**: Periksa kredensial di `config/database.php`
- **Halaman tidak ditemukan**: Pastikan mod_rewrite aktif dan konfigurasi web server benar
- **Gagal upload file**: Periksa izin folder `gambar/`
- **Error session**: Pastikan folder penyimpanan session memiliki izin yang tepat

## 🚀 Panduan Penggunaan

### 1. Memulai Aplikasi
1. **Persiapan**
   - Pastikan XAMPP/WAMP/LAMP sudah berjalan
   - Pastikan layanan Apache dan MySQL aktif
   - Buka browser favorit Anda

2. **Akses Aplikasi**
   - Buka alamat: `http://localhost/uas_web`
   - Akan muncul halaman login

### 2. Login ke Sistem
1. **Sebagai Admin**
   - Username: `admin`
   - Password: `admin123`
   - Fitur yang tersedia:
     - Manajemen pengguna
     - Manajemen barang
     - Laporan dan statistik
     - Pengaturan sistem

2. **Sebagai User Biasa**
   - Username: `user`
   - Password: `user123`
   - Fitur yang tersedia:
     - Melihat daftar barang
     - Mengedit profil sendiri
     - Melaporkan masalah

### 3. Mengelola Pengguna (Admin Only)
1. **Menambah Pengguna Baru**
   - Buka menu "Kelola Pengguna"
   - Klik tombol "Tambah Pengguna"
   - Isi formulir dengan data lengkap
   - Klik "Simpan"

2. **Mengedit Data Pengguna**
   - Cari pengguna yang ingin diedit
   - Klik ikon pensil pada baris yang sesuai
   - Lakukan perubahan
   - Klik "Update" untuk menyimpan

3. **Menghapus Pengguna**
   - Temukan pengguna yang akan dihapus
   - Klik ikon tempat sampah
   - Konfirmasi penghapusan
   - **Peringatan**: Tindakan ini tidak dapat dibatalkan

### 4. Manajemen Barang
1. **Menambahkan Barang**
   - Pastikan login sebagai admin
   - Buka menu "Data Barang"
   - Klik "Tambah Barang"
   - Isi formulir dengan lengkap
   - Upload gambar (opsional)
   - Klik "Simpan"

2. **Mengedit Data Barang**
   - Cari barang yang akan diedit
   - Klik ikon pensil
   - Lakukan perubahan
   - Klik "Update"

3. **Menghapus Barang**
   - Temukan barang yang akan dihapus
   - Klik ikon tempat sampah
   - Konfirmasi penghapusan

### 5. Fitur Tambahan
1. **Pencarian**
   - Gunakan kotak pencarian di bagian atas
   - Pencarian bisa berdasarkan nama, kode, atau deskripsi

2. **Filter Data**
   - Gunakan dropdown filter untuk menyaring data
   - Bisa difilter berdasarkan kategori, stok, dll.

3. **Ekspor Data**
   - Klik tombol "Ekspor"
   - Pilih format (PDF/Excel)
   - Data akan diunduh otomatis

### 6. Manajemen Profil
1. **Mengubah Profil**
   - Klik nama pengguna di pojok kanan atas
   - Pilih "Profil Saya"
   - Klik "Edit Profil"
   - Lakukan perubahan
   - Klik "Simpan Perubahan"

2. **Ganti Password**
   - Buka halaman profil
   - Klik "Ganti Password"
   - Masukkan password lama dan baru
   - Klik "Update Password"

### 7. Logout
1. Klik nama pengguna di pojok kanan atas
2. Pilih "Keluar"
3. Anda akan diarahkan ke halaman login

## 📂 Struktur Direktori

```
uas_web/
├── assets/                   # Aset statis
│   ├── css/                 # File stylesheet
│   │   └── style.css        # File CSS utama
│   └── img/                 # Gambar dan ikon
│       ├── HP IPHONE 17 PRO MAX.png
│       ├── HP OPPO.png
│       ├── HP SAMSUNG.png
│       ├── HP VIVO.png
│       └── HP XIAOMI.png
│
├── config/                   # File konfigurasi
│   └── database.php         # Konfigurasi koneksi database
│
├── gambar/                   # Gambar yang diunggah
│   ├── HP IPHONE 17 PRO MAX.png
│   ├── HP OPPO.png
│   ├── HP SAMSUNG.png
│   ├── HP VIVO.png
│   └── HP XIAOMI.png
│
├── modules/                  # Modul aplikasi
│   ├── auth/                # Autentikasi
│   │   ├── forgot-password.php  # Lupa password
│   │   ├── login.php             # Halaman login
│   │   ├── logout.php            # Proses logout
│   │   ├── register.php          # Pendaftaran pengguna
│   │   └── reset-password.php    # Reset password
│   │
│   └── user/                # Manajemen pengguna
│       ├── add.php          # Tambah pengguna
│       ├── delete.php       # Hapus pengguna
│       ├── edit.php         # Edit pengguna
│       ├── list.php         # Daftar pengguna
│       └── profile.php      # Profil pengguna
│
├── views/                   # Template tampilan
│   ├── footer.php          # Footer aplikasi
│   └── header.php          # Header aplikasi
│
├── .htaccess               # Konfigurasi server
├── index.php               # File entry point
└── README.md               # Dokumentasi ini
```

## 📱 Tampilan

### Halaman Login
<img width="1366" height="657" alt="image" src="https://github.com/user-attachments/assets/3aa4c0d5-15b9-481c-afc4-f7ca676f0006" />

### Halaman Lupa Password
<img width="1366" height="654" alt="image" src="https://github.com/user-attachments/assets/a77e487e-9f67-4b1a-b698-12df70110517" />

### Daftar Pengguna
<img width="1366" height="662" alt="image" src="https://github.com/user-attachments/assets/67f040e5-8409-4e03-8f2d-ebd2dedcc948" />
<img width="1366" height="667" alt="image" src="https://github.com/user-attachments/assets/52721451-902b-4132-a54f-8da9c0174aa9" />
<img width="1366" height="660" alt="image" src="https://github.com/user-attachments/assets/443eb563-bf04-4fb4-8f15-7a2151d70ec2" />

### Profil Pengguna
<img width="1366" height="680" alt="image" src="https://github.com/user-attachments/assets/63665d62-c259-48d4-8d2a-4d17a3bb8591" />
<img width="1366" height="679" alt="image" src="https://github.com/user-attachments/assets/3bdbd15c-a6cf-4328-8795-a58b16ed74c9" />

### Tampilan Mobile
<img width="1366" height="686" alt="image" src="https://github.com/user-attachments/assets/641ee2ea-c527-43d3-acac-c5e5f4e5eb29" />

### Tambah Barang (Admin)
<img width="1366" height="683" alt="image" src="https://github.com/user-attachments/assets/3ee78708-92f3-4b02-b354-dc6dee4d6a5b" />

### Ubah Barang (Admin)
<img width="1366" height="679" alt="image" src="https://github.com/user-attachments/assets/9e513339-b5ff-483a-b44b-d8564edfb3df" />

### Hapus Barang (Admin)
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/96151098-b052-445c-99b6-2e8cfc17ee0a" />

### Cari Barang (Admin)
<img width="1362" height="679" alt="image" src="https://github.com/user-attachments/assets/00b61421-96d5-4bbc-9db8-b5d415dcf7a3" />

### Halaman Admin
<img width="1366" height="662" alt="image" src="https://github.com/user-attachments/assets/57077dfd-51a7-40b6-91e4-06695977ce2c" />

### Halaman User
<img width="1366" height="673" alt="image" src="https://github.com/user-attachments/assets/a4c7a810-7de2-4cda-844a-7cf3657f911f" />

### Halaman Logout user dan admin
<img width="1365" height="666" alt="image" src="https://github.com/user-attachments/assets/60465569-00d4-4970-97f2-9dc449a8ab28" />
<img width="1366" height="688" alt="image" src="https://github.com/user-attachments/assets/17a5948f-517d-4d47-8007-5f3431dcd4a1" />

### Terima Kasih


