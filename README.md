# Polyglot File Generator

Polyglot File Generator adalah alat berbasis web sederhana namun ampuh yang memungkinkan Anda menyembunyikan file ZIP di dalam file media (Gambar atau Audio). File yang dihasilkan akan tetap berfungsi normal sebagai media, namun mengandung data rahasia di dalamnya yang bisa diekstrak kembali.

---

## Fitur Utama

- **100% Client-Side**: Semua pemrosesan file dilakukan langsung di browser Anda. Tidak ada data yang diunggah ke server, menjamin privasi dan keamanan data Anda.
- **Dukungan Multi-Format**:
  - **Host**: `.jpg`, `.jpeg`, `.png`, `.mp3`
  - **Guest**: `.zip`
- **Antarmuka Modern**: Menggunakan Tailwind CSS untuk desain yang responsif dan mode gelap (dark mode) yang nyaman.
- **Instan & Ringan**: Tanpa perlu instalasi tambahan, cukup buka file HTML di browser.

---

## Cara Kerja

Alat ini memanfaatkan karakteristik struktur file biner. File gambar/audio memiliki penanda akhir file (End of File), sementara program pembaca media biasanya mengabaikan data apa pun yang muncul setelah penanda tersebut. Alat ini menempelkan data ZIP tepat setelah data media asli.

1. **Host File** dibaca sebagai ArrayBuffer.
2. **Guest File (ZIP)** dibaca dan digabungkan di akhir buffer Host.
3. Hasilnya adalah file baru dengan identitas Host namun memiliki muatan ZIP di "ekor" filenya.

---

## Cara Penggunaan

1. **Pilih File Host**: Pilih file `.jpg`, `.jpeg`, `.png`, `.mp3`.
2. **Pilih File Guest**: Pilih file `.zip` yang berisi data.
3. **Nama Output (Opsional)**: Berikan nama untuk file hasil gabungan.
4. Klik **"GABUNGKAN FILE"**: File akan otomatis terunduh.

### Cara Membuka File Polyglot Sebagai Host:
Buka langsung file host dengan klik 2x pada file. Maka file host akan terbuka.

### Cara Membuka File Polyglot Sebagai Guest:
Buka menggunakan aplikasi ekstraktor seperti 7-Zip tanpa mengganti ekstensi file.

---

## ⚠️ Disclaimer

Proyek ini dibuat untuk tujuan edukasi dan riset keamanan. Penulis tidak bertanggung jawab atas penyalahgunaan alat ini. Selalu gunakan teknologi ini secara etis dan bertanggung jawab.

