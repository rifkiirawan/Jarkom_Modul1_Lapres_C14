# Lapres Modul1 Kelompok C14

## A. Display Filter
## 1. Sebutkan webserver yang digunakan pada "testing.mekanis.me"!
### Menggunakan Display filter : http.host == "testing.mekanis.me"
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/1.png?raw=true)
### Follow -> TCP Stream
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/1b.png?raw=true)
### Dapat terlihat webserver yang digunakan, yaitu NGINX
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/1c.png?raw=true)

## 2. Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!
### Menggunakan Display filter : http contains "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/2.png?raw=true)
### Meggunakan Export object
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/2b.png?raw=true)
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/2c.png?raw=true)
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/2d.png?raw=true)

## 3. Cari username dan password ketika login di "ppid.dpr.go.id"!
### Menggunakan Display filter : http.host contains "ppid.dpr.go.id"  && http.request.method == "POST", lalu username dapat dilihat pada HTML form URL
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/3.png?raw=true)

## 4. Temukan paket dari web-web yang menggunakan basic authentication method!
### Menggunakan Display filter : http.www_authenticate
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/4.png?raw=true)

## 5. Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!
### Menggunakan Display filter : http.host contains "aku.pengen.pw"
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/5.png?raw=true)
### Lalu password dan username dapat ditemukan pada authorization
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/5b.png?raw=true)
### Buka website aku.pengen.pw lalu masukkan username dan passwordnya lalu terdapat soal yang jawabannya seperti di gambar
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/5c.png?raw=true)

## 6. Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file  zipkey.txt (passwordnya adalah isi dari file txt tersebut).
### Menggunakan Display filter : ftp-data.command == "STOR zipkey.txt" || ftp-data.command == "STOR Answer.zip"
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/6.png?raw=true)
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/6b.png?raw=true)
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/6c.png?raw=true)
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/6d.png?raw=true)
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/6e.png?raw=true)

## 7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut. Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf"
### Menggunakan Display filter : frame contains "Yes.pdf"
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/7.png?raw=true)
### Follow -> TCP Stream
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/7b.png?raw=true)
### Save as RAW
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/7c.png?raw=true)
### Unzip file .zip yang telah di save
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/7d.png?raw=true)
### Isi dari file Yes.pdf setelah dibuka
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/7e.png?raw=true)

## 8. Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!
### Mencari ip address Microsoft FTP Service Menggunakan Display Filter : ftp contains "Microsoft FTP Service
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/8.png?raw=true)
### Menggunakan Display filter : ftp.request.command == RETR && ip.dst == 198.246.117.106
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/8b.png?raw=true)

## 9. Cari username dan password ketika login FTP pada localhost!
### Menggunakan Display filter : ftp.request.command == "USER" || ftp.request.command == "PASS"
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/9.png?raw=true)

## B. Capture Filter
## 10. Cari file .pdf di wireshark lalu download dan buka file tersebut! clue: "25 50 44 46" 
### Dapat diselesaikan dengan cara : ctrl+f -> hex value -> 25 50 44 46 -> follow -> tcp stream
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/10.png?raw=true)
### ubah jadi raw
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/10b.png?raw=true)
### selesai
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/10c.png?raw=true)

## 11. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21! 
### Menggunakan Capture filter : Port 21
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/11.png?raw=true)
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/11b.png?raw=true)

## 12. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!
### Menggunakan Capture filter : src port 80
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/12.png?raw=true)
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/12b.png?raw=true)

## 13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443! 
### Menggunakan Capture filter : Dst port 443
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/13.png?raw=true)
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/13b.png?raw=true)

## 14. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian! 
### Mendapatkan alamat IP kami dari CMD
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/14.png?raw=true)
### Menggunakan Capture filter : Src host 192.168.42.252 (Alamat IP)
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/14b.png?raw=true)
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/14c.png?raw=true)

## 15. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!
### Menggunakan Capture filter : dst host monta.if.its.ac.id
![alt text](https://github.com/rifkiirawan/Jarkom_Modul1_Lapres_C14/blob/main/img/15.png?raw=true)

# Kendala selama pengerjaan :
### - Masih kurang dalam filter-filter yang dapat digunakan
### - Kurang mengerti cara mengerjakan sesuai dengan permintaan soal
