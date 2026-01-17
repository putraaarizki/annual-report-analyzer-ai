# 📊 AI Annual Report Analyzer (RAG w/ n8n)

![n8n](https://img.shields.io/badge/n8n-Workflow-orange?style=flat-square) ![AI](https://img.shields.io/badge/AI-RAG-blue?style=flat-square) ![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

> **Bot analisis dokumen keuangan otomatis berbasis n8n dan Retrieval-Augmented Generation (RAG).**

Project ini dibangun untuk mempermudah ekstraksi *insight* dari Laporan Tahunan (Annual Report) perusahaan yang seringkali mencapai ratusan halaman. Dengan menggunakan workflow otomatis n8n, pengguna dapat mengunggah file PDF dan melakukan tanya-jawab (chat) interaktif untuk mendapatkan data spesifik seperti rasio keuangan, strategi bisnis, hingga profil risiko.

---

## 🚀 Fitur Utama

* **📄 PDF Ingestion:** Secara otomatis membaca dan mengekstrak teks dari file PDF Laporan Tahunan.
* **🧠 Semantic Search:** Menggunakan Vector Database untuk mencari konteks yang relevan, bukan hanya pencarian kata kunci biasa.
* **💬 Interactive Q&A:** Chatbot cerdas yang bisa menjawab pertanyaan seperti *"Berapa laba bersih tahun ini dibandingkan tahun lalu?"* atau *"Apa strategi mitigasi risiko perusahaan?"*.
* **🔗 Citations:** (Opsional) Memberikan referensi halaman dari mana jawaban diambil agar data dapat diverifikasi.

## 🛠️ Tech Stack

Project ini menggunakan teknologi *Low-Code* yang dipadukan dengan *Modern AI Stack*:

* **Orchestration:** [n8n](https://n8n.io/) (Self-hosted / Cloud)
* **LLM (Brain):** OpenAI GPT-4o / GPT-3.5-turbo (bisa disesuaikan)
* **Vector Store (Memory):** Pinecone / Qdrant / Supabase Vector
* **Embeddings:** OpenAI text-embedding-3-small

## ⚙️ Cara Kerja (Workflow)

1.  **Load:** Pengguna mengunggah file PDF Annual Report.
2.  **Split:** Dokumen dipecah menjadi bagian-bagian kecil (chunks).
3.  **Embed:** Chunks diubah menjadi vektor angka (embeddings) dan disimpan ke Vector Database.
4.  **Retrieve:** Saat pengguna bertanya, sistem mencari chunks yang paling relevan secara semantik.
5.  **Generate:** LLM menjawab pertanyaan berdasarkan konteks chunks yang ditemukan.

## 📦 Cara Install & Penggunaan

1.  **Clone Repository ini:**
    ```bash
    git clone [https://github.com/username-kamu/n8n-rag-annual-report.git](https://github.com/username-kamu/n8n-rag-annual-report.git)
    ```
2.  **Import Workflow:**
    * Buka dashboard n8n kamu.
    * Klik **Add Workflow** > **Import from File**.
    * Pilih file `.json` yang ada di folder repository ini.
3.  **Setup Credentials:**
    * Masukan API Key OpenAI & Vector DB kamu di bagian *Credentials* n8n.
4.  **Jalankan:**
    * Aktifkan workflow dan mulai test chat.

## 📸 Screenshot

<img width="1367" height="621" alt="image" src="https://github.com/user-attachments/assets/f921249a-25ee-43fe-b0cd-ec51e2168ecd" />


![Workflow Screenshot](path/to/screenshot.png)

## 🤝 Kontribusi

Saran dan perbaikan sangat diterima! Silakan buat **Pull Request** atau buka **Issue** jika menemukan bug.

## 📝 Lisensi

Didistribusikan di bawah Lisensi MIT. Lihat `LICENSE` untuk informasi lebih lanjut.
