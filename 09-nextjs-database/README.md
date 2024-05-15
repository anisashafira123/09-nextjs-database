`Nama : Anisa Shafira`

`NIM : 2341727005`

`Link Vercel`

https://09-nextjs-database-zeta.vercel.app/

# Praktikum 1: Setup Database dan Fetching Data

Berhasil deploy di server Vercel

![Screenshot (236)](/image/1%20(2).png)

`Soal 1. Jelaskan apa yang telah Anda pelajari?`
Dengan memanfaatkan Vercel, pengembang dapat dengan mudah membangun, mendeploy, dan mengelola situs web serta aplikasi front-end. Setiap kali pengembang membuat perubahan pada proyek dan mengirimkannya ke repositori git, Vercel akan secara otomatis mendeteksi perubahan tersebut dan melakukan deploy baru hanya dalam hitungan detik. Ini memungkinkan pengembang untuk langsung melihat perubahan mereka di lingkungan produksi dengan cepat dan tanpa kesulitan.

`Soal 2 : Membuat basis data Postgres`

![Screenshot (237)](/image/2.png)

Vercel juga bisa digunakan untuk membuat database. Dalam praktikum ini, kita telah mencoba membuat database Postgres. Untuk mengakses database tersebut, kita membuat file .env yang berisi kode dari Vercel. Kemudian, file .env tersebut ditambahkan ke file .gitignore agar saat kita mengunggah ke GitHub, kode dalam .env tidak terbaca.

`Soal 3. Melakukan seed ke basis data`

![npm run seed](/image/3.png)

Awalnya error, namun setelah menginstallnya terlebih dahulu dengan perintah npm i --save dotenv
dan npm i --save bcrypt serta mengubah kode di seed.js menjadi seperti ini: require('./data.js') berhasil melakukan seed ke basis data

`Soal 4. Menjelajah Basis Data`
Buka akun vercel , cek pada sidenav klik Data kemudian akan melihat tabel berisi : users, customers, invoices, dan revenue

![Screenshot (238)](/image/4.png)

Eksekusi Query SQL 

![Screenshot (239)](/image/5.png)

Perintah SQL tersebut digunakan untuk mengambil data dari dua tabel, yaitu invoices dan customers, dan mengembalikan daftar nama pelanggan serta jumlah tagihan tertentu

# Praktikum 1: Fetching Data
Membuat global Query (Model) dan menambahkan kode yang ada.

![modul global](/image/6.png)

`Jawaban soal 5`

![Screenshot (234)](/image/7.png)

Setelah menambahkan kode di setiap komponen maka hasil dashboard akan muncul

`Fetching Data untuk Komponen RevenueChart`
src\app\page.tsx

![Screenshot 2024-05-15 122142](/image/8.png)

`Jawaban soal 6`

![Screenshot 2024-05-15 121821](/image/9.png)

halaman React yang menampilkan sebuah dashboard dengan chart

`Soal 7. Fetching Data untuk komponen LatestInvoices`

untuk profile gambar

![public](/image/10.png)

Buka src\app\page.tsx kemudian lakukan import komponen LatestInvoices, lalu hapus comment pada komponen LatestInvoices di dalam fungsi Page(). Hasilnya akan melihat 5 data yang diambil dari basis data (bagian Latest Invoices).

![soal7](/image/11.png)

# Tugas Praktikum

src\app\page.tsx

![Screenshot (242)](/image/12.png)

src\app\components\molecules\card.tsx

![Screenshot (241)](/image/13.png)
![Screenshot (241)](/image/14.png)

Hasil

![Screenshot (235)](/image/15.png)

Perhatikan fungsi fetchCardData() (pada file src\model\query.tsx) dari soal nomor 1. Jelaskan maksud kode dan kueri yang dilakukan dalam fungsi tersebut!

`kode tersebut adalah serangkaian fungsi yang digunakan untuk mengambil data dari database PostgreSQL. Ada fungsi-fungsi untuk mengambil data pendapatan, tagihan terbaru, data kartu dashboard, tagihan yang difilter, halaman tagihan, pelanggan, pelanggan yang difilter, dan pengguna berdasarkan alamat email. Semua fungsi ini menggunakan modul @vercel/postgres untuk berinteraksi dengan database dan ada juga penggunaan fungsi formatCurrency() untuk mengubah format mata uang.`

`Link Vercel`

https://09-nextjs-database-zeta.vercel.app/

