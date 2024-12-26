# Prediksi Senyawa Kandidat Obat untuk Target KRAS (Kirsten Rat Sarcoma Viral Oncogene) Menggunakan Pendekatan Algoritma K-Nearest Neighbor (KNN)
# Kelompok 1 RB

Proyek ini bertujuan untuk mengidentifikasi senyawa kandidat obat yang berpotensi menargetkan KRAS (Kirsten Rat Sarcoma Viral Oncogene) menggunakan pendekatan algoritma K-Nearest Neighbor (KNN). KRAS adalah onkogen yang sering bermutasi dan terkait dengan kanker paru-paru, kolorektal, dan pankreas. Penelitian ini menggunakan metode machine learning untuk meningkatkan efisiensi dalam penemuan obat.

## Fitur Utama
- *Algoritma KNN*: Digunakan untuk mengklasifikasikan senyawa sebagai aktif atau tidak aktif berdasarkan karakteristik kimianya.
- *Preprocessing Data*: Termasuk normalisasi, imputasi data, dan pembagian dataset menjadi data latih dan data uji.
- *Oversampling dengan SMOTE*: Mengatasi ketidakseimbangan kelas dalam dataset untuk meningkatkan sensitivitas model terhadap kelas minoritas (senyawa aktif).
- *Optimasi Parameter*: Tuning parameter k, metrik jarak (*Euclidean dan Manhattan), dan pembobotan jarak untuk meningkatkan akurasi prediksi.
- *Evaluasi Model*: Meliputi akurasi, precision, recall, dan F1-score, dengan hasil evaluasi yang mencapai akurasi 84% pada data uji.

## Dataset
Penelitian ini menggunakan dua dataset:
1. *Dataset Lipinski*: Berisi informasi sifat kimia seperti berat molekul, logP, jumlah donor hidrogen, jumlah akseptor hidrogen, dll.
2. *Dataset Fingerprint Molekul*: Representasi struktural senyawa dalam format biner yang diambil dari database PubChem.

Kombinasi dari kedua dataset ini memberikan fitur kimia dan struktural yang komprehensif untuk analisis aktivitas biologis senyawa terhadap KRAS.

## Arsitektur Pemodelan
1. *Preprocessing Data*:
   - Normalisasi data numerik menggunakan Min-Max Scaling.
   - Transformasi kelas menjadi numerik.
   - Penggabungan fitur kimia dan fingerprint molekul.

2. *Klasifikasi KNN*:
   - Menentukan nilai optimal k melalui validasi silang.
   - Eksperimen dengan berbagai metrik jarak, termasuk Euclidean dan Manhattan.
   - Pembobotan jarak untuk memberikan bobot lebih besar pada tetangga yang lebih dekat.

3. *Oversampling dengan SMOTE*:
   - Menyeimbangkan distribusi kelas minoritas dengan interpolasi data sintetis.

4. *Evaluasi Model*:
   - Metrik evaluasi meliputi akurasi, precision, recall, dan F1-score.
   - Analisis confusion matrix untuk mengidentifikasi kekuatan dan kelemahan model.

## Hasil
- *Akurasi Model*: 84% pada data uji.
- *Precision, Recall, F1-Score*: Semua mencapai 84%.
- *Peningkatan Sensitivitas*: Penggunaan SMOTE meningkatkan sensitivitas model terhadap senyawa aktif.
