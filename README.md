# MODEL KLASIFIKASI RUPARUPA

Repository ini berisi program jupyter notebook (ipynb) untuk membuat model klasifikasi jenis mebel menggunakan Convolutional Neural Network. 

## Link Dataset

Dataset yang kami gunakan berasal dari dataset yang tersedia pada website Kaggle yang bernama Furniture Detector (link ada dibawah). Dataset kami terdiri dari 5 kelas yaitu chair, swivelchair, bed, table, dan sofa. Isi dataset terdiri atas 3500 file gambar train, 500 file gambar validasi, dan 100 file gambar test yang masing-masing jumlah gambarnya sudah setara.
[https://www.kaggle.com/datasets/akkithetechie/furniture-detector]

## Library yang digunakan

- Tensorflow
- Numpy
- Matplotlib
- Seaborn
- Sklearn

## Augmentasi Data

Augmentasi yang digunakan dalam data pelatihan mencakup normalisasi piksel gambar ke rentang [0, 1] dengan rescale serta berbagai transformasi seperti rotasi, pergeseran horizontal dan vertikal, transformasi geser (shear), zoom, dan flipping horizontal. Sedangkan data validasi hanya melalui proses rescale tanpa modifikasi lainnya untuk menjaga kemurnian evaluasi model.

## Arsitektur CNN

1. Input Layer dengan dimensi 3 channel warna RGB.
2. Convolution dan Pooling Layer yang dilakukan sebanyak 3 kali yang menambahkan filter konvolusi (32, 64, dan 128), menggunakan aktivasi ReLU, dan mengurangi dimensi spasial gambar.
3. Flatten Layer untuk mengubah data multidimensi menjadi vektor 1 dimensi.
4. Fully Connected Layer menggunakan Dropout sebesar 0,5 untuk mencegah overfitting.
5. Output Layer yang terdiri atas 5 neuron yang mewakili masing-masing kelas menggunakan aktivasi softmax.

## Cara Menjalankan Program

1. Pastikan library yang dibutuhkan sudah diinstal. (Jika run di Google Colab tidak perlu instal lagi)
   ```bash
   !pip install tensorflow numpy matplotlib seaborn sklearn
   ```
2. Pastikan folder dataset berada pada direktori yang sama dengan ipynb.
3. Jalankan program dengan menjalankan cell satu per satu.
4. Setelah model dilatih, hasil model akan disimpan dalam bentuk file .h5
5. Untuk melihat hasil akurasi model bisa menjalankan cell evaluasi model, confussion matrix, dan classification report.
6. Untuk memastikan model dapat mengklasifikasi gambar bisa menjalankan cell terakhir (gambar diambil dari dataset test).

## Kelompok 4
- Alifio Nauval Priatmodjo (50421127)
- Befon Mario Christmawan (50421271)
- Ivanno Rifky Ali Raharjo (50421673)
- Muhammad Zharfan Alfanso (51421100)

Link GitHub Backend : [https://github.com/muhzarfan/back-end-rupa2]  
Link GitHub Frontend : [https://github.com/alifionauval/ruparupa]  
Link Github Machine Learning : [https://github.com/muhzarfan/model-ruparupa]  
Link Figma : [https://www.figma.com/design/wm6Y63ngdAHnPUef59v5lz/Design?node-id=7-3&t=iD9N2lHIsPdQSDpY-1]  
Link Trello : [https://trello.com/invite/b/67820138bdd1937ea9a6411a/ATTI5edb9cd2b0486426f45cbe84bd94404eF282ED0A/kelompok-4-rpl-2]  
Link Google Docs Proposal Penawaran : [https://docs.google.com/document/d/1szpxZGRCdu1v95KaTYMj-LD0JaTX4u16k1wnWNui_K0/edit?usp=sharing]  
