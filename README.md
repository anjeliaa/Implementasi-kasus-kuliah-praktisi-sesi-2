> **Materi:** *"Bridging Global Infrastructure to Address Local Challenges with High-Performance Computing (HPC)"*  
> **Narasumber:** Asst. Prof. Dr. Worawan Diaz Carballo (Thammasat University, Thailand)  
> **Penyelenggara:** Informatics Practitioner Lecture Series Program Studi Informatika, Universitas Bengkulu  
> **Tautan Video Webinar:** [YouTube Live - Informatics Practitioner Lecture Series](https://www.youtube.com/live/qeWpf9uXBqE?si=93aEOgHdIRU9MQ2z)

---

## 📌 Ringkasan Studi Kasus

Penggunaan energi listrik pada gedung-gedung fasilitas kampus kerap mengalami pemborosan akibat tingginya penggunaan pendingin udara (AC) serta perilaku penghuni (*agents*) yang kurang mematuhi regulasi efisiensi energi. Manajemen kampus membutuhkan simulasi akurat untuk menguji dampak berbagai kebijakan efisiensi sebelum menerapkannya di lapangan secara langsung.

### **Pertanyaan Utama & Kebutuhan Operasional**
> *"Bagaimana memodelkan interaksi ribuan agen penghuni gedung secara paralel (HPC) untuk menemukan skenario kebijakan energi yang paling hemat biaya tanpa mengganggu kenyamanan dan aktivitas akademik?"*

### **Solusi Data Science & High-Performance Computing**
Menggunakan pendekatan **Agent-Based Modeling (ABM)** yang dijalankan secara paralel menggunakan pemrosesan **High-Performance Computing (HPC)** untuk memodelkan perilaku 2.000 agen dalam gedung kampus selama 24 jam dan mengukur total pemakaian listrik (kWh) per skenario kebijakan.

---

## 🔄 Metodologi Implementasi HPC

Proyek ini dilaksanakan mengikuti 6 tahapan alur kerja *Parallel Simulation & Energy Modeling*:

```mermaid
graph LR
    A[1. Local Problem Formulation] --> B[2. Agent Behavior Definition]
    B --> C[3. HPC Parallel Processing]
    C --> D[4. Data Aggregation]
    D --> E[5. Power Efficiency Analytics]
    E --> F[6. Policy Decision & Action]
1. **Local Problem Formulation:** Identifikasi pembengkakan biaya listrik gedung akibat penggunaan AC berlebih dan operasional jam malam.
2. **Agent Behavior Definition:** Merumuskan probabilitas kehadiran agen (mahasiswa/staf), tingkat kepatuhan terhadap aturan, serta beban temperatur AC.
3. **HPC Parallel Processing:** Mendistribusikan beban kalkulasi simulasi 2.000 agen secara simultan menggunakan *multiprocessing / parallel core execution*.
4. **Data Aggregation:** Mengumpulkan dan menjumlahkan beban daya listrik gedung secara riil dari seluruh agen untuk tiap jam simulasi.
5. **Power Efficiency Analytics:** Mengukur total konsumsi daya harian (kWh) serta kecepatan waktu eksekusi komputasi (*Execution Time*).
6. **Policy Decision & Action:** Merekomendasikan penetapan temperatur baku AC (24°C–25°C) dan pembatasan jam operasional otomatis gedung.

---

## 📈 4 Level Tingkatan Analytics

| Level Analytics | Pertanyaan Utama | Hasil / Implementasi pada Kasus |
| :--- | :--- | :--- |
| **Descriptive** | *Apa yang terjadi?* | Pembengkakan konsumsi listrik harian gedung pada jam-jam puncak aktivitas akademik. |
| **Diagnostic** | *Mengapa ini terjadi?* | Simulasi agen menunjukkan pengaturan temperatur AC di bawah 20°C dan pelanggaran jam operasional menjadi penyumbang terbesar pemborosan daya. |
| **Predictive** | *Apa yang akan terjadi?* | Model simulasi HPC memprediksi akumulasi konsumsi listrik harian (kWh) berdasarkan skenario tingkat kepatuhan agen. |
| **Prescriptive** | *Apa tindakan terbaik?* | Penerapan kebijakan *Energy Saving A* (AC 24°C dan pembatasan jam malam) yang terbukti memotong konsumsi listrik hingga **~35-40%**. |

---

## 📊 Ringkasan Hasil Simulasi HPC

| Skenario Kebijakan Energi | Temperatur AC | Maks Jam Ops | Total Listrik (kWh) | Efisiensi Hemat Daya |
| :--- | :---: | :---: | :---: | :---: |
| **Baseline (Tanpa Aturan)** | 20°C | 22:00 | ~40.300 kWh | 0% (Acuan) |
| **Energy_Saving_A (Rekomendasi)** 🏆 | **24°C** | **20:00** | **~18.800 kWh** | **~53.3%** |
| **Strict_Green_B (Ketat)** | 25°C | 18:00 | ~12.500 kWh | ~69.0% |

---

## 💡 Rekomendasi Kebijakan & Intervensi Lapangan

1. **Penetapan Suhu AC Standar:** Mengunci termostat pendingin udara pada suhu minimal **24°C** di seluruh ruang kelas dan laboratorium.
2. **Otomatisasi Jam Operasional Gedung:** Mematikan sistem daya non-esensial secara otomatis pada pukul **20:00 WIB** untuk memangkas pemakaian daya standby.
3. **Edukasi Kepatuhan Agen:** Mengalokasikan insentif efisiensi bagi unit/departemen yang berhasil menjaga tingkat kepatuhan efisiensi listrik di atas 80%.
