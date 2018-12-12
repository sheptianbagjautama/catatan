Catatan Programming

#LARAVEL RESET PASSWORD SETTING
================================
<h2>configurasi file .env 
MAIL_DRIVER=smtp
MAIL_HOST=smtp.gmail.com
MAIL_PORT=587
MAIL_USERNAME="nama email host yang akan mengirimkan email"
MAIL_PASSWORD="password email host yang akan mengirimkan email"
MAIL_ENCRYPTION=tls
MAIL_FROM_ADDRESS="nama email yang akan dilihat oleh user pada saat pengiriman reset password digmail"
MAIL_FROM_NAME="nama subject di email pada saat pengiriman reset password gmail"</h2>


#LARAVEL MULTIAUTH ADMIN AND USER
1. gunakan auth bawaan laravel "php artisan make:auth"
2. buat model dan migrate terlebih dahulu untuk role admin "php artisan make:model Admin -m"
3. samakan isi file model dan migrasi dengan user
4. tambahkan auth baru file config/auth.php
5. perubahan di file Exception/Handler.php
6. duplicate folder auth(Controller) dan ubah namannya menjadi authAdmin
7. membuat file notifikasi dengan cara "php artisan make:notification AdminResetPasswordNotification"
8. duplicate juga folder auth(View) dan ubah namannya menjadi authAdmin
9. beberapa perubahan di file web untuk inisialisasi route
10. pengetesan email untuk reset password menggunakan log jika sudah production menggunakan smtp.gmail


Agar tidak terjadi error berikut "Specified key was too long error", kita harus config tipe database seperti ini 
di config/database.php
Lakukan perubahan pada dua bagian yang terdapat di ‘mysql’ setting :
Before
'charset' => 'utf8mb4',
'collation' => 'utf8mb4_unicode_ci',

After
'charset' => 'utf8',
'collation' => 'utf8_unicode_ci',

Note: Kita melakukan ini karena pada versi mysql yang lama kemungkinan akan menampilkan error character length pada table ketika kita melakukan migration. 







