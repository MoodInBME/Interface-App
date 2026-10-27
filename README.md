# Interface-App

Aplikasi Flutter untuk Tugas Akhir **MoodIn**:

- **tampilan cermin** di NVIDIA Jetson Orin Nano Super (Linux), di balik cermin dua arah;
- **aplikasi pendamping** Android untuk akun, riwayat, dan pengaturan.

Keduanya menampilkan tingkat stres, kategori _mood_, dan tanda vital yang diterima lewat MQTT di jaringan lokal. Repo ini menggantikan [Interface-Display](https://github.com/MoodInBME/Interface-Display) (PySide6 + QML), yang sudah diarsipkan.

Bagian dari proyek [MoodIn](https://github.com/MoodInBME/MoodIn-master).

![tahap](https://img.shields.io/badge/tahap-persiapan-lightgrey)
![flutter](https://img.shields.io/badge/Flutter-UI-02569B?logo=flutter&logoColor=white)

> **Status (27 Okt 2026):** belum ada kode. Pengembangan dimulai di milestone M3, diawali uji kelayakan Flutter di Jetson.

## Rencana

1. **Uji kelayakan di Jetson** (Ubuntu 24.04, JetPack 7.2): _build_ Flutter untuk Linux, mode layar penuh, orientasi _portrait_, serta pemakaian CPU dan RAM saat model berjalan bersamaan. Bila ada kendala, hasil uji dibawa ke bimbingan sebelum layar dipindahkan.
2. **Kerangka monorepo** (rencana, dapat berubah):

   ```text
   Interface-App/
   ├── apps/
   │   ├── mirror/            tampilan cermin (Linux, Jetson)
   │   └── companion/         aplikasi pendamping (Android)
   └── packages/
       ├── moodin_contracts/  model pesan MQTT sesuai kontrak versi TA
       └── moodin_ui/         tema, komponen, dan aset bersama
   ```

3. **Layar dari desain Figma.** Berkas Figma tidak dipublikasikan.
4. **Klien kontrak pesan versi TA**, setelah kontrak ditetapkan di MoodIn-master.

## Prinsip tampilan

Prinsip berikut dibawa dari Interface-Display:

- tidak menampilkan angka basi atau hasil dari jendela pengukuran yang belum penuh;
- mode demo atau simulasi selalu diberi penanda yang terlihat;
- tidak pernah menerima citra wajah; hanya nilai numerik.

## Aset

Aset visual era GEMASTIK yang dipakai ulang, seperti maskot dan ikon _mood_, disalin dari Interface-Display. Asal setiap aset dicatat di `CHANGELOG.md` saat disalin.

## Lisensi

Belum ditetapkan; menunggu keputusan pembimbing.
