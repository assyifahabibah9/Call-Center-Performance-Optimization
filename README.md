# Call Center Performance Optimization: Mengoptimalkan Efisiensi Operasional Layanan Pelanggan

*Analisis End-to-End Terhadap 5.000 Log Panggilan untuk Mengevaluasi Bottlenecks Operasional dan Kinerja Agen — PwC Virtual Case Experience*

---

## Latar Belakang

Di industri penyedia jasa layanan pelanggan (*Customer Service*), operasional Call Center merupakan garda terdepan dalam menjaga reputasi bisnis dan kepuasan pelanggan. Kecepatan merespons panggilan serta kualitas penyelesaian masalah adalah dua faktor utama yang menentukan keberhasilan retensi. Hambatan kecil pada efisiensi waktu antrean dapat memicu efek domino berupa kekecewaan pelanggan secara massal.

Proyek ini merupakan bagian dari **PwC Virtual Case Experience (Data Analyst Job Simulation)**. Dalam simulasi ini, saya bertindak sebagai analis yang bertanggung jawab untuk melakukan evaluasi operasional komprehensif terhadap kinerja harian agen dan efisiensi sistem Call Center guna mendeteksi akar masalah pelayanan serta merumuskan rekomendasi strategis yang tajam bagi pihak manajemen perusahaan.

---

## Dataset & Metrik Utama

* **Sumber Data:** PwC Virtual Case Experience (Call-Center-Dataset.xlsx)
* **Ukuran Data:** 5.000 baris log panggilan (Mencakup periode Januari - Maret 2021)
* **Tools:** Microsoft Power BI untuk pemodelan data, *data cleaning* visual, dan pembuatan dashboard interaktif.
* **Metrik Utama Bisnis:**
    * **Answered Rate:** Persentase panggilan masuk yang berhasil dijawab oleh agen.
    * **Abandonment Rate:** Persentase panggilan yang terputus/dibatalkan sebelum sempat dijawab oleh agen.
    * **Resolve Rate:** Tingkat keberhasilan penyelesaian masalah dari total panggilan yang dijawab.
    * **Average Speed of Answer (S):** Rata-rata durasi waktu tunggu pelanggan (dalam detik) hingga panggilan diangkat oleh agen.
    * **Average Satisfaction Rating:** Nilai rata-rata kepuasan pelanggan setelah panggilan berakhir (skala 1.00 - 5.00).



---

## Eksplorasi & Analisis Dashboard

Dashboard dirancang dalam satu halaman eksekutif interaktif yang menyajikan performa makro operasional sekaligus menyediakan kapabilitas *drill-down* mikro untuk memantau performansi individu dari 8 agen aktif.

### 1. Ringkasan Eksekutif Operasional (Macro Performance)

* **Total Volume Panggilan:** **5.000 panggilan** tercatat masuk dalam kurun waktu 3 bulan.
* **Tingkat Respons (Answered vs Abandoned):** Sebanyak **81,08%** (4.054 panggilan) berhasil dijawab, namun terdapat **18,92%** (946 panggilan) yang tidak terjawab (*abandoned*). Angka kehilangan panggilan hampir 19% ini merupakan sinyal awal penumpukan antrean.
* **Tingkat Penyelesaian Masalah:** Sebesar **72,92%** dari panggilan yang dijawab berhasil diselesaikan (*resolved*) dengan baik oleh tim agen.

### 2. Analisis Akar Masalah Krisis Kepuasan (Root-Cause Analysis)

**Temuan 1: Krisis Kepuasan Bersifat Sistemik (Systemic Issue)**

Rata-rata tingkat kepuasan pelanggan (*Average Satisfaction Rating*) berada di angka **3.40 dari skala 5.00**, tertinggal jauh dari target minimum kualitas perusahaan sebesar **4.50** (ditandai oleh garis indikator target oranye pada *gauge chart*).

Analisis mendalam pada tabel *Agent Performance Metrics* menunjukkan bahwa **tidak ada satu pun agen yang mampu mencapai target KPI 4.50**. Performa kepuasan tertinggi dikunci oleh Martha (**3.47**) dan performa terendah berada di angka **3.33** oleh Joe. Fakta bahwa performa seluruh agen seragam di bawah target membuktikan secara empiris bahwa masalah utama berada pada kendala sistem/operasional makro, bukan kesalahan personal perorangan.

**Temuan 2: Hambatan Waktu Tunggu yang Kritis (Operational Bottlenecks)**

* **Avg. Speed of Answer:** Rata-rata waktu tunggu pelanggan hingga panggilan diangkat mencapai **67,52 detik** (lebih dari 1 menit). Berdasarkan standar industri pelayanan global (*80/20 rule*, di mana 80% telepon idealnya diangkat dalam waktu 20 detik), angka 67 detik menunjukkan antrean yang sangat parah. Pelanggan cenderung sudah frustrasi terlebih dahulu sebelum sempat berbicara dengan agen.
* **Ketidakseimbangan Kapasitas Jam Kerja (Peak Hours):** Melalui grafik *Call Distribution by Hour*, beban panggilan harian terpantau sangat tinggi dan konstan sepanjang pukul 09:00 hingga 17:00 (~500 panggilan per jam). Puncak absolut (*absolute peak*) terjadi tepat pada pukul **13:00** (waktu istirahat). Lonjakan volume panggilan di jam istirahat berisiko besar membenturkan kapasitas staf yang terbatas dengan antrean yang menumpuk.

---

## Rekomendasi Bisnis Strategis

Berdasarkan seluruh temuan berbasis data di atas, berikut adalah 3 rekomendasi utama untuk mengoptimalkan kinerja Call Center:

**1. Mengurangi Waktu Tunggu Melalui Arsitektur IVR (Interactive Voice Response)**

Perusahaan direkomendasikan untuk menerapkan atau memperbarui sistem menu suara otomatis (IVR). Sistem ini akan menyaring, mengkategorikan, atau menyelesaikan masalah-masalah dasar pelanggan secara mandiri sebelum dihubungkan ke manusia, sehingga memangkas beban antrean waktu tunggu reguler yang saat ini bengkak di angka 67,52 detik.

**2. Penjadwalan Staf Fleksibel Berbasis Jam Sibuk (*Shift Optimization*)**

Memanfaatkan data tren waktu dari grafik distribusi panggilan, manajemen wajib mengoptimalkan penataan *shift* kerja agen. Penambahan jumlah staf aktif atau pembagian waktu istirahat yang bergantian secara ketat harus diterapkan pada jam kritis, khususnya pukul **13:00**, guna memangkas *abandonment rate* (18,92%) dan mempercepat respons penanganan.

**3. Audit Standardisasi Solusi (*Knowledge Base Audit*)**

Fakta seragamnya nilai kepuasan agen di angka 3.3 - 3.4 menjadi indikator kuat perlunya pembaruan pada panduan penyelesaian masalah (*script/knowledge base*) internal. Diperlukan audit internal untuk menyederhanakan birokrasi penyelesaian keluhan agar agen memiliki wewenang lebih cepat dalam membantu pelanggan, yang pada akhirnya akan menaikkan tingkat kepuasan umum (*satisfaction rating*).

---

## Kesimpulan

Dashboard *Call Center Performance Optimization* ini berhasil membongkar akar masalah penurunan performa layanan. Evaluasi data menunjukkan adanya hubungan sebab-akibat yang kuat: **Tingginya waktu tunggu panggilan (67,52 detik) di jam-jam sibuk memicu penurunan kepuasan pelanggan secara massal hingga menyentuh angka 3.40.**

Proyek ini membuktikan bahwa visualisasi data operasional yang tepat mampu mengubah baris log panggilan mentah menjadi fondasi keputusan strategis yang tajam bagi pihak manajemen perusahaan.

---

*Project ini merupakan bagian dari PwC Virtual Case Experience — Power BI Job Simulation. Dataset bersifat publik dan digunakan untuk keperluan portofolio dan pembelajaran.*

*Tools: Microsoft Power BI (Data Modeling, DAX, & Data Visualization)*