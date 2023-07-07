# Aplikasi Kasir Sederhana
Aplikasi Kasir sederhana dengan Bahasa Python untuk Project Pacmann

# Latar Belakang
Andi adalah seorang pemilik supermarket besar di salah satu kota di Indonesia. Andi memiliki rencana untuk melakukan perbaikan proses bisnis, yaitu Andi akan membuat sistem kasir yang self-service di supermarket miliknya. Sehingga customer bisa langsung memasukkan item yang dibeli, jumlah item yang dibeli, dan harga item yang dibeli dan fitur yang lain.
Sehingga customer yang tidak berada di kota tersebut bisa membeli barang dari supermarket tersebut. Setelah Andi melakukan riset, ternyata Andi memiliki masalah, yaitu Andi membutuhkan Programmer untuk membuatkan fitur - fitur agar bisa sistem kasir self-service di supermarket itu bisa berjalan dengan lancar.

# Requirements / Objective
- Customer dapat membuat id transaksi
- Customer dapat memasukan nama item, jumlah item dan harga barang
- Jika ada kesalahan, tetapi tidak ingin menghapus itemnya, customer bisa update nama item atau update jumlah item dan atau update harga item
- Jika batal membeli item belanjaan, customer bisa menghapus salah satu item dari nama item atau langsung menghapus semua transaksi atau reset transaksi
- Ketika sudah selesai belanja, customer bisa melakukan check order untuk memeriksa pesanan yang di masukan sudah benar atau belum
- Customer dapat menghitung total belanja yang sudah dipesan, kemudian terdapat ketentuan sebagai berikut :
    - Jika total belanja di atas Rp 200.000 maka akan mendapatkan diskon 5%
    - Jika total belanja di atas Rp 300.000 maka akan mendapatkan diskon 8%
    - Jika total belanja di atas Rp 500.000 maka akan mendapatkan diskon 10%
   
# Flowcart
![Logo](https://github.com/ifanislami/python-ifan/blob/main/pictures/Flowchart.png)

# Function dan Atribut
- ```Self.items``` : Atribut yang berupa dictionary yang berfungsi untuk menyimpan data transaksi yang dilakukan oleh customer
```self.trnsct_123``` : Atribut untuk menjalankan class yang di-extend (Transaction) dan menginisialisasi objek dari class Transaction yang diberi nama trnsct_123
- ```add_item``` : Method yang berfungsi untuk menambahkan list produk yang telah dimasukkan oleh customer yang berisi nama item, jumlah item, dan harga item
- ```update_name``` : Method yang berguna untuk mengubah nama item yang ingin diganti
- ```update_qty``` : Method yang berguna untuk mengubah jumlah item yang di-order
- ```update_price``` : Method yang berfungsi untuk mengubah harga item yang dibeli
- ```remove_item``` : Method yang digunakan untuk menghapus item tertentu
- ```reset_transaction``` : Method yang digunakan untuk menghapus seluruh data transaksi
- ```check_order``` : Method yang berfungsi untuk menampilkan seluruh data transaksi yang telah dibuat
- ```total_harga``` : Method untuk menghitung total harga/item
- ```total_price``` : Method yang digunakan untuk menampilkan total harga seluruh produk
- ```Main_menu``` : Method menampilkan menu utama aplikasi kasir. Pada menu tersebut terdapat 9 pilihan seperti tambah pesanan, periksa pesanan, update nama pesanan dan sebagainya. Saat user memasukkan pilihannya, program akan mengeksekusi perintah sesuai dengan pilihan yang dipilih. 

# Test Case
* Test 1:

Customer ingin menambahkan item baru menggunakan method ```add_item()``` dan memeriksa item yang ditambahkan menggunakan method ```check_order()```,  dengan sebagai berikut:

    - Nama item Ayam Goreng, Qty: 2, Harga: 20000
    - Nama item Pasta Gigi. Qty: 3, Harga:15000

![Link](https://github.com/ifanislami/python-ifan/blob/main/pictures/TestCase1.png)

- Test 2:

Ternyata customer salah membeli salah satu item dari belanjaannya, maka customer menggunakan method ```delete_item()```. Item yang ingin dihapus adalah Pasta Gigi.

![Link](https://github.com/ifanislami/python-ifan/blob/main/pictures/TestCase2.png)

- Test 3:

Setelah dipikir kembali customer salah memasukan semua item yang dibelanjakannya. Daripada menghapus satu-satu, maka customer cukup menggunakan method ```reset_transction()```.

![Link](https://github.com/ifanislami/python-ifan/blob/main/pictures/TestCase3.png)

- Test 4:

Setelah customer selesai belanja, maka akan menghitung total belanja yang harus dibayar menggunakan method ```total_price()```. Sebelum mengeluarkan total belanja yang dibayar, akan menampilkan semua item yang dibeli. 

![Link](https://github.com/ifanislami/python-ifan/blob/main/pictures/TestCase4.png)

# Saran Perbaikan
Mungkin kedepan bisa coba diujikan lgsg ke customer, lalu lebih baik bisa dibuatkan file database untuk menyimpan transaksi dalam waktu yang lama untuk rekap. Mengingat script ini hanya menyimpan data untuk sementara, ketika direstart maka data kembali terhapus.
