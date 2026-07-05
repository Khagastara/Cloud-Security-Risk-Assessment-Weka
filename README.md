# Cloud-Security-Risk-Assessment-Weka
Proyek ini menilai risiko keamanan komputasi awan menggunakan beberapa model klasifikasi. Proyek ini memperluas metodologi dari Sharma dan Singh (2022) dengan menambahkan data sintetis dan teknik ensemble stacking.

## Latar Belakang
Penilaian risiko keamanan cloud membutuhkan model yang akurat untuk mengklasifikasikan tingkat risiko berdasarkan berbagai faktor operasional. Metodologi <a href="https://doi.org/10.1016/j.gltp.2022.03.030">Sharma dan Singh (2022)</a> menjadi dasar proyek ini. Proyek ini memperluas metodologi tersebut dengan menambah jumlah faktor risiko dan menguji kombinasi beberapa classifier.

## Dataset
Data yang digunakan adalah data sintetis dengan 12 faktor risiko. Data ini dirancang untuk merepresentasikan kondisi keamanan cloud secara sistematis, mencakup variabel operasional yang relevan terhadap tingkat risiko.

## Metode
Model dibangun menggunakan tiga classifier di WEKA. Model pertama adalah Decision Tree. Model kedua adalah Randomizable Filter Classifier. Model ketiga adalah K-star.
Ketiga model kemudian digabungkan menggunakan teknik ensemble stacking. Teknik ini menggabungkan prediksi dari beberapa model dasar untuk menghasilkan prediksi akhir yang lebih stabil.
Proyek ini juga menyertakan simulasi berbasis SLA menggunakan OpenStack. Simulasi ini menguji skenario operasional nyata pada infrastruktur cloud.

## Hasil
Hasil evaluasi tiap classifier disimpan dalam folder <b>results/</b> dalam format teks langsung dari output RMSE pada WEKA.
| Algoritma                        | 50% Testing | 35% Testing | 15% Testing | 5% Testing |
|----------------------------------|-------------|-------------|-------------|------------|
| Decision Tree Classifier         | 0,5065 | 0,5314 | 0,546  | 0,5408 |
| Randomizable Filtered Classifier | 0,5494 | 0,5678 | 0,5663 | 0,5732 |
| K-Star                           | 0,4853 | 0,5007 | 0,5183 | 0,5413 |
