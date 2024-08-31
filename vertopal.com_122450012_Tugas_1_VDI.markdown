
# Tugas 1 VDI - Resume Artikel

> Judul Artikel : Making data viualization more efficient and effective:
> a survey

> Nama Jurnal : The VLDB Journal

> Volume & Halaman : Vol. 29, halaman 93-117

> Tanggal Publikasi : 19 November 2019

> Penulis : Guoliang Li, Xuedi Qin, Yuyu Luo, Nan Tang

> Penulis Resume : Sesilia Putri Subandi // 122450012


## Abstrak

Visualisasi data berperan penting dalam dunia bisnis yang dipenuhi
banyak data, terutama dalam membantu pengambilan keputusan yang
berkaitan dengan pendapatan utama dari banyak perusahaan bidang
industri. Namun, dikarenakan tingginya permintaan pemrosesan data
berkaitan dengan volume, kecepatan, dan kebenaran data, terdapat
kebutuhan darurat untuk para ahli *database* untuk membantu dalam
efisiensi dan efektifitas dalam visualisasi data. Menanggapi permintaan
ini, artikel ini melakukan survei terhadap metode-metode yang membuat
visualisasi data lebih efektif dan efisien.

1.  Spesifikasi Visualisasi
2.  Pendekatan Efisien dalam Visualisasi Data
3.  Rekomendasi Visualisasi Data


## 1. Pendahuluan

Visualisasi data mengubah data abstrak menjadi bentuk fisik yang dapat
dilihat (seperti panjang, posisi, bentuk, warna, dll) sangat berarti
untuk menampilkan data kepada manusia yang berorientasi visual. Di era
sekarang, semua organisasi memiliki lebih banyak data yang menyebabkan
organisasi tersebut menggunakan data dan analisis tingkat tinggi untuk
membuat strategi dan keputusan operasional.

Komunitas grafik komputer meningkatkan secara signifikan teknologi
visualisasi yang indah dan bisa diinterpretasikan. Komunitas visualisasi
memudahkan pengguna untuk menentukan dan berinteraksi dengan visualisasi
seperti D3, Vega-Lite, VizQL, Tableau, dan Microsoft Power BI.

Visualisasi data juga digunakan banyak aplikasi terkait basis data
seperti Excel, Google Sheets, Oracle Data Visualzation Desktop, IBM DB2,
Amazon Quicksight, Microsoft Power BI, dan masih banyak lagi.

**Alur Visualisasi Data**

1.  Import data
2.  Persiapan data
3.  Manipulasi data
4.  Pemetaan
5.  *Rendering*

Berdasarkan alur tersebut, terdapat tiga aturan yang membuat visualisasi
data lebih efektif dan efisien.

1.  Spesifikasi visualisasi
2.  Pendekatan efisien untuk visualisasi data
3.  Rekomendasi visualisasi data

## 2. Spesifikasi Visualisasi

### 2.1 Spesifikasi dari Visualisasi Data

Secara umum, bahasa visualisasi data terdiri dari 3 bagian yaitu:

1.  Data (*records* dan transformasi)
2.  *Marks* (tipe, ukuran, legenda, keberagaman)
3.  Pemetaan

### 2.2 Kategorisasi Bahasa Visualisasi Data

Strategi dalam mengkategorikan bahasa visualisasi data umumnya
berdasarkan tingkat kemahalannya.

**Bahasa level rendah** merujuk ketika pengguna perlu untuk menentukan
semua elemen pemetaan. Beberapa bahasa level rendah dalam visualisasi
data yaitu Prefuse, Flare, Protovis, D3, Vega, dan Reactive Vega.

**Bahasa level tinggi** merangkum detail dari konstruksi visualisasi,
seperti fungsi pemetaan, maupun beberapa properti untuk penandaan
seperti ukuran kanvas, legenda, dan properti lainnya. Beberapa contoh
visualisasi level tinggi yaitu ggplot2, Vega-Lite, Altair, Echarts,
VizQL, dan ZQL.

### 2.3 Operasi Visual Berbasis GUI

Dibandingkan dengan visualisasi deklaratif, cara yang lebih ramah untuk
pengguna dalam menyediakan spesifikasi adalah dengan mengikuti \"prinsip
manipulasi langsung\", sebuah konsep yang banyak digunakan dalam aspek
interaksi antara manusia dan komputer.

Beberapa contoh alat berbasis GUI antara lain Tableau, Qlik, Excel,
Google Sheets, Amazon QUicksight, Microsoft Power BI, Google Fusion
Tables, iVisDesigner, Lyra, Keshif, dan Data Illustrator.

**Visualisasi Data Interaktif**

Visualisasi data adalah proses eksplorasi, di mana pengguna harus
menghilangkan spesifikasi dari visualisasi yang sedang dieksplor hingga
mendapatkan visualisasi yang mereka inginkan.

Dua kategori dari visualisasi data interaktif, Polaris dan Tableau
menggunakan langkah-langkah *query* untuk menciptakan visualisasi
multidimensi. DeepEye dan Voyager memungkinkan segi eksplorasi dan
membantu pengguna dalam menavigasi visualisasinya dengan mudah.

### 2.4 Spesifikasi yang tidak Ditentukan 

Visualisasi tidaklah berarti jika tidak memberikan *insights* dari data.
Namun, dalam banyak kasus, pengguna tidak begitu mengetahui semua aspek
dari data karena data tersebut mungkin berukuran besar dan rutin
di-*update*. Karena itu, hal ini menimbulkan persyaratan untuk mendukung
spesifikasi yang tidak ditentukan.

Secara umum mengenai spesifikasi yang tidak ditentukan, pengguna hanya
menggunakan beberapa \"petunjuk\", dan menjadi tugas bagi sistem
visualisasi untuk menginterpretasikan masukan yang tidak ditentukan itu
dalam berbagai cara yang mungkin. Jenis \"petunjuk\" pertama yaitu
\"berbasis referensi\", yang kedua yaitu \"berbasis kata kunci\", dan
yang ketiga yaitu \"berbasis bahasa alami\".

## 3. Pendekatan Efisien untuk Visualisasi Data

### 3.1 Visualisasi Data Eksak 

Banyak sistem visualisasi data membaca data dari database. Sistem juga
memanipulasi data dari pernyataan SQL dan kemudian menggunakan alat
visualisasi untuk me-*render* visualisasi.

**Terjemahan query** Cara alami untuk menggunakan kembali banyak sistem
(DBMS) adalah dengan menerjemahkan *query* visualisasi menjadi *query*
yang dapat diterima oleh sistem tersebut.

**Mengintegrsikan Sistem Visualisasi dengan DBMS** Walaupun menggunakan
terjemahan *query* adalah alami, terdapat beberapa kekurangan. Salah
satu masalah utamanya yaitu banyaknya fungsi yang berulang, menghasilkan
teknik optimasi yang tidak terpadu dengan asumsi dan kinerja yang
berbeda di server dan klien, menjadikan pengembang kesulitan untuk
memilih teknik optimasi yang sesuai.

Sebuah cara menjanjikan untuk menyelesaikan permasalahan di atas adalah
dengan mengintegrasikan pengambilan data dan *render* bersamaan untuk
mempercepat proses pembuatan visualisasi.

**Penempatan Kolom** Dalam manajemen data, faktor kunci performa adalah
susunan data, seperti susunan berbasis baris dan berbasis kolom.

**Indeks** Indeks banyak digunakan untuk meningkatkan performa pencarian
yang pada dasarnya mengurangi angka pada baris-baris di tabel yang perlu
diperiksa.

**Prediksi dan Langkah Awal** Seringkali, visualisasi yang sedang
dieksplor terinspirasi dari yang sudah ada sebelumnya. Memprediksi data
yang menarik pengguna dan mengambil langkah awal dari data
menyebabkannya banyak digunakan pada langkah selanjutnya dalam
eksplorasi yang dapat mempercepat proses eksplorasi, dan teknik ini
banyak digunakan di sistem visualisasi.

Terdapat dua kategori prediksi dan *prefetching* yaitu:

1.  Visualisasi yang sedang dieksplor
2.  Data histori

Terdapat dua tahap dalam memprediksi data:

1.  Fase analisis prediksi
2.  Memprediksi petak data

### 3.2 Aproksimasi Visualisasi Data 

Ketika volume data bertambah secara eksponen, pemrosesan data secara
tradisional tidak bisa memenuhi proses interaksi yang cepat. Terdapat 3
perspektif:

1.  Berbasis AQP
2.  Pengambilan sampel berbasis Inkremental
3.  Berbasis Persepsi Manusia

### 3.3 Visualisasi Data Progresif

Banyak pekerjaan dalam aproksimasi visuualisasi data yang menghasilkan
visualisasi progresif kepada pengguna. Selain pengambilan sampel
berbasis inkremental dan visualisasi data progresif, terdapat juga
banyak pekerjaan yang menyediaka visualisasi progresif berdasarkan
agregasi hierarki. Sistem tersebut membangun sebuah struktur hierari
dengan mengagregasi data pada level yang berbeda-beda.

## 4. Rekomendasi Visualisasi

Visualisasi data adalah proses iteratif, dan poin utama dari para
praktisi yaitu bahwa mereka terlibat dalam setiap langkah dalam proses
modifikasi. Mungkin terdapat beberapa solusi rekomendasi visualisasi
yang memudahkan pengguna, dengan merekomendasikan visualisasi yang baik
kepada para pengguna.

### 4.1 Rekomendasi Berdasarkan Spesifikasi

#### 4.1.1 Spesifikasi tidak Lengkap 

Sistem rekomendasi visualisasi dengan ketentuan spesifikasi kosong tanpa
masukan pengguna, sementara sistem rekomendasi dengan sebagian
spesifikasi menerima sebagian masukan elemen spesifikasi visualisasi
dari pengguna.

**Peringkat visualisasi berbasis aturan** Sistem rekomendasi berbasis
aturan memberi peringkat teradap kandidat visualisasi berdasarkan aturan
yang sudah ditentukan sebelumnya, di mana biasanya terdiri dari metrik
efektifitas persepsi manusia, diukur sebagai nilai efektifitas *s*
dengan mempertimbangkan tipe data, informasi statistik, preferensi
visual manusia, dan lain-lain.

**Peringkat visualisasi berbasis pembelajaran mesin** Sistem rekomendasi
berbasis pembelajaran mesin mengoleksi data latih, yang datang dari
sumber atau web, kemudian melatih sebuah model perangkingan yang
mengambil masukan *X* sebagai *list* dari vektor, dan *Y* sebagai
*output*nya.

#### 4.1.2 Spesifikasi berbasis referensi 

Beberapa sistem rekomendasi visualisasi merekomendasikan berdasarkan
referensi data atau referensi visualisasi. Secara khusus, sistem
tersebut merekomendasikan visualisasi yang serupa atau berbeda dari
referensi yang diberikan.

**Berbasis deviasi** merekomendasikan visualisasi berdasarkan deviasi
dengan beberapa referensi visualisasi.

**Berbasis anomali** merekomendasikan visualisasi yang membedakan
anomali paling baik dalam visualisasi utama.

**Berbasis kesamaan/jarak** pengguna menyediakan tren yang diinginkan,
pola, atau *insights*. Pengguna dapat menggambar tren atau pola sebagai
visualisasi *V*, kemudian sistem merekomendasikan visualisasi *V\'*
berdasarkan kesamaannya.

### 4.2 Rekomendasi berbasis perilaku 

Sistem rekomendasi berbasis perilaku menangkap perilaku pengguna sebagai
masukan, kemudian menganggap tugas pengguna dan merekomendasikan
visualisasi yang berguna berdasarkan tugas-tugas tersebut.

### 4.3 Rekomendasi personalisasi

Sistem rekomendasi personalisasi menangkap perilaku historis pengguna
sebagai masukan untuk merekomendasikan personalisasi visualisasi yang
menarik.

## 5. Arah Penelitian Lainnya 

### 5.1 Persiapan data untuk visualisasi data

Nyatanya, data sangatlah kotor, dan memvisualisasikan data kotor
memungkinkan kesalahan pengguna. Fenomena ini sudah diketahui sejak lama
sebagai salah satu tipe visualisasi bias dari komunitas visualisasi
data. Seperti contoh, sebuah dataset terintegrasi dari beberapa sumber
yang memungkinkan terdapat duplikasi. Sebaiknya, data yang
divisualisasikan dibersihkan terlebih dahulu, seperti normalisasi data,
deduplikasi, data kosong, dan deteksi *outlier*.

*Peluang Penelitian*: mendeteksi visualisasi bias dan pembersihan data.

### 5.2 Tolak ukur visualisasi data

Penting untuk mengembangkan tolak ukur untuk performa dan rekomendasi.
Tolak ukur ini harus tepat untuk tugas analisis visual, menyediakan
jejak dan data yang dapat digunakan kembali, dan dalam kasus
rekomendasi, memiliki cakupan yang tinggi dan kulitas dari labelnya.

*Peluang Penelitian*: kategorisasi visualisasi, melatih data.

### 5.3 Visualisasi data untuk aplikasi berbasis *database*

*Peluang Penelitian*: visualisasi data untuk penemuan data, visualisasi
data untuk debug data.

## 6. Kesimpulan 

Visualisasi data adalah bidang yang berkembang pesat dan jumlahnya
sangat banyak hasil penelitian baru dan sistem baru yang dikembangkan
baru-baru ini. Penelitian dan praktisi dari berbagai bidang telah
berkontribusi untuk keberhasilan visualisasi data yang luar biasa, yaitu
didorong oleh sebagian besar (jika tidak semua) domain dan aplikasi.
Seperti disebutkan sebelumnya, sistem visualisasi data komersial bagus
dalam kemudahan penggunaan dalam hal spesifikasi visualisasi data.
Namun, banyak praktisi masih menderita karena efisiensi dan masalah
rekomendasi sistem ini.
