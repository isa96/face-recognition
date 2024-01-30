# Project 1 : Face Recognition
Face Recognition merupakan Project dalam menyelesaikan Bootcamp Computer Vision Specialist.

#### Author : Teguh Prasetyo

## Pendahuluan
Teknologi Artificial Intelligence (AI) dewasa ini sangat bermanfaat bagi masyarakat. Salah satu bidang AI yang banyak diaplikasikan dalam kehidupan 
sehari-hari yaitu Computer Vision, dimana computer dilatih untuk dapat mengenali image (citra). Misalnya Face Recognition, dimana computer dilatih 
untuk dapat membedakan wajah laki-laki atau perempuan, atau lebih jauh lagi dapat mengenali nama seseorang dari wajahnya. 
Face Recognition ini sangat bermanfaat dalam kehidupan sehari-hari, misalnya untuk absensi kehadiran di suatu kantor, untuk tujuan authentifikasi pemilik akun/ID dan 
lain-lain seperti pada foto di bawah ini.



## Objektif

Project ini bertujuan untuk melakukan eksperimen dengan 3 algoritma Deep Learning populer yaitu VGG, GoogleNet dan ResNet dan 
mengoptimalkan penggunaannya dengan melakukan hyperparameter tuning. Kemudian dari hasil eksperimen tersebut akan dilakukan pengambilan kesimpulan algoritma terbaik.

## Dataset

Image dataset yang digunakan dalam project ini terdiri dari 5000 images (terdapat 17 image duplikat). List nama file dari setiap image yang digunakan dapat 
dilihat pada file dengan nama  `List Nama File Foto sebagai Dataset.csv`, untuk mendapat file image tersebut dapat mendownload dari 
[CelebA](https://mmlab.ie.cuhk.edu.hk/projects/CelebA.html) di Kaggle, kemudian filter image sesuai List nama file yang ada pada file CSV tersebut. 
Untuk menentukan kategori Gender Male atau Female dapat menggunakan file `list_attribute.csv` pada kolom *image_id* dan kolom *Male*, 
kemudian lakukan *Join Inner* pada kolom *image_id* antara file *List Nama File Foto sebagai Dataset.csv* dengan *list_attribute.csv*, sehingga diperoleh 5000 baris data 
yang sama dengan dataset Image.  

## Metodologi

Training model deep learning menggunakan library keras dan tensorflow. Lebih detail dapat dilihat pada notebook.

Dalam proses penyelesaian tugas eksperimen dibuat bertahap, sehingga tahapannya membuat eksperimen dengan VGG-19 dahulu melalui eksperimen 1, 2 dan 3. 
Hasil terbaik dari eksperimen dengan VGG-19 tersebut kemudian di gunakan Model parameternya untuk pengerjaan dengan algoritma ResNet-50 dan 
GoogleNet (Inception-V3) untuk perbandingan.

## Hasil

Hasil terbaik adalah dengan menggunakan algoritma ResNet-50 dengan accuracy 0.95.

Catatan: Training menggunakan CPU dengan IDE VSCode 

## Kesimpulan

* Penggunaan Transfer Learning pada task Gender Classification dapat memberikan hasil akurasi yang tinggi 
* Tuning parameter seperti jumlah dense layer, fine tuning, loss function, dll bisa memiliki pengaruh terhadap hasil akurasi
* Transfer Learning bisa mendapatkan akurasi yang cukup baik walaupun hanya menggunakan data yang lebih sedikit.


