# Proyek Akhir: Menyelesaikan Masalah Institusi Pendidikan
- **Nama:** [Dhimas Sena Rahmantara]
- **Email:** [dhimassr@gmail.com]
- **ID Dicoding:** [dhimassena]

## Business Understanding

### Latar Belakang Bisnis
Jaya Jaya Institut merupakan salah satu institusi pendidikan perguruan yang telah berdiri sejak tahun 2000. Hingga saat ini ia telah mencetak banyak lulusan dengan reputasi yang sangat baik. Akan tetapi, terdapat banyak juga siswa yang tidak menyelesaikan pendidikannya alias dropout.

Jumlah dropout yang tinggi ini tentunya menjadi salah satu masalah yang besar untuk sebuah institusi pendidikan. Oleh karena itu, Jaya Jaya Institut ingin mendeteksi secepat mungkin siswa yang mungkin akan melakukan dropout sehingga dapat diberi bimbingan khusus.

### Permasalahan Bisnis
Beberapa permasalahan bisnis yang akan coba diselesaikan adalah sebagai berikut.
1. Apa saja faktor yang menyebabkan siswa dropout?
2. Apakah course tertentu berpengaruh kepada tingkat dropout siswa?
3. Apakah tingkat dropout pada siswa penerima beasiswa lebih rendah daripada siswa yang bukan?
4. Bagaimana perbandingan dropout siswa laki-laki dan perempuan?
5. Apakah ada cara untuk mendeteksi siswa yang akan dropout?

### Cakupan Proyek
Pengerjaan proyek ini mencakup beberapa hal, diantaranya:
1. **Melakukan Exploratory Data Analysis (EDA)** terhadap data siswa yang diberikan. Hal tersebut dilakukan agar mendapatkan insight mengenai pola siswa dropout yang terjadi pada Jaya Jaya Institut.
2. **Membuat Model Machine Learning** untuk membantu pihak istitusi mendeteksi siswa dengan kemungkinan dropout.
3. **Membuat Visualisasi Dashboard** agar dapat menampilkan kondisi terkini yang terjadi pada siswa Jaya Jaya Institut.

### Persiapan
**Sumber Data**
Dataset yang dipakai adalah [Dataset Karyawan Jaya Jaya Insitut] (https://raw.githubusercontent.com/dicodingacademy/dicoding_dataset/refs/heads/main/students_performance/data.csv)

**Setup Environment**
Visualisasi Dashboard HR Jaya Jaya Maju dapat dijalan dengan langkah-langkah berikut.
1. Menjalankan `submission_Institusi_Pendidikan.ipynb`
   - Lihat file `requirements.txt` untuk melihat dependensi yang dibutuhkan.
   - Jalankan seluruh isi file `submission_Institusi_Pendidikan.ipynb` menggunakan Google Colab / Jupyter Notebook.
2. **Menjalankan Dashboard**:
   Pastikan sudah menginstal Docker pada komputer. Lalu ikuti langkah-langkah di bawah ini:
   - Jalankan perintah berikut
      ```
      docker pull metabase/metabase:latest
      ```
   - Jalankan container metabase menggunakan perintah
      ```
      docker run -p 3000:3000 --name eduedu metabase/metabase
      ```
   - Login ke Metabase menggunakan username dan password berikut:
      ```
      username: root@mail.com
      password: root123
      ```
---

## Business Dashboard
Hasil visualisasi dashboard yang telah dikerjakan dapat menunjukkan kondisi siswa Jaya Jaya Institut secara real-time. Mulai dari kondisi jumlah siswa, perbandingan jumlah siswa yang dropout dengan siswa keseluruhan, hingga prediksi dropout dengan probabilitasnya jika akan dropout.

### Tutorial Mengakses Dashboard
**Menggunakan Metabase**
1. Buka metabase di browser dengan menggunakan Docker
2. Username dan Password untuk masuk ke Metabase dengan username:`root@mail.com`, password: `root123`

### Tutorial Mengakses Prototype
**Menggunakan Streamlit**
1. Buka browser dan buka link streamlit berikut ini:
```
https://edu-edu.streamlit.app/
```
2. Inputan nilai sesuai dengan field isian
3. Klik `Prediksi` untuk melihat hasil prediksi

## Conclusion
Proyek ini berhasil menjawab beberapa pertanyaan bisnis seputar masalah dropout siswa yang terjadi di Jaya Jaya Institut. Berikut ini adalah penjelasannya.
1. Apa saja faktor yang menyebabkan siswa dropout?
* Dari analisis dan prediksi yang dilakukan beberapa faktor yang menyebabkan siswa Dropout antara lain; **age_at_enrollment**, **previous_qualification_grade**, jumlah atau unit kegiatan kurikuler baik di semester 1 dan juga semester 2 **(approved, evaluation, grade)**, dan juga **gdp** siswa tersebut.

2. Apakah course tertentu berpengaruh kepada tingkat dropout siswa?
* Semua course yang ada di Jaya Jaya Institut memiliki siswa yang Dropout. Dari 17 jumlah keseluruhan course, hanya course **Oral Hygiene** dan **Biofuel Production Technologies** yang memiliki siswa Dropout masing-masing sebanyak **8 siswa** dan **33 siswa**. Course lainnya memiliki lebih dari **50 siswa** yang Dropout.

3. Apakah tingkat dropout pada siswa penerima beasiswa lebih rendah daripada siswa yang bukan?
* Perbandingan antara siswa peneriman beasiswa dengan yang bukan penerima beasiswa adalah 1099 siswa berbanding 3325 siswa. Untuk siswa **bukan peneriman beasiswa** terdapat **1287 siswa** yang Dropout atau sebesar **38.7%**. Sedangkan siswa Dropout yang mereka adalah penerima beasiswa berjumlah **134 siswa** atau sebesar **12.2%**. Hal ini menunjukan persentase siswa Dropout bukan penerima beasiswa lebih besar dariapda siswa Dropout penerima beasiswa.

4. Bagaimana perbandingan dropout siswa laki-laki dan perempuan?
* Secara persentase keseluruhan, perbandingan banyak siswa laki-laki dan perempuan adalah **1556 siswa (35.17%)** berbanding **2868 siswa (64.83%)**. Sedangkan secara jumlah per kelompok gender, siswa laki-laki yang Dropout adalah **701 siswa** dari 1556 siswa atau **45%** dan siswa perempuan yang Dropout ada sebanyak **720 siswa** dari 2868 atau **25.1%**. Sehingga walaupun secara jumlah siswa yang Dropout, jumlah siswa perempuan lebih banyak, namun secara persentase siswa laki-laki yang Dropout lebih besar.

5. Apakah ada cara untuk mendeteksi siswa yang akan dropout?
* Hal tersebut adalah dengan melakukan klasifikasi dan prediksi siswa dengan menggunakan model machine learning serta membuat visualisasi dashboard siswa yang langsung dapat dipantau oleh pihak Jaya Jaya Institut. Dimana dalam melakukan klasifikasi dan prediksi, model machine learning yang dikembangkan memiliki akurasi tertinggi sebesar **78.66%** dengan menggunakan algoritma **Random Forest**.

### Rekomendasi Action Items untuk Perusahaan
Berikut ini beberapa aksi / langkah yang dapat diambil Perusahaan Jaya Jaya Institut untuk menekan tingkat droout yang terjadi.
1. Memberikan bimbingan khusus kepada siswa, terlebih kepada siswa yang diprediksi akan dropout apalagi menjelang akan diadakannya ujian. Karena faktor admission grade yang diraih siswa sangat berpengaruh kepada tingkat dropout siswa.
2. Memberikan pelatihan kepada pengajar mengenai cara-cara menyampaikan course yang lebih menarik kepada siswa agar materi yang diajarkan dapat lebih dipahami oleh siswa. Apalagi dilihat dari beberapa course yang menyumbangkan angka droput cukup tinggi bagi Jaya Jaya Institut.
3. Mengadakan program temu alumni yang telah bekerja atau mendatangkan expertise agar siswa yang masih belajar di Jaya Jaya Insitut mendapatkan motivasi bahwa ilmu yang mereka miliki memang akan dipakai dan berguna di dunia kerja dan industri.
4. Memberikan lebih banyak beasiswa karena dilihat dari analisis yang dilakukan, siswa penerima beasiswa lebih banyak yang bertahan belajar di Jaya Jaya Institut daripada yang bukan penerima beasiswa. Bisa jadi ini adalah motivasi untuk mereka agar tetap dan terus belajar di Jaya Jaya Institut.
