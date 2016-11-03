Sudah banyak situs maupun lembaga yang menyediakan data shapefile contohnya seperti ESRI namun file tersebut masih belum dapat kita lihat hasilnya tanpa menggunakan software pembantu contoh nya seperti QGIS maupun python , didalam shapefile itu sendiri mempunyai banyak file contohnya seperti file shp dan dbf , untuk membaca shapefile dengan menggunakan python kita bisa memanggil langsung file shp tersebut atau bisa membuat class terlebih dahulu.

**Pembahasan**

SHP adalah salah satu file yang berada didalam shapefile yang menyimpan data geometri.

Didalam file shp terdapat beberapa data seperti :

1.  Bbox adalah sebuah boundary box(koordinat 4 titik) atau koordinat batas view pada peta

2.  Point adalah titik koordinat

3.  Shapetype adalah jenis data geometri yang mempunyai standar nomor yang ditetapkan oleh ESRI seperti nomor 1 untuk poin, 2 untuk polygon, 3 untukpolyline ,dll.

Membaca jumlah data geometri dengan python :

import shapefile

sf = shapefile.Reader(“namafile.shp”)

sf.shapes()

a = sf.shapes()

len(a)

DBF adalah sebuah file yang menyimpan file tabular yang menyimpan data atribut.

Membaca data dbf :

import shapefile

sf.records()

sf.records(n)
