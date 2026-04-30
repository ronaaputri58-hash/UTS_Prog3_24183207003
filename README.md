Ronaa Putri Indana Zulfa
24183207003
PTI 4A

1. Inisialisasi Komponen (Constructor)
​Di dalam public pertemuan6(), kamu menyiapkan tampilan awal:
​ButtonGroup: Digunakan agar pilihan RadioButton bersifat eksklusif (hanya bisa pilih satu). buttonGroup1 untuk tipe pemesanan (makan di tempat/bawa pulang), dan buttonGroup2 untuk metode pembayaran (kasir/QRIS).
​Tanggal Otomatis: Menggunakan SimpleDateFormat untuk mengambil tanggal sistem hari ini dan menampilkannya di tanggal_field. Field ini diatur .setEditable(false) agar user tidak bisa mengubah tanggal secara manual.
​ComboBox (Dropdown): Mengisi pilihan kategori menu (Makanan, Snack, Ice, Coffe).
​2. Memilih Menu (dropdown_kategoriActionPerformed)
​Fungsi ini berjalan saat user memilih kategori di dropdown:
​Menggunakan logika if-else untuk menentukan daftar makanan/minuman yang akan muncul di JList (list_menu).
​Data menu ditulis dalam format Nama Menu - Harga. Format ini penting karena nanti akan "dipotong" (split) saat proses perhitungan.
​list_menu.setListData(data) berfungsi memperbarui daftar menu yang tampil di layar.
​3. Menambah ke Keranjang (tambahActionPerformed)
​Ini adalah logika "Add to Cart":
​Validasi: Mengecek apakah user sudah memilih menu dari list. Jika belum, muncul pesan peringatan.
​Parsing Harga: Karena format list adalah Nama - Harga, koding kamu menggunakan split(" - ").
​potong[0] diambil sebagai nama.
​potong[1] diambil sebagai harga, lalu dibersihkan dari titik (replace) dan diubah menjadi angka (Integer.parseInt).
​Akumulasi: Variabel daftar_pesanan menyimpan daftar menu dalam bentuk teks panjang (String), dan totalSemua menjumlahkan harga setiap kali tombol tambah diklik.
​4. Proses Transaksi (pesanActionPerformed)
​Ini adalah bagian final untuk mencetak struk:
​Validasi RadioButton: Mengecek apakah user sudah memilih tipe pesanan dan metode bayar. Jika belum, proses dihentikan (return).
​Cek Keranjang: Jika daftar_pesanan masih kosong, user diminta menambah menu dulu.
​Output Ringkasan: Menggabungkan semua data (Nama pemesan, No Meja, daftar menu, dan total harga) ke dalam satu String ringkasan.
​JOptionPane: Menampilkan struk/ringkasan tersebut dalam kotak dialog pesan.
​Reset: Setelah pesan berhasil, semua variabel dan inputan (keranjang, total, nama pemesan) dikosongkan kembali agar siap untuk pesanan berikutnya.

# UTS_Prog3_24183207003
