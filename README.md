# Capstone-Project-Modul-3
Capstone Project Modul 3 - Hotel booking Cancellation

## Business Problem Understanding
**Context** 

Kita merupakan Data Scientist yang baru direkrut oleh perusahaan Hotel bintang 5. Tanggung jawab kita adalah untuk memprediksi kecenderungan pelanggan yang akan membatalkan pemesanan mereka di hotel kita atau tidak melalui fitur-fitur tertentu. Sebelum menunjuk kita sebagai Data Science, Hotel sering mengalami kerugian pendapatan karena pelanggan tiba-tiba membatalkan pemesanan kamar mereka sehingga kamar menjadi kosong dan tidak dapat ditempati oleh pelanggan lain.

**Problem Statement :**

Pembatalan dapat berdampak buruk pada hotel. Hilangnya pendapatan terjadi sebagai akibat dari kamar yang tidak terjual. No-show adalah pembatalan tanpa pemberitahuan. 

Ketika sebuah hotel dihadapkan dengan pembatalan menit terakhir dan kemudian check-in menit terakhir, hotel tidak bisa berbuat banyak selain menjual kamar dengan harga yang jauh lebih rendah, jadi peluang untuk mendapatkan revenue yang maksimal sangat minim.

Dan kemudian, ada juga biaya penggunaan layanan Online Travel Agent (OTA) untuk check-in menit terakhir. Hotel harus membayar biaya tertentu kepada OTA karena OTA bertindak sebagai perantara mereka, sehingga menurunkan keuntungan.

Tetapi jika hotel tidak bergantung pada OTA atau tidak memiliki unduhan otomatis pemesanan dan pembatalan, maka waktu pemesanan dan pembatalan tinggi, dan lebih banyak waktu berarti biaya lebih tinggi.

**Goals :**

Bagaimana kita dapat memprediksi dan meminimalkan pembatalan pemesanan kamar oleh pelanggan sehingga hotel bisa mendapatkan keuntungan yang maksimal dan pendapatan tambahan dari Makanan dan Minuman dari pelanggan yang menginap di hotel, serta meningkatkan demand agar kamar hotel dapat terisi semua.

**Analytic Approach :**

Kita akan menganalisis faktor apa saja yang mempengaruhi pembatalan pemesanan kamar hotel dan menentukan pola pelanggan yang akan membatalkan pemesanan atau tidak. 

Lalu kita akan coba untuk membangun model klasifikasi yang akan membantu perusahaan untuk dapat memprediksi probabilitas pelanggan yang akan membatalkan pesanannya atau tidak

**Metric Evaluation**

1. True-Positive : Kita memperkirakan bahwa pelanggan akan membatalkan pemesanan mereka dan ternyata benar mereka membatalkan pemesanannya
Konsekuensi: Kita dapat memaksimalkan keuntungan kita dengan mengisi kamar kita sepenuhnya, serta mendapatkan keuntungan tambahan dari layanan F&B.

2. False-Negative : Kita memperkirakan bahwa pelanggan tidak akan membatalkan pemesanan mereka dan ternyata mereka membatalkan pemesanan mereka
Konsekuensi: Kamar yang dibatalkan pelanggan akan tetap kosong dan hotel akan kehilangan keuntungan di kamar ini, sementara sebenarnya kita dapat mengisinya dengan pelanggan lain.

3. False Positive : Kita memperkirakan bahwa pelanggan akan membatalkan pemesanan mereka dan sebenarnya mereka tidak membatalkan pemesanan mereka
Konsekuensi: Kita akan kehilangan pelanggan, tetapi jika hotel kita demandnya tinggi seharusnya tidak ada beban pada profitabilitas hotel karena tidak ada kamar hotel yang kosong sebagai akibat dari kasus ini.

4. True-Negative : Kita memperkirakan bahwa pelanggan tidak akan membatalkan pemesanan mereka dan sebenarnya mereka tidak membatalkan pemesanan mereka
Konsekuensi: Mayoritas karakteristik pelanggan yang memesan kamar hotel.

MODELLING USING KNN
Teknik ini memberikan hasil prediksi berdasarkan kelas mayoritas dari beberapa pengamatan serupa atau 'tetangga' terdekat. Meskipun cukup sederhana dan tidak menghasilkan Model, KNN dapat memberikan akurasi yang memadai dibandingkan dengan metode lain, kelemahannya adalah KNN tidak cukup praktis di sebagian besar kasus dan membutuhkan memori yang besar. KNN bersifat non parametrik, artinya tidak menghasilkan persamaan seperti Linear Regression atau Logistic Regression.

Dalam algoritma KNN, ada beberapa parameter yang akan diatur. Dibutuhkan titik, menemukan titik K-terdekat, dan memprediksi label untuk titik itu.

1. Yang pertama adalah jumlah K (contoh) yang paling dekat dengan query. Memilih K yang tepat untuk data kita dilakukan dengan mencoba beberapa K dan memilih salah satu yang paling sesuai. Oleh karena itu, memilih rentang nilai K adalah praktik terbaik daripada mencoba angka yang berbeda secara manual sebagai K.
2. Weights
    - Uniform : algoritma akan mengklasifikasikan nilai berdasarkan jumlah total nilai yang sama pada titik-titik data. Jumlah terbesar dari nilai serupa dalam kedekatan, prediksi akan dibuat untuk nilai itu.
    - Distance : algoritma yang memberikan bobot jarak dari suatu nilai ke nilai yang mirip pada jarak tersebut. Semakin dekat nilai yang mirip dengan nilai sebenarnya, algoritma akan memberikan bobot lebih pada koneksi. Oleh karena itu, jumlah total nilai yang mirip dalam kedekatan tidak selalu diterjemahkan ke dalam kelas prediksi, melainkan seberapa dekat mereka dengan nilai prediksi.
3. Power Parameter
    - p=1 : manhattan_distance (l1)
    - p=2 : euliddean_distance(l2)
    - arbitrer p : jarak minkowski (l_p)


#### RECOMMENDATION & IMPROVEMENT

1. Sebaiknya cancellation policy hotel bisa lebih di perketat lagi agar para customer tidak seenaknya untuk melakukan pembatalan.
2. Jika ada pelanggan yang membatalkan pemesanan kamar, sebaiknya pihak hotel langsung follow up ke pelanggan lain bahwa ada kamar kosong yang bisa di pesan agar perusahaan tidak kehilangan pendapatan.
3. Pihak perusahaan juga dapat melakukan diskon terhadap kamar tertentu karena para pelanggan pasti cenderung memilih kamar yang termurah
4. Menambahkan kolom price per room agar kita bisa mengetahui tipe room apa aja yang paling banyak di cancel agar kita bisa menyusun strategi bisnis dan marketing yang baik
5. Kebijakan seperti apa yang perusahaan gunakan agar kita bisa menganalisa lebih lanjut mengenai turun naiknya revenue perusahaan
6. Tidak disarankan untuk menggunakan Machine Learning ini jika demand terhadap hotel rendah, dikarenakan nanti kita akan cenderung menolak pelanggan yang berpotensial untuk menginap.








