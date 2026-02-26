### 🌉 Enterprise Batch Data Pipeline: Big Data Processing with Spark

Batch Data Ingestion & Processing with Spark  
**Enterprise Edition** (WSL + VS Code + Data Lake + Partitioning)  

**Programming Language:** Python  
**Work Environment:** Linux Server Environment  
**Code Editor:** VS Code (Remote WSL)  
**Command Line Interface:** Bash  
**Distributed Data Processing Engine:** PySpark  

---

##  👨‍🏫 Dosen Pembimbing
[![GitHub - Muhayat Lab](https://img.shields.io/badge/GitHub-Muhayat--Lab-181717?logo=github&style=for-the-badge)](https://github.com/muhayat-lab)

##  👨‍💻 Developer
[![GitHub - Zharvian](https://img.shields.io/badge/GitHub-Zharvians-007ACC?logo=github&style=for-the-badge)](https://github.com/Zharvians)

**Nama:** Muhammad Ade Ramadhani  
**NPM:** 230104040213  
**Kelas:** TI23A  

---

## 🗂 Project Overview

Enterprise batch data pipeline yang dirancang untuk:

- Mengambil data mentah (raw) dari sumber CSV  
- Membersihkan data (cleaning) dan menghapus duplikasi/NA  
- Transformasi data (hitung total_amount per transaksi)  
- Agregasi data (top products, revenue per kategori, rata-rata transaksi per customer)  
- Menyimpan data ke **Data Lake** dalam format Parquet, termasuk **partitioned by category**  

Pipeline ini dibuat untuk **pembelajaran Big Data Enterprise** dengan **PySpark di WSL**.

---

## 📁 Struktur Project
```bash 
bigdata-project/
├── data/
│ ├── raw/ # CSV input
│ ├── clean/ # Data bersih
│ └── curated/ # Hasil agregasi & analytics
├── logs/ # Log pipeline
├── scripts/ # Script pipeline PySpark
├── venv/ # Virtual environment Python
└── README.md
```

---

## ⚙ Setup & Requirements

1. **WSL Ubuntu 22.04**  
2. **Python 3.12+** + `python3-venv`  
3. **Java OpenJDK 17** (JAVA_HOME diset)  
4. **PySpark 3.5+** (install via `pip install pyspark==3.5.2`)  
5. **VS Code Remote WSL** untuk editing dan running script  

---

## 🚀 Cara Menjalankan Pipeline

1. Aktifkan virtual environment:

```bash
source venv/bin/activate
```

2. Jalankan pipeline:
```bash
python scripts/batch_pipeline_enterprise.py
```

3. Output akan disimpan di:
```bash
data/clean/parquet/ → Clean layer
data/curated/category_revenue/ → Revenue per kategori
data/curated/top_products/ → Top products
data/curated/avg_transaction/ → Rata-rata transaksi per customer
data/clean/partitioned_by_category/ → Partitioned clean layer
```

---

## 📌 Catatan
```bash
- Pastikan folder data/raw/ sudah berisi file ecommerce_raw.csv sebelum menjalankan pipeline
- .gitignore menyertakan: venv/, logs/, data/clean/, data/curated/ agar tidak ikut di-push ke GitHub
```

---

### 📜 License
```bash
Proyek ini dibuat untuk keperluan akademik
Praktikum 2 – Teknologi Big Data

Dilarang menggunakan untuk kepentingan komersial.
© 2026 — 230104040213. Seluruh hak dilindungi.
```
