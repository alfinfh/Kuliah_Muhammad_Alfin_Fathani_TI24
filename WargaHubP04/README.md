# WargaHub P04 — Android Studio

**Praktikum Pemrograman Mobile 04** — UX, RecyclerView, Fragment, Navigasi.

- Identitas: Muhammad Alfin Fathani — 240104040150 — TI24A
- Dosen pengampu: Muhayat, M.IT
- Bahasa: Kotlin + XML Views + ViewBinding
- Package: `id.antasari.p04.wargahub`
- `compileSdk = 36`, `targetSdk = 36`, `minSdk = 26`
- Android Gradle Plugin `9.3.3` dan Gradle `9.5.0`, sesuai konfigurasi P03 yang telah diperiksa.
- Proyek memakai data fiktif dalam memori, **tidak memiliki database / CRUD**.

## Menjalankan
1. Ekstrak ZIP dan buka **folder `WargaHubP04`** melalui Android Studio > Open.
2. Pastikan Android SDK Platform 36 terpasang; atur Gradle JVM ke JDK 25 seperti proyek P03.
3. Jalankan Gradle Sync; jika pertama kali perlu jaringan untuk library.
4. Pilih Pixel 7, tekan **Run app**.
5. Navigasi Beranda → Daftar (15 item) → Rincian; tombol Kembali dan mode kosong dapat diuji.

## Gradle wrapper
Skrip `gradlew` dan `gradlew.bat` disediakan bersama JAR bootstrap lokal untuk menjalankan Gradle 9.5.0.
Bootstrap tersebut menggunakan distribusi Gradle yang **sudah ada di cache pengguna** atau mengunduh dari alamat di `gradle-wrapper.properties` jika belum ada.
Ini bukan `gradle-wrapper.jar` resmi keluaran Gradle; jika kebijakan kelas mewajibkan JAR resmi, salin **hanya** `gradle-wrapper.jar` dari proyek P03 yang telah berfungsi atau jalankan `gradle wrapper --gradle-version 9.5.0` dari Gradle resmi.

## Screenshot minimum (diambil dari emulator asli)
01 Beranda; 02 Daftar 15 laporan; 03 Rincian; 04 Daftar kosong; 05 Landscape/font besar; 06 ID tidak ditemukan.

**Cara menguji ID tidak ditemukan:** untuk pengujian sementara saja, ubah `bundleOf(DetailFragment.ARG_ID to laporan.id)` menjadi `bundleOf(DetailFragment.ARG_ID to -99L)` pada `ListFragment.kt`, lalu Run, ambil screenshot, dan **kembalikan** `laporan.id` sebelum pengumpulan.

## Status pengujian
Kode dan struktur XML telah diperiksa secara statis. **Build dan pengujian emulator belum dijalankan** di lingkungan pembuatan ZIP; hasil aktual wajib dicatat setelah dijalankan pada laptop mahasiswa.
