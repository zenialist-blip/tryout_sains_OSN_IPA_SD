# Klub Sains Kecil — OSN IPA SD

**Revisi konseptual · 5 paket / 250 soal · 14 modul · 76 percobaan visual**

Website latihan sains yang berjalan langsung di browser. Bukan paket soal resmi OSN.

## Cara unggah ke GitHub Pages

**Pilihan A — Ganti website secara menyeluruh (disarankan)**

1. Unduh dan ekstrak ZIP ini.
2. Masuk ke repositori GitHub yang digunakan untuk GitHub Pages, misalnya `suhukalor-OSN-IPA-SD`.
3. Unggah file berikut **bersamaan** pada folder publikasi GitHub Pages yang sama, biasanya root repositori: `index.html`, `styles.css`, `data.js`, `models.js`, `app.js`. File `pembahasan.html` juga boleh diunggah untuk tautan pembahasan mandiri.
4. Pastikan GitHub Pages menggunakan branch/folder tersebut, kemudian buka alamat situs. Paksa muat ulang browser jika masih menampilkan versi lama (`Ctrl + F5` pada Windows).

**Pilihan B — Hanya ganti halaman pembahasan lama**

Unggah/replace **`pembahasan.html` saja**. File ini **mandiri**: CSS, data 250 soal, gambar 76 model, dan JavaScript sudah tergabung di dalamnya. Tidak perlu file JS/CSS lainnya. Cara ini tidak otomatis mengganti tampilan `index.html` lama.

**Pilihan C — Pratinjau tanpa internet**

Ekstrak ZIP lalu klik dua kali `pembahasan.html` pada Windows. Halaman mandiri berjalan lokal tanpa server atau internet.

> Jangan mengunggah ZIP apa adanya ke GitHub Pages tanpa mengekstraknya; unggah isi file di lokasi yang tepat. Semua path pada `index.html` bersifat relatif.

## Perubahan utama

- Mengganti laboratorium berbasis kalkulator generik dengan **76 model SVG tematik**. Setiap model memiliki proses/gambar sendiri, kontrol yang mengubah keadaan visual, pengamatan, pertanyaan pemantik, penalaran, dan penjelasan batas model.
- Contoh: gelombang transversal bergerak (amplitudo, frekuensi, panjang gelombang dan cepat rambat); tuas dan momen gaya; jumlah ruas katrol; cahaya, pembiasan, lensa dan gerhana; rangkaian listrik; kalor dan perubahan wujud; sel dan ekosistem; hingga filtrasi air, biogas dan DNA barcoding.
- **250 soal dari berkas sumber dipertahankan**, termasuk pilihan jawaban, kunci, pembahasan, petunjuk, dan langkah perhitungan yang tersedia. Tidak dibuat kunci baru.
- Pembahasan tertaut ke visual yang relevan. Jawaban, status sudah paham, dan progres disimpan pada browser/perangkat lokal.
- Desain lebih organik, ramah anak, responsif layar ponsel, tanpa akun, tanpa CDN, dan tanpa API.
- Alamat lama dengan akhiran `#s1` langsung membuka latihan paket 1. Tautan khusus nomor soal didukung dalam pola `#p1q1` sampai `#p5q50`.

## Catatan akurasi dan batasan

Visual adalah **model pendidikan yang disederhanakan**, bukan simulasi fisika numerik profesional. Setiap model menyatakan asumsi dan batasannya, misalnya gelombang ideal dengan sifat medium konstan, tuas tanpa gesekan, maupun diagram anatomi skematis. Model tidak menggantikan pengukuran lapangan atau praktik laboratorium nyata.

Kunci dan pembahasan berasal dari ZIP yang diberikan, sehingga bukan hasil pencocokan ulang dengan naskah soal resmi OSN.

## Berkas

- `index.html`: laman utama website (memerlukan empat aset berikut).
- `styles.css`: tampilan organik dan responsif.
- `data.js`: basis data asli 250 soal, materi, dan pembahasan.
- `models.js`: seluruh percobaan, konsep, asumsi, dan gambar SVG.
- `app.js`: navigasi, interaksi, penyimpanan progres, dan animasi.
- `pembahasan.html`: versi lengkap yang berdiri sendiri untuk unggah satu file.

## Uji fungsional

Diuji dengan Chromium/Playwright: semua 76 model menghasilkan output dan SVG valid pada keadaan awal serta variasi kontrol; 250 soal termuat; pembahasan, jawaban, perpindahan soal, filter materi, tampilan ponsel, dan navigasi diuji tanpa error JavaScript.
