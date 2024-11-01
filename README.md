<h1 align="center"> NLP With Hugging Face Transformers </h1>
<p align="center"> Berisi tentang pipeline dari Hugging Face Transformers untuk keperluan NLP (Natural Language Processing)</p>

<div align="center">

<img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54">
<img src="https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white">

</div>
<h2 align="center"> ANALISIS </h2>

HuggingFace Transformers NLP Pipelines

1. Zero-shot Classification

Modifikasi Teks Input dan Label:

 Pada awalnya, teks input seperti "This is a course about the Transformers library" menggunakan label yang kurang sesuai untuk analisis teks terkait NLP, misalnya "education", "politics", dan "business". Modifikasi yang dilakukan:

- Teks input diubah menjadi lebih relevan, seperti "This is a detailed course on Natural Language Processing", sehingga jelas bahwa topik ini terkait NLP.
- Label kandidat diganti menjadi "technology", "education", dan "entertainment". Ini mencerminkan topik yang lebih tepat, mengingat konteks pembelajaran terkait teknologi NLP.

Tujuan Modifikasi: Memberikan label yang lebih cocok untuk klasifikasi yang terkait dengan NLP, sehingga hasil klasifikasi lebih akurat dan kontekstual.

2. Text Generation

Modifikasi Prompt dan Panjang Teks:

- Prompt awal yang generik seperti "In this course, we will teach you how to" telah disesuaikan menjadi kalimat seperti "Artificial Intelligence is changing the future by". Ini memberikan kontekstualisasi yang lebih luas.

- Parameter max_length ditingkatkan menjadi 50 kata, agar teks yang dihasilkan lebih panjang dan komprehensif. Hal ini memungkinkan model untuk mengekspresikan pemikirannya dengan lebih mendetail.

Tujuan Modifikasi: Menyediakan prompt yang spesifik pada domain teknologi dan NLP, serta menyesuaikan panjang teks untuk hasil yang lebih lengkap dan bernuansa.

3. Fill-mask Task

Modifikasi Frasa dalam Tugas Pengisian Kata:

- Frasa awal seperti "This course will teach you all about <mask> models." diganti menjadi kalimat yang lebih umum seperti "The goal of this tutorial is to teach you <mask> skills.". Ini membuka lebih banyak kemungkinan kata yang bisa diisi, seperti “technical” atau “practical,” dan memberikan konteks belajar yang lebih luas.

- Parameter top_k diubah menjadi 3 untuk menunjukkan lebih banyak alternatif kata yang mungkin.

Tujuan Modifikasi: Meningkatkan fleksibilitas hasil dengan frasa yang tidak terlalu spesifik pada model NLP saja, sehingga bisa diaplikasikan ke lebih banyak jenis pelajaran atau keterampilan.

4. Named Entity Recognition (NER)

Penggunaan Kalimat dan Entitas yang Lebih Umum:

- Kalimat seperti "My name is Sylvain and I work at Hugging Face in Brooklyn." dimodifikasi menjadi "Dr. Alice works at Google in Mountain View." untuk mencakup nama yang lebih umum dan lokasi perusahaan teknologi terkenal.

- Penggunaan entitas “Dr. Alice” dan “Google” memberikan hasil yang lebih relevan karena sering dijumpai dalam skenario NER yang nyata.

Tujuan Modifikasi: Memperkenalkan entitas umum untuk mencerminkan situasi dunia nyata, meningkatkan akurasi dan keakuratan model dalam mendeteksi nama dan organisasi terkenal.

5. Summarization

Penggunaan Teks yang Lebih Singkat dan Ringkas:

- Teks awal yang cukup panjang tentang perubahan dalam pendidikan teknik Amerika diganti menjadi teks yang lebih ringkas dan fokus pada perkembangan AI dalam beberapa kalimat.

- Teks baru seperti:
plaintext
Copy code
"The field of Artificial Intelligence has been growing rapidly, especially in areas like natural language processing and computer vision..."
lebih singkat, tetapi tetap mencakup poin utama tentang perkembangan AI.

Tujuan Modifikasi: Menghasilkan ringkasan yang tetap mempertahankan informasi inti tanpa terlalu panjang, yang penting dalam berbagai konteks bisnis dan akademik.

6. Sentiment Analysis

Modifikasi Teks untuk Klasifikasi Sentimen:

- Teks yang digunakan awalnya agak ambigu, yaitu "The model was so great! I think I'm going to choose other". Kalimat ini mengandung pujian namun diikuti dengan niatan untuk memilih model lain, yang bisa membingungkan model analisis sentimen.

- Modifikasi dibuat dengan dua teks berbeda:

"This product exceeded my expectations. I highly recommend it!" yang mewakili sentimen positif dengan pujian.

"I found some issues with this product, so I'm considering other options." yang menunjukkan sentimen negatif atau netral dengan kritik halus.

Tujuan Modifikasi: Memberikan contoh yang lebih jelas antara sentimen positif dan negatif sehingga model dapat melakukan klasifikasi yang lebih konsisten dan akurat.

7. Question Answering

Penggunaan Konteks yang Berbeda untuk Pertanyaan dan Jawaban:

- Pertanyaan awal tentang definisi air dimodifikasi untuk memberikan konteks tentang teknologi dan tokoh terkenal.

- Dua contoh konteks yang digunakan adalah:

Contoh 1: "Python adalah bahasa pemrograman tingkat tinggi yang dikembangkan oleh Guido van Rossum." dengan pertanyaan "Apa itu Python?", untuk jawaban berbasis definisi teknologi.

Contoh 2: "Elon Musk adalah CEO SpaceX dan Tesla, serta pendiri Neuralink dan The Boring Company." dengan pertanyaan "Apa peran Elon Musk di SpaceX?", yang menyoroti peran penting individu dalam sebuah perusahaan.