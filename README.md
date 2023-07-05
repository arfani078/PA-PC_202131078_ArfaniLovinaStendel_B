

# Mendeteksi Warna Pada Buah

### Cara Kerja
Praktikum terlampir di file Project UAS_ArfaniLovinaStendel-202131078.ipynb
dengaN image buah.jpg

### Library yang digunakan :
1. import cv2 : sebuah pustaka populer yang digunakan untuk pengolahan gambar dan analisis komputer.
2. import numpy as np : pustaka populer yang digunakan untuk komputasi numerik dan manipulasi array multidimensi.
3. import matplotlib.pyplot as plt : pustaka yang digunakan untuk membuat visualisasi grafis dalam Python.

#### Penjelasan cara Menampilkan hasil deteksi buah 

1. Mendeteksi warna buah: 
- Pernyataan plt.subplot(141) digunakan untuk membuat subplot dalam sebuah gambar. Dalam hal ini, angka 141 menunjukkan bahwa gambar akan dibagi menjadi 1 baris dan 4 kolom, dan subplot pertama akan dipilih sebagai area plot berikutnya.
- Pernyataan plt.imshow(adjusted_red) digunakan untuk menampilkan gambar adjusted_red di dalam subplot yang dipilih sebelumnya. Fungsi imshow() dari modul pyplot digunakan untuk menampilkan gambar atau array sebagai citra.
- Pernyataan plt.axis('off') digunakan untuk menghilangkan sumbu koordinat pada plot. Dalam hal ini, sumbu akan dinonaktifkan sehingga tidak ditampilkan pada gambar.
- Pernyataan plt.title('Deteksi Buah Merah') digunakan untuk memberikan judul pada subplot yang ditampilkan. Judul ini akan muncul di atas gambar.
Secara keseluruhan, pernyataan tersebut mengatur subplot, menampilkan gambar adjusted_red, menghilangkan sumbu koordinat, dan memberikan judul "Deteksi Buah Merah" pada subplot tersebut.

2. Mendeteksi semua buah :
- Pernyataan plt.tight_layout() digunakan untuk mengoptimalkan tata letak plot agar lebih rapi dan memastikan bahwa elemen-elemen di dalam plot tidak tumpang tindih atau terpotong. Fungsi tight_layout() dari modul pyplot secara otomatis mengatur jarak antara elemen-elemen plot seperti sumbu, judul, dan label, sehingga plot terlihat lebih teratur.
- Pernyataan plt.show() digunakan untuk menampilkan plot ke layar. Fungsi show() dari modul pyplot akan menampilkan semua plot yang sudah didefinisikan sebelumnya.
Dalam kombinasi, pernyataan plt.tight_layout() diikuti oleh plt.show() akan mengoptimalkan tata letak plot dan kemudian menampilkannya ke layar sehingga kita dapat melihat plot dengan tata letak yang rapi.

3. Proses deteksi buah berdasarkan warna:
- Pada pernyataan mask_red = cv2.inRange(image, lower_red, upper_red), kita menggunakan cv2.inRange() untuk membuat masker yang akan menandai piksel-piksel dalam image yang berada dalam kisaran warna lower_red dan upper_red. Dengan kata lain, masker mask_red akan memberikan nilai 255 pada piksel yang berada dalam kisaran warna merah, dan nilai 0 pada piksel lainnya.
- Pada pernyataan mask_yellow = cv2.inRange(image, lower_yellow, upper_yellow), kita menggunakan cv2.inRange() untuk membuat masker yang akan menandai piksel-piksel dalam image yang berada dalam kisaran warna lower_yellow dan upper_yellow. Dengan kata lain, masker mask_yellow akan memberikan nilai 255 pada piksel yang berada dalam kisaran warna kuning, dan nilai 0 pada piksel lainnya.
- Pada pernyataan mask_green = cv2.inRange(image, lower_green, upper_green), kita menggunakan cv2.inRange() untuk membuat masker yang akan menandai piksel-piksel dalam image yang berada dalam kisaran warna lower_green dan upper_green. Dengan kata lain, masker mask_green akan memberikan nilai 255 pada piksel yang berada dalam kisaran warna hijau, dan nilai 0 pada piksel lainnya.
Dengan cara ini, dapat menggunakannya untuk mengidentifikasi dan mengisolasi piksel-piksel tertentu dalam gambar berdasarkan kisaran warna yang diinginkan.

4. Definisi range warna untuk deteksi buah:
- Pada bagian lower_red = np.array([0, 0, 100]) dan upper_red = np.array([100, 100, 255]), mendefinisikan batas bawah dan batas atas untuk kisaran warna merah dalam format RGB. Dalam hal ini, nilai-nilai piksel dengan komponen merah antara 0 dan 100, komponen hijau antara 0 dan 100, serta komponen biru antara 100 dan 255 akan masuk ke dalam kisaran warna merah.
- Pada bagian lower_yellow = np.array([0, 100, 100]) dan upper_yellow = np.array([100, 255, 255]), mendefinisikan batas bawah dan batas atas untuk kisaran warna kuning dalam format RGB. Dalam hal ini, nilai-nilai piksel dengan komponen merah antara 0 dan 100, komponen hijau antara 100 dan 255, serta komponen biru antara 100 dan 255 akan masuk ke dalam kisaran warna kuning.
- Pada bagian lower_green = np.array([0, 100, 0]) dan upper_green = np.array([100, 255, 100]), mendefinisikan batas bawah dan batas atas untuk kisaran warna hijau dalam format RGB. Dalam hal ini, nilai-nilai piksel dengan komponen merah antara 0 dan 100, komponen hijau antara 100 dan 255, serta komponen biru antara 0 dan 100 akan masuk ke dalam kisaran warna hijau.
Dengan menggunakan nilai-nilai batas ini, dapat menggunakan fungsi cv2.inRange() untuk membuat (mask) yang akan mengidentifikasi piksel-piksel dalam gambar yang berada dalam kisaran warna yang diinginkan.





