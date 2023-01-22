# Object Tracking Yolov5 and Strongsort
Pada tugas ini saya mempelajari dan menerapkan object tracking dengan arsitektur YoloV5 dan object counter dengan Strongsort. Selain itu ada 2 objektif yang harus dikerjakan juga, yaitu antara lain:<br>
* Membuat algoritma untuk mendapatkan timestamp dari setiap mobil yang telah terhitung.
* Membuat algoritma untuk membuat grafik intensitas mobil dari data tracking dan counter, serta timestamp yang sebelumnya telah didapatkan.

### Hasil Penerapan Object Tracking YoloV5 dan Object Counter dengan Strongsort
Kode utama yang dijalankan adalah melalui [track.py](https://github.com/ilyamfaisal28/Object_Tracking_Yolov5_and_Strongsort/blob/main/track.py). <br>
Sedangkan untuk hasil inferensinya dapat dilihat di [Runs/track/exp69](https://github.com/ilyamfaisal28/Object_Tracking_Yolov5_and_Strongsort/tree/main/runs/track/exp69)
atau melihat video di bawah ini:

https://user-images.githubusercontent.com/89628535/213868220-09f66635-4303-458c-801d-cc268404421d.mp4

### Mendapatkan Timestamp
Kode untuk mendapatkan timestamp terdapat pada [track.py](https://github.com/ilyamfaisal28/Object_Tracking_Yolov5_and_Strongsort/blob/main/track.py).
Cara kerjanya adalah ketika objek melewati garis hijau, maka timestamp akan diperoleh dengan cara menambahkan (append) `list` timestamp dengan waktu sekarang menggunakan `datetime.datetime.now()`.
Sehingga menjadi seperti ini:<br>
`time_hit = datetime.datetime.now()` <br>
`timestamp.append(time_hit)`

### Grafik Intensitas Mobil
Sebelum pembuatan grafik, pertama harus mendapatkan data timestamp beserta kelas dan id objek dari setiap objek atau mobil yang telah terhitung. Lalu dibuat dalam bentuk file csv.
Kode untuk mendapatkan data-data tersebut beserta pembuatan file csv terdapat pada [track.py](https://github.com/ilyamfaisal28/Object_Tracking_Yolov5_and_Strongsort/blob/main/track.py).
<br>
Setelah mendapatkan file csv, lanjut membuat grafik berdasarkan file csv tersebut. Untuk kodenya dapat dilihat di [(Magang)_Pembuatan_Grafik_Timestamp_Object_Counting.ipynb](https://github.com/ilyamfaisal28/Object_Tracking_Yolov5_and_Strongsort/blob/main/(Magang)_Pembuatan_Grafik_Timestamp_Object_Counting.ipynb)
