---
title: GIT - SIMPLE GUIDE
---

> # <span style="color:indianred">Ini adalah pedoman *simple* untuk mulai menggunakan git</span>

> [Tweet this!](https://twitter.com/intent/tweet?hashtags=git&original_referer=http%3A%2F%2Frogerdudler.github.io%2Fgit-guide%2F&ref_src=twsrc%5Etfw&related=rogerdudler&text=git%20-%20the%20simple%20guide%20-%20no%20deep%20shit!&tw_p=tweetbutton&url=http%3A%2F%2Frogerdudler.github.com%2Fgit-guide&via=rogerdudler)
<!-- > # [gambar twitter](https://twitter.com/intent/tweet?hashtags=git&original_referer=http%3A%2F%2Frogerdudler.github.io%2Fgit-guide%2F&ref_src=twsrc%5Etfw&related=rogerdudler&text=git%20-%20the%20simple%20guide%20-%20no%20deep%20shit!&tw_p=tweetbutton&url=http%3A%2F%2Frogerdudler.github.com%2Fgit-guide&via=rogerdudler) -->

<!-- > ![Gambar twitter](../../themes/landscape/source/css/images/twitter-logo-new.png)
> ![Gambar twitter](https://s-media-cache-ak0.pinimg.com/originals/24/be/d6/24bed6462dfe28198b199db07a976425.jpg)
> ![Gambar twitter](/images/twitter-logo-new.PNG) -->

<!-- [![](https://scontent-sit4-1.xx.fbcdn.net/v/t1.0-9/28684846_343968986104489_8822289537515262514_n.jpg?oh=6b66c7b3c33bd652193c5a02d8ecc91e&oe=5B3A6236)](https://twitter.com/intent/tweet?hashtags=git&original_referer=http%3A%2F%2Frogerdudler.github.io%2Fgit-guide%2F&ref_src=twsrc%5Etfw&related=rogerdudler&text=git%20-%20the%20simple%20guide%20-%20no%20deep%20shit!&tw_p=tweetbutton&url=http%3A%2F%2Frogerdudler.github.com%2Fgit-guide&via=rogerdudler) -->

> *original by* [Roger Dudler](https://twitter.com/rogerdudler)
> *translate by* [Azhar Khaira](https://twitter.com/azharkhairaa)
> ![](https://scontent.fcgk6-1.fna.fbcdn.net/v/t1.0-9/28783249_343968619437859_839653962830437140_n.jpg?oh=14040b6d47c4681d46dbdec51058f23f&oe=5B46CC72)

> ## <span style="color:indianred">Setup</span>
> [=bungkusPad== Download git untuk OSX ==](https://git-scm.com/download/mac)
> [=bungkusPad== Download git untuk Windows ==](https://gitforwindows.org/)
> [=bungkusPad== Download git untuk Linux ==](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

> ## <span style="color:indianred">Membuat repositori baru</span>
> buat direktori baru, buka, dan lakukan
> **`git init`**
> untuk membuat *repository git* baru.

> ## <span style="color:indianred">Memeriksa repositori</span>
> buat salinan pekerjaan dari *local repository* dengan menjalankan perintah
> **`git clone /path/to/repository`**
> ketika menggunakan server jarak jauh, isi perintahnya akan menjadi
> **`git clone username@host:/path/to/repository`**

> ## <span style="color:indianred">Alur kerja</span>
> Repositori lokal kamu terdiri dari tiga bagian dengan sebutan "*trees*"
> yang dikelola oleh git. Yang pertama adalah `*Working Directory*`
> yang menyimpan berkas aktual. Kedua adalah `*Index*` yang
> berperan sebagai pengolah data dan yang ketiga `*Head*`
> yang mengarah pada komit terakhir.
> ![](https://scontent.fcgk6-1.fna.fbcdn.net/v/t1.0-9/28870206_343968629437858_747611564763456957_n.jpg?oh=56f254f78417d65536d9b1e69afcc6c2&oe=5B0473EF)

> ## <span style="color:indianred">Tambah dan komit</span>
> Kamu bisa melakukan perubahan (penambahan ke ***index***) menggunakan
> **`git add <filename>`**
> **`git add *`**
> ini merupakan langkah awal alur kerja dasar git.
> Untuk komit sepenuhnya gunakan
> **`git commit -m "commit message"`**
> Sekarang berkas sudah berkomit di *head*,
> tapi belum di repositori jarak jauh.

> ## <span style="color:indianred">Mengirim perubahan</span>
> Saat ini perubahan sudah tersimpan di *head* salinan kerja lokal kamu.
> Untuk mengirimkan ke repositori jarak jauh, lakukan
> **`git push origin master`**
> Ubah *master* sesuai dengan cabang yang kamu inginkan.
> 
> Jika repositori yang ada belum dikloning dan ingin dihubungkan
> ke server jarak jauh, kamu perlu menambahkan
> **`git remote add origin <server>`**
> Sekarang kamu bisa mengirimkan perubahan ke server jarak jauh yang dituju.

> ## <span style="color:indianred">Percabangan</span>
> Percabangan atau *branching* digunakan untuk mengembangkan
> fitur-fitur secara terisolasi. Cabang utama atau *master* merupakan
> cabang bawaan ketika kamu membuat repositori. Gunakan cabang lain 
> untuk pengembangan, setelah selesai, gabungkan kembali ke cabang utama.
> ![](https://scontent.fcgk6-1.fna.fbcdn.net/v/t1.0-9/28795128_343968622771192_4812218289283676283_n.jpg?oh=ac7c1d657d6ceaf2bfcf8bee288ef602&oe=5B4CF3B3)
> buat cabang baru dengan nama "fitur_x" dan beralih kedalamnya menggunakan
> **`git checkout -b fitur_x`**
> beralih kembali ke *master*
> **`git checkout master`**
> dan hapus cabang yang tadi dibuat
> **`git branch -d fitur_x`**
> suatu cabang **tidak terbuka untuk yang lainnya** kecuali
> jika kamu mengirimkannya ke repositori jarak-jauh.
> **`git push origin <cabang>`**

> ## <span style="color:indianred">Perbaruan dan penggabungan</span>
> Untuk memperbarui repositori lokal ke komit terkini, lakukan
> **`git pull`**
> dari direktori kerja kamu untuk 
> **mengambil** dan **menggabungkan** perubahan jarak-jauh.
> Untuk menggabungkan cabang lain ke cabang aktif (misal *master*), gunakan
> **`git merge <cabang>`**
> pada kasus diatas, git mencoba menggabungkan perubahan secara
> otomatis. Sayangnya hal ini tak selalu berjalan mulus dan bisa
> menyebabkan **konflik**. Kamu lah yang bertanggung jawab
> menggabungkan **konflik** tersebut secara manual dengan menyunting
> berkas yang ditunjukkan git. Setelah itu, kamu perlu menandainya dengan
> **`git add <filename>`**
> sebelum penggabungan berlaku, kamu bisa melakukan pratinjau menggunakan
> **`git diff <cabang_asal> <cabang_tujuan>`**

> ## <span style="color:indianred">Penandaan</span>
> Sangat dianjurkan membuat penanda atau *tags* untuk perangkat lunak
> yang dirilis. Hal ini amat lah lazim, yang juga terjadi di SVN. Kamu bisa
> membuat penanda baru dengan nama *1.0.0* dengan menjalankan
> **`git tag 1.0.0 1b2e1d63ff`**
> *1b2e1d63ff* adalah 10 karakter pertama dari identitas komit yang ingin
> kamu referensikan ke penanda. Kamu bisa mendapatkan identitas 
> komit dengan melihat ***LOG***

> ## <span style="color:indianred">Log</span>
> Dalam bentuknya yang paling sederhana, kamu bisa mempelajari
> riwayat repositori menggunakan
> **`git log`**
> kamu bisa menambahkan banyak parameter untuk menampilkan log 
> sesuai keinginan. Untuk melihat komit penulis tertentu:
> **`git log --author=bob`**
> Untuk melihat log yang dimampatkan, satu baris per komit:
> **`git log --pretty=oneline`**
> Atau mungkin kamu ingin melihat pohon *ASCII art* seluruh
> percabangan disertai nama dan penandanya:
> **`git log --graph --oneline --decorate --all`**
> Sekedar melihat berkas yang berubah:
> **`git log --name-status`**
> Ini baru sedikit saja dari sekian banyak parameter yang bisa kamu 
> gunakan. Lebih jauh lagi, lihat
> **`git log --help`**

> ## <span style="color:indianred">Mengembalikan perubahan lokal</span>
> Seandainya kamu melakukan kesalahan, kamu bisa
> mengembalikannya menggunakan perintah
> **`git checkout -- <namaberkas>`**
> perintah di atas mengembalikan perubahan di dalam pokok kerja kamu
> dengan konten terakhir dari *HEAD*. Perubahan dan berkas baru yang
> telah ditambahkan ke indeks akan tetap tersimpan.
> 
> Jika kamu ingin membatalkan perubahan dan komit lokal seutuhnya,
> ambil riwayat terakhir dari server dan arahkan ke cabang master lokal
> seperti ini
> **`git fetch origin`**
> **`git reset --hard origin/master`**

> ## <span style="color:indianred">Petunjuk berguna</span>
> GUI git bawaan
> **`gitk`**
> menggunakan output git penuh warna
> **`git config color.ui true`**
> menunjukkan log satu baris per komit
> **`git config format.pretty oneline`**
> menggunakan penambahan interaktif
> **`git add -i`**

> ## <span style="color:indianred">Tautan & sumber</span>
> #### Klien grafis
> [GitX (L) (OSX, sumber terbuka)](http://gitx.laullon.com/)
> [Tower (OSX)](https://www.git-tower.com/)
> [Source Tree (OSX & Windows, gratis)](https://www.sourcetreeapp.com/)
> [GitHub for Mac (OSX, gratis)](https://desktop.github.com/)
> [GitBox (OSX, App Store)](https://itunes.apple.com/gb/app/gitbox/id403388357?mt=12)
> [GitBox (OSX, App Store)](https://itunes.apple.com/gb/app/gitbox/id403388357?mt=12)
>
> #### Panduan
> [Buku Komunitas Git](https://git-scm.com/book/id/v2)
> [Git Pro](https://progit.org/book/)
> [Berfikir seperti git](http://think-like-a-git.net/)
> [Bantuan GitHub](https://help.github.com/)
> [Panduan Git Visual](http://marklodato.github.io/visual-git-guide/index-en.html)
> [Panduan Git Visual](http://marklodato.github.io/visual-git-guide/index-en.html)
> 
> #### Bantuan
> [Milis Pengguna Git](https://groups.google.com/forum/#!forum/git-users)
> [#git di irc.freenode.net](https://gitirc.eu/)
