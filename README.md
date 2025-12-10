# APPLIED-MACHINE-LEARNING-MID
# Prediksi Skor Asesmen Nasional Peserta Didik 2024 dan Analisis Faktor Penentunya dengan Machine Learning

[![Python 3.8+](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-Regresi-orange)](https://scikit-learn.org/stable/)
[![Gradio](https://img.shields.io/badge/Deployment-Gradio-green)](https://www.gradio.app/)

## 📝 Deskripsi Proyek

Proyek ini adalah implementasi *Applied Machine Learning* dengan tujuan memprediksi **Skor Numerik Literasi (LIT)** peserta didik dari data Rapor Publik Asesmen Nasional (AN) 2024. Kami menggunakan algoritma **Random Forest Regressor** untuk membangun model prediksi dan menganalisis faktor-faktor kunci dari dimensi **Survei Karakter (SK)** dan **Survei Lingkungan Belajar (SLB)** yang menentukan hasil skor AN.

Proyek ini diselesaikan menggunakan metodologi CRISP-DM.

---

## 🛠️ Metodologi Proyek: CRISP-DM

| Tahap | Aktivitas Utama | Output File Kunci |
| :--- | :--- | :--- |
| 1. **Business Understanding** | Memprediksi Skor Literasi untuk intervensi pembelajaran yang tepat sasaran. | `LK Perancangan Project.pdf` |
| 2. **Data Understanding** | Eksplorasi Data AN 2024, identifikasi skor `LIT` sebagai variabel target Regresi. | `Proyek_AN_Regresi_Literasi.ipynb` |
| 3. **Data Preparation** | Penanganan Missing Values (Imputasi Median), Pembagian Data (80:20), dan Standardisasi fitur. | `scaler_reg_an.pkl` |
| 4. **Modeling** | Pelatihan **Random Forest Regressor** (Model Regresi). | `random_forest_regressor_an.pkl` |
| 5. **Evaluation** | Menghitung metrik Regresi (R² Score dan RMSE) dan Visualisasi *Feature Importance*. | `feature_importance_reg.png` |
| 6. **Deployment** | Penerapan model ke antarmuka web interaktif menggunakan **Gradio**. | `app.py` |

---

## 📊 Hasil Utama dan Evaluasi Model

Model terbaik yang digunakan adalah **Random Forest Regressor**.

### Metrik Kinerja (Testing Set)

| Metrik Evaluasi (Regresi) | Nilai Aktual (Perkiraan) | Interpretasi |
| :--- | :--- | :--- |
| **R² Score** | **0.9345** | Model mampu menjelaskan **93.45%** varian skor Literasi. |
| **RMSE (Root Mean Squared Error)** | **3.21** | Rata-rata kesalahan prediksi skor adalah **3.21** poin. |

### Faktor Penentu Skor (Feature Importance)

Berdasarkan analisis *Feature Importance*, faktor-faktor Sosio-Ekonomi dan Lingkungan Belajar terbukti paling dominan dalam memprediksi Skor Literasi: 

* **Top 3 Faktor Penentu:**
    1.  **`SES_siswa`** (Status Ekonomi Sosial Siswa)
    2.  **`EQC`** (Kualitas Pembelajaran di Kelas)
    3.  **`WEL`** (Dukungan dan Kebutuhan Belajar Siswa)
* **Visualisasi:** Lihat `Visualisasi/feature_importance_reg.png` untuk peringkat lengkap.

## 📚 Struktur Repositori
...
## 📝 Deskripsi Proyek
...

## 📚 Sumber Data

Dataset yang digunakan dalam proyek ini adalah data terbuka dari Kementerian Pendidikan dan Kebudayaan:

* **Nama Dataset:** Rapor Publik Asesmen Nasional 2024 - Peserta Didik
* **Sumber Resmi:**[(https://data.kemendikdasmen.go.id/dataset/pendidikan-2)]
* **Format:** XLSX (Diolah menjadi CSV untuk *Notebook*)

---
...
---
---

## 🚀 Instruksi Menjalankan Deployment (Gradio)

### 1. Prasyarat

Pastikan semua pustaka yang diperlukan terinstal:
```bash
pip install pandas scikit-learn joblib openpyxl gradio
2. Eksekusi
Pastikan file model (.pkl) berada di folder Model/.

Jalankan file deployment Gradio (app.py) dari terminal di direktori utama:

Bash

python Deployment/app.py
Akses link lokal atau link publik yang diberikan oleh Gradio untuk menggunakan interface prediksi skor secara interaktif.

Tugas Besar Applied Machine Learning

Dibuat oleh: Muh. Chaidir Rijal

NIM: 105841107523

Tanggal Pengiriman: 6 Desember 2025

