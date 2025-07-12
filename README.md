# Ujian Akhir Semester (UAS) - Data Wrangling (DaWr1)

## Dokumentasi & Kesimpulan Feature Selection

Analisis dilakukan menggunakan dua metode seleksi fitur pada dataset breast cancer:
1. **Univariate Feature Selection**
2. **Recursive Feature Elimination (RFE)**

### Hasil Output
Kedua metode berhasil memilih 5 fitur terbaik dari dataset. Univariate Feature Selection menggunakan skor statistik (chi-square), sedangkan RFE menggunakan model Random Forest untuk mengeliminasi fitur secara bertahap.

### Tabel Perbandingan Metode Feature Selection

| Aspek                        | Univariate Feature Selection                | Recursive Feature Elimination (RFE)         |
|------------------------------|--------------------------------------------|---------------------------------------------|
| **Prinsip/Metode Kerja**     | Memilih fitur berdasarkan skor statistik (misal: chi-square, ANOVA) secara individual tanpa mempertimbangkan interaksi antar fitur. | Mengeliminasi fitur secara bertahap dengan membangun model (misal: Random Forest), menghapus fitur paling tidak penting, dan mengulang proses hingga tersisa jumlah fitur yang diinginkan. |
| **Ketergantungan Model**     | Tidak bergantung pada model; hanya menggunakan metode statistik. | Sangat bergantung pada model yang digunakan untuk menilai pentingnya fitur. |
| **Kelebihan**                | - Cepat dan sederhana<br>- Mudah diinterpretasi<br>- Cocok untuk data dengan banyak fitur | - Mempertimbangkan interaksi antar fitur<br>- Dapat digunakan dengan berbagai model<br>- Hasil lebih relevan untuk model yang digunakan |
| **Kekurangan**               | - Tidak mempertimbangkan interaksi antar fitur<br>- Bisa memilih fitur yang redundant | - Lebih lambat dan membutuhkan komputasi lebih besar<br>- Hasil sangat tergantung pada model yang dipilih |
| **Kapan Digunakan**          | - Saat ingin seleksi fitur secara cepat<br>- Untuk eksplorasi awal<br>- Data sangat besar | - Saat ingin seleksi fitur yang optimal untuk model tertentu<br>- Ketika interaksi antar fitur penting<br>- Untuk model yang kompleks |

### Rangkuman
- **Univariate Feature Selection** cocok untuk analisis awal, eksplorasi, atau seleksi fitur secara cepat tanpa mempertimbangkan interaksi antar fitur.
- **RFE** lebih baik digunakan untuk mendapatkan subset fitur yang optimal untuk model tertentu, terutama jika interaksi antar fitur berpengaruh besar terhadap performa model.

Kedua metode dapat digunakan secara komplementer: Univariate untuk penyaringan awal, RFE untuk seleksi lanjutan yang lebih optimal sesuai model yang digunakan.