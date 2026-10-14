# Omni AI — proyek Android online tanpa API key pribadi

## Apa yang dibuat
Aplikasi Android sederhana bernama **Omni AI** yang membuka layanan percakapan AI online Duck.ai di dalam aplikasi. Tidak ada API key pribadi yang disimpan atau diminta oleh kode proyek ini. Aplikasi ini bukan model AI mandiri; jawaban diproses oleh layanan online dan internet wajib aktif.

Layanan tujuan awal: https://duck.ai/ . Layanan, akses tanpa akun, model yang tersedia, dan dukungan WebView bisa berubah. Jika situs tidak bekerja di dalam aplikasi, buka duck.ai lewat browser. Proyek ini tidak mengontrol server atau kuota Duck.ai.

## Batasan layanan gratis
- Gratis bukan berarti tanpa batas: penyedia dapat menerapkan batas penggunaan, ketersediaan model, antrean, pembatasan wilayah, atau mengubah ketentuannya.
- Model dan fitur yang tersedia dapat berubah; kualitas jawaban tidak dijamin benar.
- Perlu internet. Aplikasi ini **tidak bisa menjawab offline**.
- Jangan masukkan kata sandi, data pribadi sensitif, atau informasi rahasia ke layanan online.
- Ini pembungkus situs web (WebView), bukan integrasi API resmi dan bukan aplikasi yang berafiliasi dengan DuckDuckGo.
- Jika situs memblokir WebView, gunakan browser; jangan mencoba melewati pembatasan situs.

## Cara build APK melalui GitHub dari HP
1. Ekstrak ZIP ini di HP, lalu buat repositori baru di GitHub.
2. Unggah isi folder proyek ke repositori (pastikan folder `.github/workflows` ikut terunggah).
3. Buka tab **Actions**, pilih **Build Omni AI APK**, lalu tekan **Run workflow**. Jika diminta, aktifkan Actions untuk repositori.
4. Setelah job selesai dengan tanda hijau, buka run tersebut dan unduh artifact **OmniAI-debug-APK**.
5. Ekstrak artifact ZIP, lalu ketuk `app-debug.apk` untuk memasang. Android mungkin meminta izin “Install unknown apps” untuk aplikasi/file manager yang dipakai.
6. Untuk menghapusnya: Pengaturan Android → Aplikasi → Omni AI → Hapus instalasi.

Workflow menggunakan GitHub-hosted runner, Java 17, Android SDK 35, dan Gradle 8.9. Build belum dijalankan di lingkungan ini; jika gagal, lihat log di tab Actions. APK debug cocok untuk uji coba pribadi, bukan rilis Play Store.

## Build lokal
Buka proyek ini dengan Android Studio yang mendukung Android Gradle Plugin 8.7.3, Java 17, Android SDK 35, dan Gradle 8.9, lalu jalankan `assembleDebug`.
