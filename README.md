# 🍷 Wine Quality Classification - Kinanti Anggraeni

## Deskripsi Proyek
Tujuan dari proyek ini adalah untuk membangun model klasifikasi yang dapat memprediksi nilai quality (kualitas anggur) berdasarkan parameter kimia seperti kadar alkohol, keasaman, kadar gula, pH, dan lainnya. Nilai quality berada pada skala 0 hingga 10.
Dataset terdiri dari:
- Data latih (training data): berisi fitur kimiawi serta label quality.
- Data uji (data_testing.csv): berisi fitur kimiawi tanpa label kualitas (untuk diprediksi).

## Data Preprocessing
- Cek dan memastikan tidak ada missing value
- Penyesuaian nama kolom untuk kemudahan analisis (rename)
- Visualisasi data: Boxplot dan scatterplot untuk melihat outlier dan korelasi fitur terhadap quality
- Korelasi fitur: Heatmap & Pairplot
- Normalisasi fitur numerik menggunakan MinMaxScaler

## Insight dari Visualisasi
- alcohol menunjukkan korelasi positif yang kuat dengan kualitas (0.47)
- volatile acidity memiliki korelasi negatif (-0.43)
- Fitur lain seperti density, citric acid, dan sulphates juga menunjukkan pola tertentu terhadap kualitas
- Terdapat outlier pada beberapa fitur seperti chlorides, residual sugar, dan total sulfur dioxide

## Modeling
1. Model yang Digunakan pada Prediksi:
- Random Forest (tuning hyperparameter via GridSearchCV)
- Keterangan hasil:
  - Akurasi model: 71,5%
  - Macro F1-score: 0.42
  - Weighted avg F1-score: 0.7
- Visualisasi: Confusion Matrix & Classification Report
2. Model lainnya yang dicoba
- KNeighborsClassifier
- Decision Tree
- Logistic Regression
##  Evaluasi Model
- Confusion matrix menunjukkan ketidakseimbangan kelas (beberapa label tidak terdeteksi dengan baik)
- Model paling akurat untuk memprediksi kualitas anggur dengan label 5 dan 6
- Perlu eksplorasi lebih lanjut terhadap teknik balancing data (SMOTE, undersampling, dll.)

## Kesimpulan 
1. Model Random Forest memberikan performa terbaik sejauh ini
2. Alkohol adalah fitur paling penting dalam menentukan kualitas anggur
3. Model masih perlu peningkatan dalam hal generalisasi dan penanganan data tidak seimbang

## 👩‍💻Author
Kinanti Anggraeni
UTS - Machine Learning
Statistika Terapan dan Komputasi
