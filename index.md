# Statistik Deskriptif

## Pengertian

> **Statistik deskriptif** adalah metode-metode yang berkaitan dengan pengumpulan dan Penyajian suatu gugus data sehingga memberikan informasi yang berguna.

Statistik Deskriptif memberikan ringkasan sederhana tentang sempel dan pengamatan yang telah dilakukan. Ringkasan tersebut bisa berisi kuantitatif, ialah : Statistik yang terlihat dengan rapi dan ringkas bisa berupa tabel, diagram, atau grafik yang bisa memberikan informasi inti dari kumpulan data yang ada dengan mudah untuk dimengerti.

## Tipe Statisktik Deskriptif

### **Mean (rata-rata)**

Mean adalah rata-rata dari sekumpulan beberapa data angka. Mean diperoleh dari hasil penjumlahan seluruh angka yang dibagi dengan banyaknya angka itu sendiri. Jika kita memiliki N angka, kita bisa menghitung mean itu dengan rumus berikut :



Dimana :

x bar = x rata-rata = nilai rata-rata sampel

x = data ke n

n = banyaknya data

### **Median**

Median merupakan nilai tengah dari sebuah urutan data angka. Median disimbolkan dengan *Me*. Nilai dari median akan sama dengan Quartile 2 (Q2). Dalam mencari median, banyak (n) dari data ganjil dan genap memiliki cara perhitungan yang berbeda. Kita dapat menggunakan rumus sebagai berikut :



Dimana :

Me = Median dari kelompok data

n = banyak data



### **Modus**

Modus adalah angka yang paling sering muncul dalam sekumpulan data angka. Modus didapat dengan mengumpulkan dan mengatur data untuk menghitung setiap frekuensi dari setiap hasil, dan hasil yang memiliki jumlah tertinggi bisa kita sebut modus dari kumpulan data angka tersebut. Untuk mencari modus kita dapat menggunakan rumus berikut :



Dimana :

Mo = modus dari kelompok data

Tb = tepi bawah dari elemen modus

b1 = selisih frekuensi antara elemen modus dengan elemen sebelumnya

b2 = selisih frekuensi antara elemen modus dengan elemen sesudahnya

p = panjang interval

Nb. Nilai b1 dan b2 adalah mutlak (positif)

### **Varians**

Varian adalah ukuran penyebab setiap nilai dalam suatu himpunan data dari rata-rata. Terdapat langkah yang harus dilakukan untuk mendapatkan varians, yaitu : dengan mengambil ukuran jarak dari setiap nilai dan mengurangi rata-rata dari setiap nilai dalam data, lalu hasil dari jarak tersebut dikuadratkan dan membagi jumlah kuadrat dengan jumlah niali dalam himpunan data. Untuk menghitung varian kita dapat menggunakan rumus berikut :



Dimana :

xi = titik data

x bar = rata-rata dari semua titik data

n = banyak dari anggota data

### **Standar Deviasi**

Standar deviasi merupakan ukuran dispersi kumpulan data relatif terhadap rata-rata atau  bisa disebut kuadrat positif dari varian. Standar deviasi dihitung dengan mengakar kuadratkan nilai dari varians, jika titik data lebih dari rata-rata data maka, semakin tinggi standar deviasi. Untuk mencari standar deviasi kita bisa menggunakan rumus berikut :



### **Skewness**

Skewness (*kemiringan*) adalah ketidaksimetrisan pada suatu distribusi statistik dimana kurva tampak condong ke kiri atau kanan. Skewness digunakan untuk menentukan sejauh mana perbedaan suatu distribusi dengan distribusi normal. Dalam distribusi normal grafik muncul seperti kurva lonceng. Ketika suatu distribusi mengalami kemiringan ke sebelah kanan dan ekor di sisi kanan kurva lebih panjang dari ekor di sisi kiri kurva maka situasi ini dikatakan kemiringan negatif. Skewness bisa dihitung menggunakan rumus berikut :



Dimana :

xi = titik data

x bar = rata-rata dari distribusi

n = jumlah titik dalam distribusi

o = standar deviasi

### **Quartile**

Quartile adalah irisan nilai dari hasil pembagian data menjadi empat bagian yang sama besar. Nilai-nilai dari quartile biasanya dilambangkan dengan Q1 untuk quartile bawah. Q1 ini mempunyai nilai 25% dari data. Q2 atau disebut quartile tengah yang mempunyai nilai sama seperti median yaitu 50% dari data. dan Q3 sebagai quartile atas mempunyai nilai 75% dari data. Dalam mencari quartile kita dapat menggunakn rumus :



Dimana :

Q  = nilai dari Quartile

n = banyak data

## **Penerapan Statistik Deskriptif  Menggunaka Python **

### **Alat dan Bahan**

Sebelum menerapkan ini sebelumnya saya sudah menyiapkan 500 data acak dalam bentuk .csv untuk mempermudah dalam penerapan tersebut, perlu disiapkan library python yang dapat didownload secara gratis.

dalam kasus ini, library python yang digunakan adalah sebagai berikut :

1.Pandas, digunakan untuk data manajemen dan data analysis

2.scipy, merupakan library berisi kumpulan algoritma dan  fungsi matematika.

### **Pertama**

pada langkah ini kita memasukkan librabry yang telah disiapkan sebelumnya

```python
import pandas as pd
from scipy import stats
```

### **Kedua**

Membuat data csv yang telah disiapkan

```python
data = pd.read_csv("dataexcel.csv",delimiter=",")
```

### **Ketiga**

Kemudian membuat code untuk memproses data yang akan diambil pada kolom csv yang telah dibuat, berikut code yang bisa digunakan 

```python
for x in colum :
    ds = [x for x in data[x]]
    desc = data[x].describe()
    array = [x for x in desc]
    print ("Detail Kolom ", x)
    print ("Rata-Rata ", array[1])
    print ("Median ", np.median(np.array(ds)))
    print ("Modus : ", stats.mode(ds))
    print ("Standard Deviasi : ", np.std(ds))
    print ("Varian : ", stats.variation(ds))
    print ("Skewness : ", stats.skew(ds))
    print ("Quartil 1 : ", array[4])
    print ("Quartil 2 : ", array[5])
    print ("Quartil 3 : ", array[6])
    sns.distplot(data[x])
    
    print ("\n")
```

Setelah dijalankan, program tersebut akan menampilkan seperti berikut :

|      |    **Stats**    | **X1** | **X2** | **X3** | **X4** | **X5** |
| :--: | :-------------: | :----: | :----: | :----: | :----: | :----: |
|  1   |      Mean       | 59.12  | 58.71  | 61.81  | 60.05  | 58.52  |
|  2   |     Median      |   57   |   60   |   66   |   60   |   58   |
|  3   |      Modus      |   53   |   61   |   66   |   48   |   42   |
|  4   | Standar Deviasi | 16.76  | 18.74  | 17.31  | 17.44  | 17.07  |
|  5   |     Varian      |  0.28  |  0.31  |  0.28  |  0.29  |  0.29  |
|  6   |    Skewness     |  0.08  |  0.10  | -0.06  |  0.06  |  0.07  |
|  7   |   Quartile 1    |  46.5  |  42.5  |  45.5  |  44.5  |   42   |
|  8   |   Quartile 2    |  57.0  |   60   |   66   |   60   |   58   |
|  9   |   Quartile 3    |  73.0  |  77.5  |   76   |   76   |   74   |
