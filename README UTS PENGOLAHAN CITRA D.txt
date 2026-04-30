ANALISA SOAL UTS PENGOLAHAN CITRA DIGITAL

========================================
SOAL 1 – TRANSFORMASI CITRA
===========================

1. Perbedaan Persebaran Nilai Keabuan

Citra Asli:
Citra asli memiliki distribusi nilai keabuan yang sesuai dengan kondisi asli gambar. Nilai piksel bisa tersebar dari gelap ke terang tergantung objek dalam citra.

Citra Negatif:
Transformasi negatif membalik nilai keabuan, dimana piksel gelap menjadi terang dan piksel terang menjadi gelap. Histogram citra juga ikut terbalik, namun informasi detail tetap sama.

Citra Logaritmik:
Transformasi logaritmik memperluas nilai piksel rendah (gelap) dan mengompresi nilai piksel tinggi (terang). Hal ini membuat detail pada area gelap lebih terlihat. Histogram cenderung menumpuk di area terang.

2. Kapan Transformasi Logaritmik Lebih Bermanfaat?

Transformasi logaritmik lebih bermanfaat ketika:

* Citra terlalu gelap
* Detail pada area gelap sulit terlihat
* Digunakan pada citra medis atau citra malam hari

Sedangkan transformasi negatif digunakan untuk:

* Membalik tampilan visual
* Analisis citra seperti X-ray

========================================
SOAL 2 – KONVOLUSI FILTER
=========================

1. Perbandingan Visual dan Nilai Piksel

Low Pass Filter (LPF):
LPF menghasilkan gambar yang lebih halus (blur). Noise berkurang karena frekuensi tinggi dihilangkan. Nilai rata-rata piksel relatif stabil.

High Pass Filter (HPF):
HPF menonjolkan tepi dan detail kasar pada gambar. Gambar terlihat lebih tajam pada bagian tepi. Nilai rata-rata cenderung kecil karena banyak perubahan intensitas.

Band Pass Filter (BPF):
BPF menghasilkan gambar yang lebih tajam (sharpening). Detail terlihat lebih jelas dibanding citra asli. Nilai rata-rata mendekati citra asli tetapi dengan kontras lebih tinggi.

2. Hubungan Domain Spasial dan Frekuensi

Low Pass Filter:
Berfungsi pada domain frekuensi rendah. Menghaluskan citra dan menghilangkan noise.

High Pass Filter:
Berfungsi pada frekuensi tinggi. Menonjolkan tepi dan perubahan intensitas.

Band Pass Filter:
Menggabungkan efek low dan high pass. Mempertahankan detail penting dan mengurangi noise ringan.

========================================
SOAL 3 – PERHITUNGAN KONVOLUSI
==============================

Diketahui citra grayscale 3x3:

100  90  80
60   50  40
30   20  10

Kernel High Pass Filter (HPF):

-1 -1 -1
-1  8 -1
-1 -1 -1

Perhitungan dilakukan pada piksel tengah (50):

= (-1×100) + (-1×90) + (-1×80)

* (-1×60) + (8×50) + (-1×40)
* (-1×30) + (-1×20) + (-1×10)

= -100 -90 -80
-60 +400 -40
-30 -20 -10

= 400 - (100+90+80+60+40+30+20+10)

= 400 - 430

= -30

Hasil akhir konvolusi pada titik tengah adalah -30.

========================================
KESIMPULAN
==========

Transformasi citra digunakan untuk memodifikasi nilai piksel guna meningkatkan kualitas visual dan informasi. Filter konvolusi membantu dalam proses penghalusan, deteksi tepi, dan penajaman citra dengan memanfaatkan konsep domain spasial dan frekuensi.
