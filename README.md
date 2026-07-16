# 🎬 AnimeOvertime 🍿
> *"Disaat Kamu Mau Nonton Anime Tapi Malah Disuruh Overtime"*

![Format](https://img.shields.io/badge/Format-HTML5%20%2F%20TailwindCSS-indigo.svg)
![Database](https://img.shields.io/badge/Database-Firebase%20Firestore-orange.svg)
![API](https://img.shields.io/badge/API-AniList%20GraphQL-blue.svg)

**AnimeOvertime** adalah aplikasi berbasis web statis (Single Page & Multi-page hybrid) modern untuk melacak jadwal rilis anime musiman (*seasonal anime tracker*) sekaligus mencatat riwayat episode yang sudah kamu tonton. Proyek ini dibuat responsif, minimalis, dan terintegrasi langsung dengan cloud database untuk memastikan data kamu aman, meskipun bos di kantor menyuruhmu lembur mendadak.

---

## ✨ Fitur Utama

*   **📅 Real-time Airing Countdown:** Hitung mundur otomatis kapan episode anime favoritmu selanjutnya akan tayang di Jepang (termasuk konversi waktu lokal).
*   **🔍 Dual-Language Smart Search:** Cari anime incaranmu tanpa perlu khawatir salah eja. Pencarian mengenali judul dalam versi **English** maupun **Romaji** secara instan.
*   **📂 Split Season Watchlist:** Daftar simpanan anime (*watchlist*) otomatis dikelompokkan dan dipisahkan rapi berdasarkan musim (*Winter, Spring, Summer, Fall*) dan tahun penayangannya.
*   **🏁 Dynamic Filter Dropdown:** Menu dropdown di halaman Watchlist hanya memunculkan opsi musim yang **benar-benar ada isinya**, membuat UI terasa ringkas.
*   **📺 Interactive Episode Tracker:** Tandai progress nonton kamu per episode dengan warna indikator hijau estetik.
*   **🛡️ Secure Custom Deletion Confirmation:** Fitur pintar yang mencegah kehilangan data tidak sengaja. Jika kamu berniat menghapus anime yang sudah memiliki riwayat tontonan (*watched episodes*), sistem akan memunculkan modal konfirmasi kustom.
*   **🔐 Cloud Sync (Firebase Auth & Firestore):** Data *watchlist* dan progress episode tersimpan aman di cloud. Ganti perangkat dari PC kantor ke HP saat di jalan? Data tetap sinkron!
*   **⚙️ Multi-Language Title Preference:** Ubah preferensi tampilan nama anime global (English/Romaji) hanya dengan satu kali klik di panel pengaturan.

---

## 🛠️ Teknologi yang Digunakan

*   **Frontend UI:** HTML5 & [Tailwind CSS v4 (via CDN)](https://tailwindcss.com/)
*   **Data Source (API):** [AniList GraphQL API v2](https://github.com/AniList/ApiV2-GraphQL-Docs) (untuk katalog data anime dunia)
*   **Backend-as-a-Service (BaaS):** 
    *   **Firebase Authentication:** Sistem registrasi/masuk berbasis *virtual email formatting* (`username@animeovertime.com`).
    *   **Cloud Firestore:** Penyimpanan berbasis dokumen untuk data *watchlist* array dan data *nested* map episode.

---

## 📁 Struktur Berkas

```text
├── index.html          # Halaman utama (Daftar seasonal anime, filter, search, & auth modal)
├── watchlist.html      # Halaman khusus daftar simpanan user (Terproteksi Auth, Grouped by Season)
└── README.md           # Dokumentasi proyek (File ini)
