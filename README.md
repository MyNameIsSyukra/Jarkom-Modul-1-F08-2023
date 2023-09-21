# Jarkom-Modul-1-F08-2023
## Kelompok F08
1. Keyisa Raihan Illah Setiadi 5025211002
2. Syukra Wahyu Ramadhan 5025211037

## No 1.
### Soal
User melakukan berbagai aktivitas dengan menggunakan protokol FTP.
a. Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut?
b. Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut?
c. Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
d. Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
### Penyelesaian
  - Pertama, import terlebih dahulu yang telah disediakan ke wireshark
  - kedua, lakukan display capture : FTP
  - kemudian cari packet yang sekiranya mencurigakan, pada soal ini terletak pada packet 147
  - buka packet tersebut dan temukan sequence number (raw) dan acknowledge number (raw)
  - untuk menjawab soal c dan d, packet response terletak pada packet setelah 147
  - buka packet tersebut dan temukan sequence number (raw) dan acknowledge number (raw)
    
![No1 0](https://github.com/MyNameIsSyukra/Jarkom-Modul-1-F08-2023/assets/90988646/8f7d014a-7456-4778-9ea3-e9cf63166757)
![no 1 1](https://github.com/MyNameIsSyukra/Jarkom-Modul-1-F08-2023/assets/90988646/0d1e502a-c421-4251-bc6f-0f3e4fa5573e)
### Kesulitan
  - Clue pada soal cukup sedikit,sehingga cukup kesulitan menemukan packet yang diinginkan

## Soal2
### Soal
Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!
### Penyelesaian
  - Pertama, import file yang disediakan ke wireshark
  - Kemudian display capture filter : 'ip.addr == 10.21.78.111' dimana 10.21.78.111 merupakan ip address dari web jarkom
  - Pilih salah satu packet
  - Kemudian click kanan->follow->tcpstream kemudian temukan webserver
    
![no2 1](https://github.com/MyNameIsSyukra/Jarkom-Modul-1-F08-2023/assets/90988646/eabed767-f41e-4ea4-b146-814e6970941e)
![no2 1](https://github.com/MyNameIsSyukra/Jarkom-Modul-1-F08-2023/assets/90988646/eabed767-f41e-4ea4-b146-814e6970941e)
### Kesulitan 
  -
## Soal3
### Soal
Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:
a. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?
b. Protokol layer transport apa yang digunakan?
### Penyelesaian
  - Pertama, Import file yang disediakan ke wireshark
  - kemudian display capture filter : ip.addr == 239.255.255.250 && udp.dstport == 3702
  - Hitung banyak packet yang pada kasus ini berjumlah 21
  - Untuk protokol layer transport yang digunakan dapat dilihat pada kolom protokol pada wireshark : UDP
    
![no3 0](https://github.com/MyNameIsSyukra/Jarkom-Modul-1-F08-2023/assets/90988646/3fcf707a-8e0e-4bd8-ad62-88ff00cac75c)
### Kesulitan
  -

## Soal4
### Soal
Berapa nilai checksum yang didapat dari header pada paket nomor 130?
### Penyelesaian
  - Import file ke wireshark
  - temukan packet nomer 130
  - buka packet tersebut dan temukan nilai checksum pada user datagram protocol :0x18e5
    
![no4 0](https://github.com/MyNameIsSyukra/Jarkom-Modul-1-F08-2023/assets/90988646/6e0e2ffa-6c60-40d7-b707-c4e3eda1f85a)
### Kesulitan
  -

## Soal5
### Soal 
Elshe menemukan suatu file packet capture yang menarik. Bantulah elshe untuk menganalisis file packet capture tersebut.
a. Berapa banyak packet yang berhasil di capture dari file pcap tersebut?
b. Port berapakah pada server yang digunakan untuk service SMTP?
c. Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP?
### Penyelesaian
  - Download semua file yang disediakan
  - Unlock txt :
    - import file soal4.pcanpg ke wireshark
    - Temukan packet yang mencurigakan, pada kasus ini terletak pada packet 16 yang merupakan email
    - klik kanan -> follow -> TCP Stream
    - Temukan password yang masih dalam bentuk base 64
    - lakukan decode base 64 : 5implePas5word
  - Banyak packet yang berhasil di capture dapat dilihat pada jumlah packet number atau dapat dihitung mandiri
  - Port yang digunakan pada service SMTP:
    - display capture filter : smtp
    - double click pada salah satu packet
    - kemudian temukan port yang digunakan : 25
  - Alamat IP public:
    - dapat dilakukan secara bruteforece dengan mencoba satu-satu alamat ip yang ada
      
![no5 1](https://github.com/MyNameIsSyukra/Jarkom-Modul-1-F08-2023/assets/90988646/868c56bc-9212-420b-bc78-8159c04bef99)
![no5 2](https://github.com/MyNameIsSyukra/Jarkom-Modul-1-F08-2023/assets/90988646/879fba35-f16c-47c3-a3aa-cdf9f9a97957)
![no5 3](https://github.com/MyNameIsSyukra/Jarkom-Modul-1-F08-2023/assets/90988646/0aed66e2-978e-4805-899d-e100a55e6c30)
### Kesulitan
  - Kesulitan untuk menemukan password dari file txt

