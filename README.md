# 🐄💧 Livestock WaterSense
 
**Sistem pemberi minum otomatis untuk ternak berbasis IoT, dengan pemantauan level air, penggunaan air, dan suhu lingkungan secara real-time melalui aplikasi mobile.**

## 📖 Deskripsi
 
**Livestock WaterSense** adalah proyek IoT yang dirancang untuk membantu peternak menjaga ketersediaan air minum ternak secara otomatis dan efisien. Sistem membaca level air pada tandon/tempat minum menggunakan **sensor ultrasonik**, lalu mengendalikan **pompa air** secara otomatis ketika level air menurun. Selain itu, sistem memantau **suhu sekitar** dan menampilkan seluruh data secara real-time pada **aplikasi mobile**.
 
## 🎯 Tujuan
 
- Mengotomatiskan pengisian air minum ternak berdasarkan level air.
- Mengurangi pemborosan air dan kebutuhan pengecekan manual.
- Memberikan data penggunaan air dan kondisi lingkungan yang dapat dipantau dari jarak jauh.
## ✨ Fitur Utama
 
| Fitur | Keterangan |
|---|---|
| 📏 **Pemantauan level air** | Mengukur ketinggian air menggunakan sensor ultrasonik |
| 🚰 **Monitoring penggunaan air** | Menampilkan total penggunaan air (liter) secara real-time |
| 🔌 **Status pompa air** | Menampilkan kondisi pompa: hidup / mati |
| ⚙️ **Mode otomatis** | Pompa menyala otomatis saat level air rendah dan berhenti pada batas yang ditentukan |
| 🎚️ **Batas level kustom** | Pengguna dapat mengatur batas level air untuk mode otomatis |
| 🌡️ **Pemantauan suhu** | Membaca suhu di sekitar area ternak |
| 📱 **Monitoring via mobile** | Seluruh data dapat dipantau melalui aplikasi mobile |
 
## 🧠 Cara Kerja
 
1. Sensor ultrasonik mengukur jarak permukaan air untuk menghitung level air.
2. Mikrokontroler memproses data dan membandingkannya dengan batas level yang diatur pengguna.
3. Pada **mode otomatis**, jika level air berada di bawah batas bawah, pompa menyala hingga level air mencapai batas yang ditentukan, lalu pompa mati.
4. Data level air, penggunaan air (liter), suhu, dan status pompa dikirim ke aplikasi mobile secara real-time.
```
[Sensor Ultrasonik] ─┐
[Sensor Suhu]  ──────┼──► [Mikrokontroler] ──► [Relay] ──► [Pompa Air]
                     │          │
                     │          ▼
                     └────► [Cloud / Server] ──► [Aplikasi Mobile]
```
 
> Sesuaikan diagram di atas dengan arsitektur sebenarnya. Kamu juga bisa mengganti dengan gambar diagram sistem.
 
## 🧰 Teknologi & Komponen
 
**Hardware**
- Mikrokontroler: `ESP 32`
- Sensor ultrasonik: `Ultrasonik HC`
- Sensor suhu: `DHT 11`
- Modul relay : `2 channel`
**Software**
- Firmware: `Arduino IDE`
- Komunikasi data: MQTT Hive Broker
- Aplikasi mobile: `Flutter, Android Studio`

## 👥 Tim Pengembang & Kontribusi
 
Proyek ini dikerjakan secara kolaboratif oleh tim berikut:
 
### Ghazy Fadhillah Abid
- UI/UX Design
- Wireframe
- RPP
- Report Document
- Activity Diagram
- IoT & Application Integration
- General System Design
- IoT & MQTT Integration
### Sindy Maharani
- ERD
- Use Case Diagram
- Sequence Diagram
- Report Document
- Frontend (User)
- PPT ATS
- Manual Book
- Final Report
### Willy Fernando
- Wiring design of IoT system
- Early stage IoT system
- Advanced stage IoT system
- HKI
- BAST
### Irmayani
- Use Case Scenario
- Frontend (Admin)
- Relationship Model
- Class Diagram
- Document Report
- Backend Application
- Poster
- PPT AAS
