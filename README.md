# GKPS Resort Medan Utara — Website v2
## Panduan Lengkap

---

## 📁 Isi Paket
```
gkps-resort-medan-utara/
├── index.html     ← Website publik (halaman utama)
├── admin.html     ← Dashboard Admin
└── README.md      ← Panduan ini
```

---

## 🚀 Cara Membuka
1. Ekstrak ZIP
2. Double-klik **`index.html`** → website publik terbuka di browser
3. Klik tombol **"Admin"** di pojok kanan atas → login ke dashboard admin

---

## 🔐 Login Admin
- **Username:** admin
- **Password default:** `admin123`
- ⚠️ **Harap ganti password** setelah login pertama melalui menu **Pengaturan Akun**

---

## 🏠 Fitur Website Publik (index.html)

### Halaman Utama
| Bagian | Keterangan |
|--------|-----------|
| **Hero** | Banner utama dengan nama gereja dan ayat Alkitab |
| **5 Kolom Jemaat** | Kampung Durian, Krakatau, Martubung, Belawan, Batang Sere |
| **4 Kolom Seksi Resort** | Bapa, Inang, Namaposo, Sekolah Minggu |
| **Pengurus Resort** | Daftar pengurus (diisi melalui Admin) |
| **Lokasi Sekretariat** | Alamat & kontak (diisi melalui Admin) |
| **Kegiatan Resort** | Galeri kegiatan dengan foto (diisi melalui Admin) |

### Halaman Jemaat (klik kartu jemaat)
Tab: **Beranda · Kebaktian · Sejarah · Seksi-Seksi · Kontak Person · Kegiatan**

### Halaman Seksi Resort (klik kartu seksi)
Tab: **Daftar Pengurus · Kegiatan Seksi · Lokasi & Sekretariat · Kontak Person · File Unduhan**

---

## ⚙️ Fitur Dashboard Admin (admin.html)

### Menu Admin
| Menu | Fungsi |
|------|--------|
| **Kegiatan Resort** | Tambah/hapus kegiatan dengan foto, tanggal, lokasi, deskripsi |
| **Kegiatan Jemaat** | Tambah/hapus kegiatan untuk tiap jemaat |
| **Kegiatan Seksi Resort** | Tambah/hapus kegiatan untuk tiap seksi |
| **Pengurus Resort** | Tambah/hapus pengurus yang tampil di homepage |
| **File Unduhan** | Upload/hapus file PDF/Word/Excel per seksi |
| **Info Sekretariat** | Edit alamat, telepon, email, jam pelayanan |
| **Pengaturan Akun** | Ubah password admin |

---

## 📸 Cara Tambah Kegiatan dengan Foto

1. Login ke `admin.html`
2. Pilih **"Kegiatan Resort"** (atau jemaat/seksi)
3. Isi form: **Judul, Tanggal, Waktu, Lokasi, Deskripsi**
4. Klik area upload foto → pilih gambar (maks 5 MB)
5. Klik **"Simpan Kegiatan"**
6. Kegiatan langsung muncul di website publik!

---

## 📂 Cara Upload File Unduhan

1. Login ke `admin.html`
2. Klik menu **"File Unduhan"**
3. Pilih seksi resort dari dropdown
4. **Klik area upload** atau **drag & drop** file
5. File langsung tersedia untuk diunduh pengunjung

---

## 🌐 Cara Pasang Online (Hosting Gratis)

### Opsi 1: Netlify (Termudah)
1. Daftar di [netlify.com](https://netlify.com) (gratis)
2. Klik "Add new site" → "Deploy manually"
3. Drag folder `gkps-resort-medan-utara` ke halaman Netlify
4. Website langsung online! Contoh: `gkps-medan-utara.netlify.app`

### Opsi 2: GitHub Pages
1. Daftar di GitHub, buat repository baru
2. Upload semua file ke repository
3. Settings → Pages → Source: main branch
4. Website online di `username.github.io/nama-repo`

---

## ⚠️ Catatan Penting tentang Penyimpanan Data

Data (kegiatan, foto, file, pengurus) disimpan di **localStorage browser**.
- ✅ Data tetap ada meski browser ditutup dan dibuka kembali
- ✅ Bekerja tanpa internet
- ⚠️ Data hanya ada di browser yang sama
- ⚠️ Hapus cache browser = data hilang
- ⚠️ Foto/file tersimpan sebagai base64, kapasitas browser ~5-10 MB

**Untuk production/online:** Disarankan migrasi ke backend (Firebase/Supabase gratis).
Hubungi pengembang untuk upgrade ke versi dengan database online.

---

## ✏️ Cara Edit Data Statis (Jadwal, Kontak, dll.)

Buka `index.html` dengan teks editor (Notepad/VS Code), cari:
```javascript
const churches = { ... }    // Data jemaat
const seksiData = { ... }   // Data seksi resort
```
Ubah sesuai kebutuhan, simpan, refresh browser.

---

*✝ Soli Deo Gloria — GKPS Resort Medan Utara*
