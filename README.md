# Toko Sembako Yoga - Smart POS & Inventory System

Aplikasi web kasir warung sembako dengan fitur lengkap OCR scan resi supplier, manajemen stok, dan notifikasi kadaluarsa.

## 🚀 Features

- **Smart POS System** - Kasir cepat dengan autokomplete produk
- **Inventory Management** - Manajemen stok real-time dengan peringatan stok menipis
- **OCR Scan Resi Supplier** - Scan nota supplier otomatis dengan AI (Tesseract.js)
- **Expiry Date Tracking** - Notifikasi barang kadaluarsa
- **Sales Reports** - Dashboard laporan penjualan detail
- **PWA Ready** - Bisa diinstall di HP sebagai aplikasi
- **Offline Support** - Bekerja tanpa internet dengan Service Worker
- **Android APK** - Wrapper native untuk Android via Capacitor

## 📱 Akses Aplikasi

**Online Version (GitHub Pages):**
- https://smur1411-glitch.github.io/project/

**Local Development:**
1. Clone repo ini
2. Buka file `TOKO SEMBAKO YOGA.html` di browser
3. Atau jalankan simple HTTP server:
   ```bash
   python -m http.server 8000
   # atau
   npx http-server
   ```
   Akses di http://localhost:8000

## 📲 Install sebagai App

### Di Browser Desktop/Mobile:
1. Buka aplikasi di browser
2. Klik tombol **"Install App"** (muncul di atas)
3. Pilih "Install" atau "Add to Home Screen"

### Di Android via APK:
Lihat folder `/android` untuk build dan install APK native.

## 🛠️ Tech Stack

- **Frontend**: HTML5, CSS3, JavaScript (Vanilla)
- **Storage**: LocalStorage & IndexedDB (Browser)
- **OCR**: Tesseract.js (Client-side OCR)
- **PWA**: Service Worker, Manifest.json
- **Mobile**: Capacitor Framework (Android Wrapper)

## 📁 File Structure

```
├── TOKO SEMBAKO YOGA.html  # Main app (single file)
├── manifest.json            # PWA manifest
├── sw.js                    # Service Worker (offline cache)
├── icon.svg                 # App icon
├── www/                     # Web assets (for Capacitor)
└── android/                 # Android project (Capacitor wrapper)
```

## 💾 Data Storage

Semua data disimpan **di browser lokal** menggunakan:
- **LocalStorage**: Produk, penjualan, pembelian
- **IndexedDB**: Cache untuk offline mode
- **Tidak ada cloud sync** - Privacy first!

## 🔧 Build APK

```bash
cd android
./gradlew assembleDebug
# Output: app/build/outputs/apk/debug/app-debug.apk
```

Atau gunakan Android Studio:
1. File > Open > pilih folder `android/`
2. Build > Build APK
3. Hasilnya di `android/app/build/outputs/apk/debug/`

## 📝 Fitur Detail

### OCR Resi Supplier
- Ambil foto nota supplier
- AI otomatis parse nama barang, qty, harga
- Manual input teks nota juga tersedia

### Manajemen Stok
- Catat stok awal setiap produk
- Track pembelian & penjualan real-time
- Alert stok habis (< 0) dan menipis (< min qty)

### Peringatan Kadaluarsa
- Set tanggal exp di setiap produk
- Dashboard badge merah untuk expired/mendekati
- Laporan kadaluarsa per kategori

### Dashboard
- Summary: Total modal, omset hari ini, profit
- Daftar produk dengan status stok
- Grafik penjualan vs pembelian

## 📊 Laporan

- **Penjualan**: Per hari/bulan, detail transaksi
- **Pembelian**: History supplier, modal analisa
- **Stok**: Inventory opname, nilai stok
- **Produk**: List semua dengan harga modal/jual

## ⚙️ Pengaturan

- Nama toko & kontak
- Kategori produk custom
- Pajak/fee default
- Reset database (clear all data)

## 📄 License

Free & Open Source untuk usaha sendiri

---

**Dibuat dengan ❤️ untuk Warung Sembako Pak Yoga**
