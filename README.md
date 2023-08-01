# Mini Project 3 - Predict Customer Personality to boost marketing campaign by using Machine Learning
Sebagai seorang Data Scientist pada sebuah perusahaan sebagai Tim inti Data Science, bertanggung jawab untuk mengolah data historical marketing campaign guna menaikkan performa dan menyasar customer yang tepat agar dapat bertransaksi di platform perusahaan.

## Ringkasan
Sebuah perusahaan dapat berkembang dengan pesat saat mengetahui perilaku customer personality nya, sehingga dapat memberikan layanan serta manfaat lebih baik kepada customers yang berpotensi menjadi loyal customers. Dengan mengolah data historical marketing campaign guna menaikkan performa dan menyasar customers yang tepat agar dapat bertransaksi di platform perusahaan, dari insight data tersebut fokus kita adalah membuat sebuah model prediksi kluster sehingga memudahkan perusahaan dalam membuat keputusan.

### 1. Conversion Rate Analysis Based On Income, Spending And Age
Analisis conversion rate adalah suatu pencarian insight data persentase pengunjung website serta tindakan yang mereka lakukan selama mengunjungi website, dan apakah tindakan mereka akan menghasilkan transaksi pembelian atau tidak selama berkunjung di website tersebut. Hal ini dapat dilakukan dengan melakukan feature engineering pada variable data yang ada, sehingga dapat menghasilkan satu kolom baru yaitu Conversion rate. Setelah Conversion rate terbentuk, maka dapat dianalisis dengan variabel lain seperti umur, penghasilan, pengeluaran, dll. sehingga dapat menemukan suatu pola perilaku konsumen.

### Hubungan Antara Umur Customer dengan Conversion Rate Dari Sebuah Marketing Campaign
![image](https://github.com/hadasadida/Mini-Project-3-Predict-Customer-Personality-to-boost-marketing-campaign-by-using-Machine-Learning/assets/124650679/538af0b3-af94-48cf-bee8-bc0be48695f6)
Berdasarkan plot, umur customer dengan conversation rate tidak memiliki hubungan yang signifikan. Sehingga dapat disimpulkan umur customer tidak berdampak terhadap conversion rate.

### Hubungan Antara Income dengan Total Spent 
![image](https://github.com/hadasadida/Mini-Project-3-Predict-Customer-Personality-to-boost-marketing-campaign-by-using-Machine-Learning/assets/124650679/ed6e0e20-0d18-4170-868c-36746a3e6904)
Berdasarkan plot, income customer berdampak terhadap total spent. Semakin besar income, semakin besar pula total spent yang dikeluarkan. 

### 2. Data Cleaning & Preprocessing
Dilakukan data preprocessing, yakni menangani berbagai permasalahan data seperti data yang kosong, data yang tidak sesuai, hingga mengidentifikasi data-data yang tidak dibutuhkan.

#### 1) Data Null
Pada kolom Income terdapat data null sebanyak 24 baris, karena jumlahnya sedikit maka dilakukan drop data null.
#### 2) Data Duplicate
Tidak ada data duplikat.
#### 3) Feature Encoding 
Dilakukan feature encoding pada kolom education, marital status dan age group.
#### 4) Standarisasi Feature
Dilakukan standarisasi pada kategori feature numerical.

### 3. Data Modeling
Data yang sudah di-cleaning pada tahap sebelumnya akan digunakan untuk pemodelan data dengan melakukan task clustering. Pada tahap ini 
akan menerapkan algoritma k-means clustering pada dataset yang ada, kemudian memilih jumlah cluster yang tepat dengan melihat dari elbow method, dan melakukan evaluasi dengan menggunakan silhouette score.

### Elbow Method 
![image](https://github.com/hadasadida/Mini-Project-3-Predict-Customer-Personality-to-boost-marketing-campaign-by-using-Machine-Learning/assets/124650679/31fe9f2a-f8f3-4f9e-a772-e2a0dc250624)
### Silhouette Score  
![image](https://github.com/hadasadida/Mini-Project-3-Predict-Customer-Personality-to-boost-marketing-campaign-by-using-Machine-Learning/assets/124650679/9a5b6846-161b-4438-9d4e-640a83d19ea3)
Berdasarkan elbow method, didapatkan jumlah cluster = 4. Jumlah tersebut cukup untuk memisahkan masing-masing cluster dengan jarak yang paling optimal. 

### 4. Customer Personality Analysis For Marketing Retargeting
1) Cluster 0
   - Memiliki jumlah customer sebanyak 602.
   - Memiliki income rata-rata 33723680, paling rendah diantara cluster lainnya.
   - Rata-rata memiliki anak-anak.
   - Frekuensi rata-rata dalam pembelian produk sangat rendah.
   - Conversion rate rata-rata paling rendah.
   - Umur rata-rata 51 tahun.
2) Cluster 1
   - Memiliki jumlah customer sebanyak 564.
   - Memiliki income rata-rata 68465310.
   - Rata-rata memiliki anak remaja.
   - Frekuensi rata-rata dalam pembelian produk sedang.
   - Conversion rate rata-rata sedang.
   - Umur rata-rata 56 tahun.
3) Cluster 2
   - Memiliki jumlah customer sebanyak 137, paling rendah diantara cluster lainnya.
   - Memiliki income rata-rata 59141540.
   - Rata-rata memiliki anak remaja.
   - Frekuensi rata-rata dalam pembelian produk rendah.
   - Conversion rate rata-rata rendah.
   - Umur rata-rata 55 tahun.
4) Cluster 3
   - Memiliki jumlah customer sebanyak 913, paling tinggi diantara cluster lainnya.
   - Memiliki income rata-rata 78631740, paling tinggi diantara cluster lainnya.
   - Rata-rata tidak memiliki anak.
   - Frekuensi rata-rata dalam pembelian produk tinggi-sedang.
   - Conversion rate rata-rata tinggi.
   - Umur rata-rata 56 tahun.
