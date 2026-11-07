# 🎄 Gali Dana B3 - Web Poster Christmas Edition

Repositori ini berisi source code untuk **single-page website Gali Dana (Open Pre-Order) bertema Natal** untuk Batch 3. Website ini dirancang sangat ringan, responsif, elegan, dan interaktif dengan fitur hitung mundur (*Live Countdown*), pergantian varian rasa dinamis (*Flavor Switcher*), serta integrasi langsung ke WhatsApp panitia.

---

## 🎨 Color Palette (Christmas Warmth)

Desain website menggunakan palet warna khusus bertema Natal yang hangat, manis, dan estetik:

| Warna | Hex Code | Nama Tema | Penggunaan |
|---|---|---|---|
| 🟡 Marshmallow | `#fffbe9` | Terang / Base | Background utama halaman & kartu soft |
| 🍪 Sugar Cookie | `#ffecc5` | Aksen Hangat | Background card countdown, info box, border hangat |
| ☕ Hot Cacao | `#562400` | Gelap / Teks | Teks judul, teks body, kontras tinggi, footer |
| 🎀 Ribbon | `#8f0500` | Aksen Merah Natal | Tombol utama, badge bestseller, harga |
| 🌲 Garland | `#044529` | Aksen Hijau Natal | Tombol order WhatsApp, tag viral, live indicator |

---

## ✨ Fitur Utama

1. **Live Countdown Penutupan PO:**
   - Hitung mundur *real-time* (Hari, Jam, Menit, Detik) menuju penutupan PO: **Kamis, 12 November 2026 pukul 23:59 WIB**.
   - Indikator status aktif dengan animasi denyut (*pulse*).
   - Otomatis menampilkan notifikasi saat periode PO berakhir.

2. **Interactive Flavor Switcher (Katalog Menu Dinamis):**
   - Saat varian rasa di-klik, foto makanan di atasnya langsung berganti secara *smooth* tanpa *reload* halaman.
   - Dilengkapi *fallback* SVG placeholder (`onerror`) agar gambar tidak pernah tampak rusak jika aset tertunda di-*load*.

3. **Filter Kategori Cepat:**
   - Tab filter instan: *Semua Menu (8)*, *🍰 Manis & Dessert (5)*, dan *🥟 Gurih & Pedas (3)*.

4. **Order Modal & Integrasi Direct WhatsApp:**
   - Ketika menekan tombol **Pesan via WA**, muncul pop-up untuk mengatur jumlah porsi, kalkulasi estimasi total harga otomatis, nama pemesan, catatan khusus (opsional), dan pilihan metode bayar.
   - Pilihan admin WhatsApp:
     - **Maria:** `+62 822-2876-4048`
     - **Yessy:** `+62 819-7718-2071`
   - Otomatis memformat teks pesan WhatsApp yang rapi, kasual, dan siap kirim.

5. **Info Pembayaran Transparan:**
   - Menerima **Cash (Tunai)** dan **QRIS / E-Wallet**.
   - Penekanan ramah dan kasual: *(Kalo pakai cash, diusahakan uangnya pas ya! Biar transaksi sat-set, lancar, dan tanpa repot kembalian 😉)*.

6. **Efek Salju Natal Ringan (CSS Only):**
   - Animasi butiran salju halus dan elegan tanpa membebani performa perangkat.
   - Dilengkapi tombol toggle `Salju: ON / OFF` di pojok kanan bawah.

---

## 📂 Struktur Folder Proyek

Untuk mencegah kesalahan *404 Not Found* saat di-*host* di **GitHub Pages**, struktur folder diatur seperti berikut:

```text
galidanab3/
│
├── index.html        # File utama (struktur HTML, CSS modern, & Vanilla JS)
├── README.md         # Dokumentasi panduan lengkap
└── assets/           # Folder penyimpanan gambar makanan & minuman
    ├── brownies choco chip.jpeg
    ├── brownies keju.jpeg
    ├── cheesecuit matcha.jpg
    ├── cheesecuit oreo.jpg
    ├── cheesecuit redvelvet.jpg
    ├── cheesecuit tiramisu.jpg
    ├── chocolate original detailed.jpg
    ├── logo bhakta.png
    ├── logo ti.png
    ├── lumpia ubi ungu coklat.jpeg
    ├── lumpia ubi ungu keju.jpeg
    ├── matcha cheese detailed.jpg
    ├── red velvet cheese detailed.jpg
    ├── salad.png
    ├── samyang roll new detailed.jpg
    ├── tahu kocek.jpeg
    └── wonton chili oil.jpeg
```

---

## 📸 Daftar Aset & Pemetaan Varian Menu

Berikut adalah daftar nama file yang berada di folder `./assets/` beserta fungsinya di website:

| No | Nama Menu | Harga | Pilihan Varian Rasa | Path File Gambar |
|---|---|---|---|---|
| 1 | **Cheesecuit** | Rp 12.000 | Tiramisu (Default)<br>Matcha<br>Oreo<br>Red Velvet | `./assets/cheesecuit tiramisu.jpg`<br>`./assets/cheesecuit matcha.jpg`<br>`./assets/cheesecuit oreo.jpg`<br>`./assets/cheesecuit redvelvet.jpg` |
| 2 | **Brownies Choco Chip** | Rp 13.000 | Choco Chip (Default)<br>Keju Melimpah | `./assets/brownies choco chip.jpeg`<br>`./assets/brownies keju.jpeg` |
| 3 | **Lumpia Ubi Ungu Coklat** | Rp 15.000 | Coklat Lumer (Default)<br>Keju Gurih | `./assets/lumpia ubi ungu coklat.jpeg`<br>`./assets/lumpia ubi ungu keju.jpeg` |
| 4 | **Soft Cookie** | Rp 8.000 | Chocolate Original (Default)<br>Matcha Cheese<br>Red Velvet Cheese | `./assets/chocolate original detailed.jpg`<br>`./assets/matcha cheese detailed.jpg`<br>`./assets/red velvet cheese detailed.jpg` |
| 5 | **Wonton** | Rp 12.000 | Original Chili Oil | `./assets/wonton chili oil.jpeg` |
| 6 | **Samyang Roll** | Rp 14.000 | Samyang Spicy Roll (Isi 3 Pcs) | `./assets/samyang roll new detailed.jpg` |
| 7 | **Tahu Kocek** | Rp 13.000 | Cabe Rawit Ulek | `./assets/tahu kocek.jpeg` |
| 8 | **Salad** | Rp 13.000 (300ml) | Saus Creamy Keju | `./assets/salad.png` |

---

## 🚀 Panduan Deploy ke GitHub Pages

Repo target: `https://github.com/noobien1/galidanab3`

1. **Inisialisasi Git dan Push ke GitHub:**
   ```bash
   git init
   git add .
   git commit -m "feat: website gali dana b3 christmas edition"
   git branch -M main
   git remote add origin https://github.com/noobien1/galidanab3.git
   git push -u origin main
   ```

2. **Aktifkan GitHub Pages:**
   - Buka repositori di GitHub: `https://github.com/noobien1/galidanab3`
   - Klik tab **Settings** > menu samping **Pages**.
   - Pada bagian **Build and deployment > Source**, pilih **Deploy from a branch**.
   - Pilih Branch: `main` dan folder: `/ (root)`.
   - Klik **Save**.
   - Tunggu 1–2 menit, website kamu akan aktif di URL:
     `https://noobien1.github.io/galidanab3/`

### ⚠️ Catatan Kritis Relative Path:
Semua pemanggilan gambar di HTML dan JavaScript wajib menggunakan **Relative Path** yang diawali `./` (contoh: `./assets/gambar.jpg`). Jangan menggunakan `/assets/...` karena di GitHub Pages URL tersebut akan mencari ke root domain (`noobien1.github.io/assets/...`) sehingga menyebabkan error **404 Not Found**.

---

## 🛠️ Panduan Kustomisasi Cepat

- **Mengubah Harga:** Buka `index.html`, cari komentar `<!-- Ganti harga di sini jika diperlukan -->` dan ubah teks harga sesuai kebutuhan.
- **Mengubah Batas Countdown:** Cari baris `const targetDate = new Date('2026-11-12T23:59:59+07:00').getTime();` di bagian `<script>` dan sesuaikan tanggalnya.
- **Mengubah Kontak WhatsApp:** Cari objek `ADMINS` di bagian `<script>`:
  ```javascript
  const ADMINS = {
    maria: { name: 'Maria', number: '6282228764048' },
    yessy: { name: 'Yessy', number: '6281977182071' }
  };
  ```

---

Dibuat dengan ❤️ untuk mensukseskan **Gali Dana Batch 3 Christmas Edition**. Selamat berjualan! 🎄✨

