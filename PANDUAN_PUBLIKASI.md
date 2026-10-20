# Panduan Publikasi Ai Technician87

## A. Publikasi gratis dengan GitHub Pages

### 1. Siapkan akun dan folder

1. Buat atau masuk ke akun di https://github.com/.
2. Unduh dan ekstrak ZIP paket website ke komputer atau ponsel. Pastikan `index.html` berada di folder teratas bersama folder `assets/`.
3. Periksa website di browser lokal terlebih dahulu. Navigasi, tombol WhatsApp, formulir, gambar, dan peta sebaiknya diuji sebelum diunggah.

### 2. Buat repository

1. Di GitHub, tekan tombol **+** lalu pilih **New repository**.
2. Isi nama, misalnya `ai-technician87-site`.
3. Pilih **Public** bila menggunakan GitHub Free, karena GitHub Pages di akun Free membutuhkan repository publik.
4. Tekan **Create repository**.

### 3. Unggah semua file

1. Pada halaman repository, pilih **Add file → Upload files**.
2. Unggah `index.html`, `.nojekyll`, `README.md`, `PANDUAN_PUBLIKASI.md`, serta folder `assets/` lengkap dengan subfolder dan file aslinya.
3. Jangan hanya mengunggah `index.html`; tanpa folder `assets/`, logo, favicon, dan foto tidak akan tampil.
4. Tulis pesan commit misalnya `Tambah landing page Ai Technician87`, lalu pilih **Commit changes**.

### 4. Aktifkan Pages

1. Buka repository → **Settings** → **Pages**.
2. Pada **Build and deployment**, di bagian **Source** pilih **Deploy from a branch**.
3. Pilih branch `main` dan folder `/(root)`, lalu tekan **Save**.
4. Buka bagian Pages atau tab **Actions** untuk memantau hasil deploy. Setelah berhasil, GitHub akan menampilkan URL situs, biasanya berbentuk `https://NAMA-USER.github.io/ai-technician87-site/`.
5. Tunggu proses deploy selesai, lalu buka URL tersebut di HP dan laptop. Jika baru saja mengaktifkan Pages, publikasi dapat memerlukan beberapa menit.

> Semua file yang dipublikasikan di website akan dapat diakses publik. Jangan mengunggah password, kunci API privat, dokumen pelanggan, atau data pribadi yang tidak semestinya dipublikasikan.

### 5. Uji sebelum dibagikan

- Uji tautan WhatsApp dari hero, navbar, kartu layanan, tombol mengambang, dan footer.
- Isi form dengan data tidak valid untuk memastikan pesan error muncul; kemudian coba data valid dan pastikan WhatsApp terbuka dengan draf yang sesuai.
- Periksa seluruh gambar dan ikon. Jika ada yang tidak tampil, periksa ejaan folder/nama file, termasuk huruf besar-kecil.
- Uji menu hamburger, FAQ, alamat email, telepon, peta, dan tautan media sosial.
- Pastikan situs tetap nyaman dibaca di layar ponsel.

### 6. Perbarui metadata setelah URL final diketahui

Buka `index.html`, cari `og:image`, `twitter:image`, `image` dalam JSON-LD, lalu ubah nilai gambar menjadi URL absolut website yang sudah tayang. Contoh bentuk URL: `https://NAMA-USER.github.io/ai-technician87-site/assets/img/og-image.jpg`. Tambahkan `og:url` dan `<link rel="canonical">` dengan URL halaman yang benar-benar dipakai. Jangan gunakan URL contoh itu mentah-mentah sebelum mengganti nama akun/repository.

### 7. Tentang performa

Halaman ini memakai Tailwind Play CDN sesuai permintaan. Halaman dapat dijalankan sebagai file statis, tetapi CDN browser lebih cocok untuk prototipe dibandingkan build CSS produksi yang dioptimalkan. Jika trafik berkembang, pindahkan Tailwind ke proses build agar CSS final lebih kecil. Website saat ini tidak memerlukan backend karena form diteruskan ke WhatsApp.

---

## B. Integrasi website dengan Google Business Profile

1. Masuk ke akun Google pemilik usaha, lalu buka https://business.google.com/.
2. Klaim atau buat profil **Ai Technician87** bila memang memenuhi syarat dan profil belum tersedia. Lengkapi nama bisnis yang digunakan di dunia nyata, kategori paling relevan, nomor telepon, alamat atau area layanan, serta jam operasional yang benar.
3. Selesaikan proses verifikasi yang ditawarkan Google. Metode verifikasi ditentukan oleh Google dan dapat berbeda menurut bisnis.
4. Buka profil yang dikelola melalui Google Search atau Google Maps, lalu pilih **Edit profile**. Cari bagian **Contact/Kontak** dan isi kolom **Website** dengan URL GitHub Pages yang sudah terbit. Simpan perubahan.
5. Isi area layanan yang benar-benar dapat dijangkau, misalnya Kota Makassar dan Kabupaten Gowa. Jangan memilih area yang tidak dilayani.
6. Bila pelanggan tidak dilayani di alamat rumah/kantor yang didaftarkan dan bisnis hanya mendatangi lokasi pelanggan, ikuti kebijakan Google untuk service-area business: sembunyikan alamat pelanggan-facing dan tampilkan area layanan. Jika pelanggan memang dilayani di alamat tersebut dan persyaratan storefront terpenuhi, konfigurasi hybrid mungkin sesuai.
7. Tambahkan foto aktual hasil pekerjaan, logo, layanan, dan pembaruan yang relevan pada profil. Minta ulasan hanya dari pelanggan yang benar-benar memakai jasa; jangan membuat ulasan, rating, atau testimonial fiktif.
8. Pastikan nama, nomor telepon, alamat, dan cakupan layanan konsisten antara website dan profil Google.

**Penting:** alamat yang tercantum di website adalah alamat bisnis yang diberikan pemilik. Sebelum menjadikannya alamat pelanggan-facing di Google, pastikan lokasi tersebut memang menerima pelanggan dan memenuhi kebijakan Google. Jika alamat hanya tempat tinggal atau titik operasional tanpa kunjungan pelanggan, atur sebagai bisnis area layanan dan sembunyikan alamat sesuai aturan.

---

## C. Cara mengganti peta Google Maps

### Metode praktis (tanpa API key)

1. Buka https://maps.google.com/ dan cari alamat bisnis yang akurat.
2. Pastikan pin yang dipilih benar-benar menunjuk lokasi usaha, bukan sekadar pusat kelurahan.
3. Klik **Bagikan/Share** → pilih tab **Sematkan peta/Embed a map**.
4. Pilih ukuran peta bila diperlukan, tekan **Salin HTML/Copy HTML**.
5. Buka `index.html`, cari komentar `GOOGLE MAPS / SERVICE AREA`, lalu temukan elemen `<iframe title="Peta lokasi ...">`.
6. Ganti nilai `src` dengan nilai `src` dari iframe Google Maps yang disalin. Pertahankan `title` yang deskriptif, `loading="lazy"`, `allowfullscreen`, `referrerpolicy`, `width="100%"`, dan tinggi yang responsif bila memungkinkan.
7. Simpan dan unggah ulang file ke GitHub. Buka halaman live dan pastikan peta menampilkan pin yang benar.
8. Jika gaya gelap membuat warna peta sulit dibaca atau tidak cocok dengan embed terbaru, hapus class `map-dark` pada iframe. Kelas tersebut menerapkan filter CSS, bukan mengubah data peta.

### Catatan privasi dan akurasi

- Jangan menampilkan alamat publik jika bisnis tidak menerima pelanggan di lokasi tersebut; sesuaikan tampilan halaman dan pengaturan profil dengan model usaha sebenarnya.
- Koordinat JSON-LD di `index.html` masih merupakan referensi area Kelurahan Katangka, bukan hasil penentuan titik pintu/alamat usaha. Perbarui dengan koordinat pin yang telah diverifikasi.
- Alternatif peta yang memakai URL Google Maps Embed API dari Google Cloud memerlukan API key dan konfigurasi project yang benar. Untuk pemula, menu **Bagikan → Sematkan peta** biasanya lebih mudah.

---

## D. Pemetaan aset yang tersedia

| Tujuan | File lokal | Ukuran sumber |
|---|---|---:|
| Logo utama/footer | `assets/img/brand/logo-ai-technician87.png` | 512 × 512 px |
| Logo vector | `assets/img/brand/logo-ai-technician87.svg` | 600 × 600 viewBox |
| Favicon | `assets/icons/favicon.ico` | 48 × 48 px |
| Favicon kecil | `assets/icons/favicon-16.png`, `favicon-32.png` | 16 × 16, 32 × 32 px |
| Ikon aplikasi | `assets/icons/android-chrome-192.png`, `android-chrome-512.png` | 192 × 192, 512 × 512 px |
| Ikon iOS | `assets/icons/apple-touch-icon.png` | 180 × 180 px |
| Hero desktop | `assets/img/hero-cctv-desktop.webp` | 1920 × 1080 px |
| Hero mobile | `assets/img/hero-cctv-mobile.webp` | 900 × 1200 px |
| Panel hero | `assets/img/hero-panel.webp` | 448 × 560 px |
| Visual target pasar | `assets/img/business-cctv.webp` | 1200 × 800 px |
| Portofolio (4 foto) | `assets/img/portofolio/*.webp` | 1200 × 900 px masing-masing |
| Open Graph | `assets/img/og-image.jpg` | 1200 × 630 px |
| Twitter/X card | `assets/img/twitter-image.jpg` | 1200 × 630 px |

---

## E. Sumber resmi

- GitHub Pages — membuat situs: https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
- GitHub Pages — memilih sumber publikasi: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
- Google Business Profile — mengelola area layanan: https://support.google.com/business/answer/9157481?hl=id
- Google Business Profile — pedoman representasi bisnis: https://support.google.com/business/answer/3038177?hl=id
- Google Maps — sematkan peta: https://developers.google.com/maps/documentation/embed/embedding-map?hl=id
