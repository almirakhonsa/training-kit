---
layout: cheat-sheet
title: Buku Saku Git GitHub
byline: Git adalah sistem manajemen revisi terdistribusi bersifat terbuka yang menyediakan aktivitas GitHub di laptop atau komputer pribadi Anda. Buku saku ini meringkas baris instruksi-instruksi Git yang paling sering dipakai sebagai referensi singkat.
leadingpath: ../
---

{% capture colOne %}
## Pasang Git
GitHub menyediakan klien bagi komputer, termasuk di dalamnya ada antarmuka grafis untuk tindakan repositori yang paling umum dilakukan dan tampilan konsol tempat menuliskan baris perintah untuk melaksanakan tindakan lebih lanjut.

### GitHub untuk Windows
http://windows.github.com

### GitHub untuk Mac
http://mac.github.com

Distribusi Git untuk Linux dan sistem POSIX tersedia di situs resmi Git SCM.

### Git untuk semua media
https://git-scm.com

## Konfigurasi alat
Konfigurasi informasi pengguna untuk semua repositori lokal

```$ git config --global user.name "[nama]"```

Menetapkan nama yang ditautkan dalam pencatatan _commit_ Anda

```$ git config --global user.email "[alamat surel]"```

Menata alamat surel yang ditautkan dalam pencatatan _commit_ Anda

## Buat repositori
Memulai repositori baru atau mengambil dari tautan yang sudah ada

```$ git init [nama-proyek]```

Membuat repositori lokal dengan nama tertentu

```$ git clone [url]```

Unduh sebuah proyek dan seluruh riwayat revisinya
{% endcapture %}
<div class="col-md-6">
{{ colOne | markdownify }}
</div>


{% capture colTwo %}

## Buat perubahan
Tinjau suntingan dan daftarkan _commit_

```$ git status```

Daftar semua berkas yang baru dibuat atau telah dimodifikasi akan didaftarkan dalam bentuk _commit_

```$ git diff```

Menunjukkan perbedaan berkas-berkas yang belum didaftarkan dalam _commit_

```$ git add [berkas]```

Rekam berkas untuk didaftarkan ke dalam _commit_

```$ git diff --staged```

Menunjukkan perbedaan berkas antara hasil revisi dengan versi berkas terakhir yang terdaftar

```$ git reset [berkas]```

Batal merevisi berkas, namun tetap mempertahankan isinya

```$ git commit -m "[descriptive message]"```

Daftarkan perubahan berkas secara permanen di riwayat revisi

## Perubahan untuk banyak berkas
Beri nama serangkaian _commit_ dan gabungkan upaya pengubahan menjadi satu

```$ git branch```

Daftar semua cabang lokal di repositori saat ini

```$ git branch [nama-cabang]```

Buat cabang baru

```$ git checkout [nama-cabang]```

Berpindah ke cabang tertentu dan perbarui direktori yang sedang dikerjakan

```$ git merge [nama-cabang]```

Menggabungkan riwayat cabang tertentu ke dalam cabang yang sedang digunakan

```$ git branch -d [nama-cabang]```

Hapus cabang tertentu
{% endcapture %}
<div class="col-md-6">
{{ colTwo | markdownify }}
</div>
<div class="clearfix"></div>


{% capture colThree %}

## Pergantian nama berkas
Relokasi dan menghapus berkas revisi

```$ git rm [berkas]```

Menghapus berkas dari direktori kerja dan daftarkan penghapusan

```$ git rm --cached [berkas]```

Menghapus berkas dari riwayat revisi dengan tetap mempertahankan berkas lokal

```$ git mv [berkas-asli] [berkas-baru]```

Mengganti nama berkas dan menyiapkan berkas untuk pendaftaran _commit_

## Tahan pelacakan
Mengabaikan berkas dan jalur untuk sementara

```
*.log
build/
temp-*
```

Sebuah berkas teks bernama `.gitignore` mengabaikan revisi berkas yang tidak disengaja serta jalur berkas yang cocok dengan pola tertentu

```$ git ls-files --others --ignored --exclude-standard```

Daftarkan semua berkas yang diabaikan dalam proyek ini

## Simpan fragmen
Menyimpan dan mengembalikan perubahan yang belum lengkap

```$ git stash```

Menyimpan semua perubahan berkas yang terlacak untuk sementara

```$ git stash pop```

Mengembalikan berkas yang paling baru disimpan

```$ git stash list```

Daftar semua koleksi perubahan yang tersimpan

```$ git stash drop```

Membuang koleksi perubahan yang paling baru disimpan
{% endcapture %}
<div class="col-md-6">
{{ colThree | markdownify }}
</div>


{% capture colFour %}

## Riwayat ulasan
Jelajah dan periksa perkembangan berkas-berkas dalam proyek

```$ git log```

Daftar riwayat revisi untuk cabang saat ini

```$ git log --follow [berkas]```

Daftar riwayat revisi untuk sebuah berkas, termasuk pergantian namanya

```$ git diff [cabang-pertama]...[cabang-kedua]```

Menunjukkan perbedaan konten diantara dua cabang

`` `$ git show [commit]` ``

Menampilkan perubahan isi dan metadata yang terdaftar dalam sebuah _commit_

## Lakukan _commit_ kembali
Menghapus kesalahan dan buat riwayat penggantian

`` `$ git reset [commit]` ``

Membatalkan semua _commit_ setelah `[commit]`, dengan menerapkankan perubahan lokal

`` `$ Git reset --hard [commit]` ``

Membuang semua riwayat dan perubahan sampai pada titik yang telah ditentukan oleh _commit_

## Sinkronisasi perubahan
Daftar (tautan) remot dan perbarui riwayat repositori

```$ git fetch [remot]```

Unduh semua riwayat dari repositori remot

```$ git merge [remot]/[cabang]```

Menggabungkan cabang remot ke dalam cabang lokal saat ini

```$ git push [remote] [branch]```

Unggah semua _commit_ dari cabang lokal ke GitHub

```$ git pull```

Unduh riwayat marka dan gabungkan perubahan
{% endcapture %}
<div class="col-md-6">
{{ colFour | markdownify }}
</div>
