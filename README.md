# advprog-modul6

# Mahoga Aribowo Heryasa

# 2206025230

###  Commit 1 Reflection notes

Pada fungsi `main()`, `TCPListener` digunakan untuk membaca koneksi TCP dari server. `TCPListener` mengembalikan kumpulan `Stream` atau koneksi terbuka dari server dan client. Setiap `Stream` yang masuk akan di handle oleh method `handle_connection`. Didalam method tersebut, `BufReader` digunakan untuk membaca data dari `Stream`. Lalu, dengan method `.lines()` data yang dibaca akan dipisahkan per baris berdasarkan kemunculan *newline*. Dengan method `.map` setiap result dari hasil method `.lines()` dipetakan menjadi string dengan memanggil method `.unwrap()`. Kemudian, method `take_while()` akan melakukan *loop* sampai menemukan baris kosong untuk mengambil setiap baris. Terakhir, method `.collect` akan mengumpulkan setiap baris yang telah diambil dan merubah nya menjadi vector yang disimpan pada variabel `http_request`. Hasil `http_request` kemudian di print pada konsol terminal untuk menunjukkan detail request yang diberikan oleh client.      