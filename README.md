# 1. Eksekusi seluruh profile yang ada :  
## a.  Edit file profile /etc/profile dan tampilkan pesan sebagai berikut :  
       echo “Profile dari /etc/profile”

![jwbn1a](https://github.com/user-attachments/assets/dfcfce9d-a8ed-4508-9244-cd760874d5b3)
![isi file jwbn1a](https://github.com/user-attachments/assets/103c7947-b1db-41f5-9b1f-d3ae905d9ad1)
- /etc/profile : Berisi shell script yang berlaku untuk seluruh pengguna Linux. 

## b.  Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu :  
       /home/stD02001/.bash_profile  
       /home/. stD02001/.bash_login  
       /home/mahasiswa/.profile  
       /home/mahasiswa/.bashrc  
## Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap  file tersebut, cantumkan instruksi echo, misalnya pada /home/ mahasiswa/.bash_profile :  
       echo “Profile dari .bash_profile”  
## Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yang bersangkutan. 
![jwbn1b1](https://github.com/user-attachments/assets/bf60b280-80e7-41bf-a425-a711a8bcf2be)
![isi file jwbn1b1](https://github.com/user-attachments/assets/32d5917f-61ef-4221-94cf-d0be7f9da58b)
![jwbn1b2](https://github.com/user-attachments/assets/4cdc58a3-eb08-4f7a-80d2-9db2e2c346c3)
![isi file jwbn1b2](https://github.com/user-attachments/assets/4d89d4e2-4b13-4f0e-8262-c9cf117605e4)
![jwbn1b3](https://github.com/user-attachments/assets/3c152065-1c6a-4891-a41a-50d2faa63554)
![isi file jwbn1b3](https://github.com/user-attachments/assets/23c59dcb-9298-4f91-863d-491e88870bb6)
![jwbn1b4](https://github.com/user-attachments/assets/6990a686-c557-42e2-b3ad-592ef8c67d62)
![isi file jwbn1b4](https://github.com/user-attachments/assets/d1ab96da-88e3-4f67-87db-972130bd63eb)

## c.  Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut: 
       $ su mahasiswa  
       $ exit  
## kemudian gunakan opsi – sebagai berikut :  
       $ su – mahasiswa  
       $ exit  
## Jelaskan perbedaan kedua utilitas tersebut. 
![jwbn1c1](https://github.com/user-attachments/assets/93c9dcfe-ced7-4b8b-a5de-7fa5b31fcb6b)
![jwbn1c2](https://github.com/user-attachments/assets/4ba27dd7-a4e7-432e-825e-46297fc8c397)
- su (Switch User):
  - Mengganti pengguna tanpa memuat environment atau profile pengguna baru.
  - Direktori kerja tetap sama seperti pengguna sebelumnya.
  - Tidak mengeksekusi file profile seperti .bash_profile atau .bashrc dari pengguna baru.
- su - (Switch User with Login Shell):
  - Mengganti pengguna dan memuat lingkungan sepenuhnya seperti saat login.
  - Menjalankan file profile dari pengguna baru, seperti /etc/profile, .bash_profile, .bashrc, dan lain-lain.
  - Mengganti direktori kerja ke direktori home pengguna baru.

# 2. Prompt String (PS)  
## a. Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell  
      PS1=‟> „  
      export PS1 
![jwbn2a](https://github.com/user-attachments/assets/c98e92e8-d623-4719-a32a-4a7777a0e1aa)

## b.  Eksperimen hasil PS1 : 
       $ PS1=“\! > “  
       69 > PS1=”\d > “  
       Mon Sep 23 > PS1=”\t > “  
       10:10:20 > PS1=”Saya=\u > “  
       Saya=mahasiswa > PS1=”\w >”  
       ~ > PS1=\h >” 
![jwbn2b](https://github.com/user-attachments/assets/17d54005-ab82-45db-bafc-89be8c3f121a)
- PS1="\! > "      : Menampilkan nomor urutan perintah
- PS1="\d > "      : Menampilkan tanggal
- PS1="\t > "      : Menampilkan waktu (jam, menit, detik)
- PS1="Saya=\u > " : Menampilkan username
- PS1="\w > "      : Menampilkan current working directory (cwd)
- PS1="\h > "      : Menampilkan hostname

# 3. Logout  
## Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout  
       Echo “Terima kasih atas sesi yang diberikan”  
       Sleep 5  
       clear 
![jwbn3](https://github.com/user-attachments/assets/96073d85-346a-4b83-9311-baa8f630a5e6)
![isi file jwbn3](https://github.com/user-attachments/assets/4cf767cb-6fe1-4406-ae51-e149903d096d)

Setelah mengedit di file .bash_logout dan menyimpan nya. nanti semua terminal terhapus semuanya.

# 4. Bash script  
## a.  Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing :  
       p1.sh  
       #! /bin/bash  
       echo “Program p1”  
       ls –l  
       p2.sh  
       #! /bin/bash  
       echo “Program p2”  
       who  
       p3.sh  
       #! /bin/bash  
       echo “Program p3”  
       ps x
![jwbn4a](https://github.com/user-attachments/assets/40c73d03-b857-40db-baf5-3e9245c864be)
![isi file jwbn4a1](https://github.com/user-attachments/assets/25c373da-116c-4f92-bb11-bde4459b32de)
![isi file jwbn4a2](https://github.com/user-attachments/assets/e57536c9-d7ee-4a90-a4ed-9580a90378d6)
![isi file jwbn4a3](https://github.com/user-attachments/assets/a98b810f-a8ad-4556-99e0-747dda804969)

## b.  Jalankan script tersebut sebagai berikut :  
       $  ./p1.sh ; ./p3.sh ; ./p2.sh  
       $  ./p1.sh &  
       $  ./p1.sh $ ./p2.sh & ./p3.sh &  
       $  ( ./p1.sh ; ./p3.sh ) &  
![jwbn4b1](https://github.com/user-attachments/assets/039c905b-d8ed-45b7-9464-168a772a1224)
![jwbn4b1 1](https://github.com/user-attachments/assets/6448e02d-2624-47eb-9169-ab08a7ae4803)
- $ ./p1.sh ; ./p3.sh ; ./p2.sh
  - Perintah ini akan menjalankan p1.sh, setelah selesai baru menjalankan p3.sh, dan setelah itu baru menjalankan p2.sh.
  - Tanda titik koma (;) memastikan setiap perintah dieksekusi secara berurutan, yaitu script berikutnya baru akan dijalankan setelah script sebelumnya selesai.
    
![jwbn4b2](https://github.com/user-attachments/assets/5a12b7ee-20f3-4f0e-8729-91e3cf9ba137)
- $ ./p1.sh &
  - Perintah ini akan menjalankan p1.sh di background.
  - Tanda ampersand (&) menandakan bahwa perintah tersebut berjalan di background, sehingga kamu bisa menjalankan perintah lain sambil menunggu script selesai.
    
![jwbn4b3](https://github.com/user-attachments/assets/5b434226-5e77-4197-a3d7-0aabf879327f)
- $ ./p1.sh & ./p2.sh & ./p3.sh &
  - Ini akan menjalankan p1.sh, p2.sh, dan p3.sh secara bersamaan di background.
  - Masing-masing script tidak saling menunggu, sehingga mereka berjalan secara paralel.
    
![jwbn4b4](https://github.com/user-attachments/assets/527cd740-3288-4d54-a9bd-a1a53bd3b3ca)
- $ ( ./p1.sh ; ./p3.sh ) &
  - Perintah ini akan menjalankan p1.sh dan p3.sh secara berurutan, tetapi grup perintah ini dijalankan di background.
  - Penggunaan tanda kurung (()) mengelompokkan p1.sh dan p3.sh sebagai satu kesatuan. Script p1.sh akan dieksekusi terlebih dahulu, dan setelah selesai, p3.sh akan dijalankan, namun keseluruhan proses dijalankan di background karena ada tanda ampersand (&).
    
# 5. Jobs  
## a. Buat shell-script yang melakukan loop dengan nama pwaktu.sh,  setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil. 
       #!/bin/bash  
       while [ true ]  
       do  
       date >> hasil  
       sleep 10  
       done  
![jwbn5a](https://github.com/user-attachments/assets/1a754920-0be6-46a0-90b3-85e0553e73de)
![isi file jwbn5a](https://github.com/user-attachments/assets/c450d3be-5a83-447d-b174-094f89397f56)
- ./pwaktu.sh : Script ini akan mulai menambahkan tanggal dan waktu ke file hasil setiap 10 detik

## b.  Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di background sebagai berikut :  
       $ jobs  
       $ find / -print > files 2>/dev/null &  
       $ jobs  
![jwbn5b](https://github.com/user-attachments/assets/ffce21ea-297c-4f75-92b4-7ae614bbfeb2)
- find / -print > files 2>/dev/null &
  - find / -print > files: Mencari dan mencetak semua file mulai dari root /, kemudian mengarahkan output ke file bernama files.
  - 2>/dev/null: Mengarahkan pesan error (jika ada) ke /dev/null untuk menyembunyikannya.
  - &: Menjalankan perintah ini di background.
- jobs
  - Menampilkan daftar semua pekerjaan yang sedang berjalan di background

## c. Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut ke background  
       $ fg %1  
       $ bg 
![jwbn5c](https://github.com/user-attachments/assets/6efee02b-a988-43a9-bdf9-b77fd7f79479)
- fg : untuk memindahkan pekerjaan pertama (%1) dari background ke foreground.
- Ctrl+Z : untuk menghentikannya sementara (suspend). Proses ini akan berpindah ke status stopped di background.
- bg : menjalankannya kembali di background dengan perintah

## d.  Stop program background dengan utilitas kil  
       $ ps x  
       $ kill [Nomor PID]  
![jwbn5d](https://github.com/user-attachments/assets/7c504059-c015-4d5b-80c4-c7079cddde4a)
![jwbn5d1](https://github.com/user-attachments/assets/fa47266c-e0df-4ebc-8736-2cc711cd02ad)
![jwbn5d2](https://github.com/user-attachments/assets/ae7afeec-84e9-4ed3-8154-69e3432531e0)
- ps x : Untuk melihat daftar proses beserta nomor PID (Process ID).
- kill : menghentikan program yang ingin di hentikan.

# 6. History  
## a. Ganti nilai HISTSIZE dari 1000 menjadi 20  
       $ HISTSIZE=20  
       $ h 
![jwbn6a](https://github.com/user-attachments/assets/ac06d5d7-094f-479d-be86-43352221bde7)
- HISTSIZE adalah variabel yang menentukan jumlah baris history yang disimpan di memori selama sesi shell saat ini.
- HISTSIZE=20 : akan membatasi jumlah perintah yang disimpan dalam history menjadi 20.

## b. Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir dilakukan  
       $ !-5 
![jwbn6b](https://github.com/user-attachments/assets/32f759d1-736d-487b-b26c-4ca98b05c8ae)

!-5 : Mengeksekusi kembali perintah yang dilakukan 5 instruksi sebelumnya.

## c. Ulangi instruksi yang terakhir.  Gunakan juga ^P dan ^N untuk bernavigasi pada history bufer  
       $ !!  
![jwbn6c](https://github.com/user-attachments/assets/d5a10508-bc02-459b-b639-982ca01fa8f4)
- !! : Menjalankan perintah terakhir di history.

## d.  Ulangi instruksi pada history bufer nomor 150  
       $ !150 
![jwbn6d](https://github.com/user-attachments/assets/bd81a196-22c3-4427-827a-f0056d9b7773)
!150 : Menjalankan perintah yang tercatat pada nomor 150 di history.

## e.  Ulangi instruksi dengan prefix “ls”  
       $ !ls 
![jwbn6e](https://github.com/user-attachments/assets/4a137958-e9f7-45b5-a584-9f2a13c905d9)
- !ls : Untuk mengulangi perintah terbaru yang dimulai dengan ls.
