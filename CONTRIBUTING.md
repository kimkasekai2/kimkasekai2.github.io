# Panduan Kontribusi

Terima kasih kepada semua pengembang yang telah berkontribusi bagi proyek ini, serta atas dukungan dari kalian semua!

Jika Anda menyukai proyek ini, silakan berikan sebuah Star untuk proyek ini, sponsor kami, atau lakukan kontribusi penting bagi kami qwq~

## Laporan Bug

1. Gunakan versi terbaru untuk memastikan bug tersebut belum diperbaiki.

2. Pastikan bug atau kesalahan tersebut bukan berasal dari masalah pada pihak Anda sendiri. Misalnya, menggunakan browser yang cukup usang (seperti IE), atau menonaktifkan sebagian fitur browser (seperti melarang penyimpanan data)

3. Jelaskan bug dengan jelas agar kami dapat memperbaikinya dengan lebih baik.

4. Anda dapat menggunakan templat Issue "Laporan Bug" untuk memberi masukan, tetapi mohon isi kontennya dengan benar.

5. Dilarang menambahkan konten apa pun yang melanggar hukum atau sensitif secara politis ke dalam isinya; jika terjadi, akan diambil tindakan penguncian + pemblokiran sesuai situasi.

## Usulan Fitur

1. Gunakan versi terbaru untuk memastikan saran tersebut belum diimplementasikan/diselesaikan.

2. Jelaskan saran tersebut dengan jelas agar kami dapat mengimplementasikan/menyelesaikannya dengan lebih baik.

3. Anda dapat menggunakan templat Issue "Usulan Fitur" untuk memberi masukan, tetapi mohon isi kontennya dengan benar.

4. Dilarang menambahkan konten apa pun yang melanggar hukum atau sensitif secara politis ke dalam isinya; jika terjadi, akan diambil tindakan penguncian + pemblokiran sesuai situasi.

## Mengirimkan Kode

Catatan: Harap ikuti secara ketat ketentuan di bawah ini serta standar pengembangan di awal desktop.html saat menyunting kode, jika tidak maka tidak akan digabungkan

1. Usahakan mengirimkan seluruh isi dalam satu Commit sekaligus. Commits tambahan diperbolehkan, tetapi usahakan tidak melebihi 5 Commits.

2. Usahakan menggunakan baris perintah Git, GitHub Desktop, [https://github.dev](https://github.dev/tjy-gitnub/win12) dan semacamnya untuk melakukan submit. Mohon jangan langsung mengunggah file melalui browser untuk submit.

3. Dilarang mengunggah konten apa pun yang melanggar hukum atau sensitif secara politis; jika terjadi, akan diambil tindakan penguncian + pemblokiran sesuai situasi (Catatan: berita aktual pun tidak boleh).

4. Saat submit, mohon jangan asal menentukan judul maupun isi commit, misalnya:

   - Contoh yang baik: Memperbaiki masalah xx yang tidak dapat digunakan, Menambahkan aplikasi xx
   
   - Contoh yang buruk: blablabla, benda ini kelupaan, bug-nya kebanyakan... qwq

5. Persyaratan format:

   - Mohon jangan menggunakan alat formatter untuk memformat file HTML

   - Untuk file JavaScript dan CSS, boleh menggunakan alat formatter bawaan Visual Studio Code

### Persyaratan Pesan Commit

   1. Jika pembaruan cukup penting atau berukuran besar, ikutilah format berikut:

      ```
      v11.4.5 - memperbarui xxx

      (Pembaruan dari @Somebody)
      - memperbarui...
      - mengoptimalkan...
      - memperbaiki...
      ...
      ```

      - Persyaratan penggunaan format ini:

         1. Anda wajib memberi tahu kami sebelum melakukan submit pembaruan ini.

      - Penjelasan:

         1. Judul harus memuat nomor versi serta isi utama pembaruan.

         2. Baris pertama isi harus mencantumkan sumber pembaruan.

         3. Isi harus menjelaskan apa saja yang diperbarui dalam bentuk daftar.

      - Perhatian:

         1. Mohon jangan memilih nomor versi sembarangan. Jika Anda kurang jelas, silakan hubungi kami melalui grup diskusi kami (<https://teams.live.com/l/invite/FEA0yrNkE_bAn-ddwI>) untuk mendapat penetapan nomor versi.

         2. Saat memperbarui, ingatlah untuk menambahkan konten terkait pembaruan ini ke dalam riwayat pembaruan aplikasi "Tentang Windows 12 Versi Web".

   2. Jika kondisi-kondisi berikut terpenuhi, isi commit tidak diatur terlalu standar:

      - Isi pembaruan sedikit.

      - Isi pembaruan tidak mengandung perubahan penting.

      Meskipun tidak ada aturan standar, Anda tetap perlu:

         1. Menyusun judul commit yang jelas dan singkat, mampu meringkas inti utama pembaruan.

         2. Mencantumkan siapa pengirim commit pada isinya, serta menjelaskan isi pembaruan kali ini dalam bentuk daftar atau cara lain.

### Standar Pengembangan

1. Ketentuan untuk file HTML

   1. Ketentuan atribut id: kecuali benar-benar diperlukan, usahakan jangan menggunakan atribut id agar tidak terjadi konflik, gunakan class sebagai gantinya. Jika memang harus digunakan, ingatlah beberapa hal berikut:

      1. Kecuali untuk node body>*, mohon jangan menggunakan nama id yang terdiri dari satu kata

      2. Nama yang dipilih harus bermakna

      3. Untuk node selain body>*, berilah nama dengan pola "kata-kunci-elemen-induk-(...)-nama-id". Misalnya: taskmgr-search, setting-search, dll.

   2. Ketentuan atribut class:

      1. Nama yang dipilih harus bermakna

      2. Tidak perlu memberi class pada setiap elemen, cukup sesuai kebutuhan

      3. Saat menggunakan selector css, pastikan elemen yang dipilih berada dalam cakupan yang diharapkan, artinya menargetkan elemen secara tepat agar tidak salah mencocokkan elemen lain

   3. Ketentuan gaya kode:

      1. Untuk gambar svg, usahakan dimampatkan menjadi satu baris atau diekstrak ke file terpisah agar tidak terlalu membengkak

      2. Untuk kode yang tidak perlu ditulis terurai, usahakan dimampatkan menjadi satu baris

2. Ketentuan untuk file JS

   1. Kembangkan kode dengan mengikuti gaya berikut:

   ```js
      var sum = 0;
      for (var i = 0; i < 10; i++) {
         sum += i;
      }
      console.log(sum);
   ```

   2. Untuk penamaan fungsi dan variabel, gunakan camelCase, misalnya:

      - isLoaded

      - storagedItems

   3. Untuk penamaan kelas, gunakan PascalCase (camelCase huruf besar), misalnya:

      - WindowManager

      - Widgets

   4. Ketentuan gaya kode:

      1. Untuk kode yang tidak perlu ditulis terurai, usahakan dimampatkan menjadi satu baris

## Mengirimkan Berita

1. Pastikan berita yang Anda kirimkan **sama sekali tidak ada yang muncul di kehidupan nyata saat ini ataupun masa lampau**, artinya murni fiksi.

2. Dilarang mengunggah konten apa pun yang melanggar hukum atau sensitif secara politis; jika terjadi, akan diambil tindakan penguncian + pemblokiran sesuai situasi (Catatan: berita aktual pun tidak boleh).
