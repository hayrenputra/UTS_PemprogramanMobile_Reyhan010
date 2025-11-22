Berikut daftar widget Flutter yang digunakan dalam project TokoAhMeng dari skripmu, beserta fungsi utamanya — diurutkan sesuai urutan tampilan dan navigasi aplikasi dari start sampai detail produk.



APP START:
- MaterialApp
  - Fungsi: root/widget utama aplikasi Flutter, mengatur tema, routing halaman.
- runApp()
  - Fungsi: memanggil widget utama aplikasi (TokoAhMengApp).



HomePage:
- Scaffold
  - Fungsi: kerangka dasar halaman, menyediakan appBar, body, dll.
- AppBar
  - Fungsi: header halaman, menampung judul aplikasi.
- Container
  - Fungsi: membungkus dan memberi dekorasi (background gradient).
- ListView.builder
  - Fungsi: menampilkan list kategori secara vertikal dan bisa di-scroll.
- Card
  - Fungsi: menampilkan kategori dengan tampilan kotak, shadow, dan border.
- ListTile
  - Fungsi: konten kategori, berisi icon (kategori) + label + icon navigasi.
- Icon
  - Fungsi: visual ikon untuk tiap kategori.
- Text
  - Fungsi: menampilkan nama kategori.
- onTap (ListTile)
  - Fungsi: navigasi ke ProductListPage (menggunakan `Navigator.pushNamed` dan membawa data kategori).



ProductListPage:
- Scaffold
  - Fungsi: struktur dasar halaman katalog produk.
- AppBar
  - Fungsi: header, memunculkan judul kategori terpilih.
- Column
  - Fungsi: menata dropdown sort dan katalog produk secara vertikal.
- DropdownButton
  - Fungsi: memilih urutan/sortir produk (Nama/Harga).
- GridView.count
  - Fungsi: menampilkan produk dalam grid (kotak 2/4 kolom responsif).
- GestureDetector
  - Fungsi: membungkus card produk agar bisa di-tap untuk navigasi ke detail.
- Container
  - Fungsi: memberi layout tetap bentuk square/kotak pada card produk.
- Card
  - Fungsi: tile produk, border dan shadow kecil untuk visual kotak.
- Padding
  - Fungsi: beri ruang agar isi Card tidak mepet ke border.
- Column
  - Fungsi: menata icon, nama produk, dan harga secara vertikal di Card.
- Icon
  - Fungsi: menampilkan icon produk.
- Text
  - Fungsi: nama produk dan harga.
- Stack & Positioned
  - Fungsi: memposisikan tombol favorit hati di pojok kanan atas dalam square card.
- onTap Card(product)
  - Fungsi: navigasi ke ProductDetailPage dengan data produk terpilih.



ProductDetailPage:
- Scaffold
  - Fungsi: struktur dasar halaman.
- AppBar
  - Fungsi: header, sudah ada tombol back otomatis.
- SingleChildScrollView
  - Fungsi: memungkinkan halaman detail di-scroll jika konten lebih panjang dari viewport.
- Padding
  - Fungsi: ruang tepi agar konten detail lebih rapi.
- Column
  - Fungsi: menata layout detail produk secara vertikal.
- Container + ClipRRect
  - Fungsi: area khusus icon produk besar dalam card border bulat.
- Icon
  - Fungsi: icon utama produk (besar di atas).
- SizedBox
  - Fungsi: jarak antar elemen di tampilan.
- Card
  - Fungsi: penampung detail produk (nama, harga, deskripsi).
- Text
  - Fungsi: menampilkan nama produk, harga, dan deskripsi.

- onTap back (AppBar)
  - Fungsi: navigasi otomatis kembali ke ProductListPage.
