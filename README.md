# ☁️ Amazon EC2 Mastery: Scalable Computing for the Modern Era

## 📖 Overview
Amazon Elastic Compute Cloud (Amazon EC2) adalah tulang punggung dari infrastruktur **AWS Cloud**. Layanan ini menyediakan kapasitas komputasi yang aman dan dapat diubah ukurannya di cloud. Repositori ini didedikasikan untuk mendokumentasikan implementasi sistem yang berfokus pada **Efisiensi Performa** dan skalabilitas tinggi.

---

## 🚀 Fitur Utama & Keunggulan
* **Elasticity:** Kemampuan untuk melakukan *scaling* secara otomatis dengan *Auto Scaling Groups*.
* **Full Control:** Akses tingkat *root* ke setiap instans untuk kustomisasi penuh.
* **Security:** Terintegrasi dengan Amazon VPC dan Security Groups untuk isolasi jaringan tingkat tinggi.
* **Cost-Efficiency:** Pilihan tipe instans yang beragam (On-Demand, Reserved, dan Spot Instances).

---

## 🏗️ Komponen Arsitektur EC2
1.  **AMI (Amazon Machine Image):** Template siap pakai yang berisi OS dan konfigurasi aplikasi.
2.  **Instance Types:** Optimasi berdasarkan beban kerja (Compute, Memory, Storage, atau General Purpose).
3.  **EBS (Elastic Block Store):** Media penyimpanan persisten dengan performa tinggi.
4.  **Key Pairs:** Protokol keamanan menggunakan enkripsi kunci publik-privat untuk akses SSH.

---

## ⚡ Strategi Optimasi Performa (IT Expert Level)
Untuk menjaga **Efisiensi Performa**, berikut adalah *checklist* yang sering saya gunakan:
- [x] **Right-Sizing:** Memastikan tipe instans sesuai dengan utilisasi CPU/RAM.
- [x] **Placement Groups:** Mengurangi latensi antar instans dalam beban kerja HPC.
- [x] **Instance Metadata Service (IMDSv2):** Meningkatkan keamanan akses metadata instans.
- [x] **EBS-Optimized Instances:** Memastikan throughput penyimpanan maksimal tanpa hambatan jaringan.

---

## 🛠️ Contoh Implementasi: Web Server High Availability
```bash
# Script sederhana untuk inisialisasi Apache di EC2 (User Data)
#!/bin/bash
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
echo "<h1>Deployed by nawvalovsky via Amazon EC2</h1>" > /var/www/html/index.html
