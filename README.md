# Happy Birthday, Ezza 🌸

Website ucapan ulang tahun interaktif, tema merah bernuansa anime, dengan landing page kelopak bunga sebelum masuk ke halaman utama.

## Struktur folder

```
ezza-birthday-site/
├── index.html          ← halaman utama
├── css/
│   └── style.css        ← semua styling
├── js/
│   └── script.js         ← semua interaksi + isi teks (CONFIG)
├── images/               ← foto-foto yang dipakai
└── audio/
    └── backsound.mp3     ← taruh lagu pilihan kamu di sini (belum ada filenya)
```

## Cara nambahin lagu backsound

1. Siapkan file lagu dalam format `.mp3` (usahakan ukurannya gak terlalu besar, di bawah 8–10MB supaya loading-nya cepat).
2. Rename file itu jadi `backsound.mp3`.
3. Taruh di folder `audio/`, gantikan file placeholder yang ada di situ.
4. Musik akan otomatis coba diputar begitu tombol "Buka Undangan" di landing page diklik (browser butuh interaksi klik dulu baru boleh autoplay audio). Ada juga tombol 🔇/🔊 kecil di pojok kanan bawah buat mute/unmute manual.

> Pastikan kamu punya hak pakai/lisensi buat lagu yang dipasang, apalagi kalau situsnya bakal dibagikan publik.

## Cara ganti teks/isi konten

Semua teks (ucapan, alasan sayang, pujian, quiz, dll) ada di bagian atas file `js/script.js`, di dalam object `CONFIG`. Tinggal edit teksnya di situ, gak perlu sentuh bagian lain.

## Cara ganti foto

Ganti file di folder `images/` dengan foto kamu sendiri (nama file harus sama persis, atau update juga path-nya di `index.html` / `js/script.js`).

## Deploy ke GitHub Pages

1. Buat repository baru di GitHub (public atau private, keduanya bisa dipakai di GitHub Pages — kalau private butuh GitHub Pro).
2. Upload semua isi folder ini (bukan foldernya, tapi isinya) ke root repository:
   ```bash
   git init
   git add .
   git commit -m "Happy birthday website"
   git branch -M main
   git remote add origin https://github.com/USERNAME/NAMA-REPO.git
   git push -u origin main
   ```
3. Di repository GitHub, buka **Settings → Pages**.
4. Di bagian **Source**, pilih branch `main` dan folder `/ (root)`, lalu **Save**.
5. Tunggu 1–2 menit, situsnya akan aktif di:
   `https://USERNAME.github.io/NAMA-REPO/`

## Catatan

- Semua fitur (kuis, undian pesan, form harapan, dll) jalan sepenuhnya di browser (client-side) — gak butuh server atau database, jadi aman buat GitHub Pages yang sifatnya static hosting.
- Data yang diisi di form "tulis harapan" cuma tersimpan sementara di halaman (gak persisten), karena situs static ini tidak terhubung ke database apapun.
