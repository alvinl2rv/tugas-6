# tugas-6
VI. Tugas

1. Eksekusi seluruh profile yang ada:
a. Edit file /etc/profile dan tampilkan pesan sebagai berikut:
echo "Profile dari /etc/profile"
<img width="1280" height="800" alt="t5 5 1 2" src="https://github.com/user-attachments/assets/c0168ad6-a117-4ef8-914e-144ef4dc23f1" />



b. Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu:
/home/stD02001/.bash_profile /home/stD02001/.bash_login /home/mahasiswa/.profile /home/mahasiswa/.bashrc
Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap file tersebut, cantumkan instruksi echo, misalnya pada /home/mahasiswa/.bash_profile:
echo "Profile dari .bash_profile"
Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yang bersangkutan.
<img width="1280" height="800" alt="t5 1 b" src="https://github.com/user-attachments/assets/31db9ab5-3d65-428a-b111-cb5870c762e1" />


c. Jalankan instruksi substitute user, kemudian keluar dengan perintah exit sebagai berikut:

2.$ su mahasiswa $ exit
<img width="1280" height="800" alt="t5 2" src="https://github.com/user-attachments/assets/f5de39f3-1d8a-4273-9f74-0e30ed2cc9b2" />


kemudian gunakan opsi – sebagai berikut:

$ su - mahasiswa $ exit

Jelaskan perbedaan kedua utilitas tersebut.

Prompt String (PS)
a. Edit file .bash_profile, ganti prompt PS1 dengan '>'. Instruksi export diperlukan dengan parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh shell.

PS1='> ' export PS1

b. Eksperimen hasil PS1:

$ PS1="! > " 69 > PS1="\d > " Mon Sep 23 > PS1="\t > " 10:10:20 > PS1="Saya=\u > " Saya=mahasiswa > PS1="\w > " ~ > PS1=\h >"

<img width="1280" height="800" alt="t5 2" src="https://github.com/user-attachments/assets/5885a734-47b2-42ab-b214-0b00c35c8a3c" />

3.Logout Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout.

Echo "Terima kasih atas sesi yang diberikan" Sleep 5 clear
<img width="1280" height="800" alt="t5 3" src="https://github.com/user-attachments/assets/47722f73-ec87-4bc9-9abc-0ba9fe578b9d" />


4. Bash script
a. Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing:
p1.sh
#!/bin/bash echo "Program p1" ls -l
p2.sh
#!/bin/bash echo "Program p2" who
p3.sh
#!/bin/bash echo "Program p3" ps x
<img width="1280" height="800" alt="VirtualBox_Ubuntu_13_10_2026_09_54_56" src="https://github.com/user-attachments/assets/4babc837-205e-44cf-be32-7f39f962e796" />


b. Jalankan script tersebut sebagai berikut:
$ ./p1.sh ; ./p3.sh ; ./p2.sh
$ ./p1.sh &
$ ./p1.sh & ./p2.sh & ./p3.sh &
<img width="1280" height="800" alt="t5 4 b" src="https://github.com/user-attachments/assets/667b8958-42ca-44ea-a5fa-68679ebecb07" />


5.Jobs
a. Buat shell-script yang melakukan loop dengan nama nyawaktu.sh, setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil.
#!/bin/bash
while [ true ] do date >> hasil sleep 10 done

b. Jalankan sebagai background, kemudian jalankan satu program (utilitas find) di background sebagai berikut:

$ jobs

$ find . -print > files 2>/dev/null &

$ jobs

c. Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut ke background.

$ fg %1

$ bg

d. Stop program background dengan utilitas kill

$ ps x

$ kill [Nomor PID]

History
a. Ganti nilai HISTSIZE dari 1000 menjadi 20

$ HISTSIZE=20

$ h

b. Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir dilakukan

$ !-5

c. Ulangi instruksi yang terakhir. Gunakan juga ^P dan ^N untuk bernavigasi pada history buffer

$ !!

d. Ulangi instruksi pada history buffer nomor 150

$ !150

e. Ulangi instruksi dengan prefix "ls"

$ !ls
