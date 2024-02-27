# Java Fundamental Basic: Hello World
Lesson 2 pada Proademy Pro Sigmaka Mandiri
Setelah melakukan instalasi JDK serta IDE, yang dalam hal ini digunakan Intellij IDEA Comunity Edition dari JetBrains
Seperti pada pelatihan-pelatihan bahasa pemrograman lain, hal pertama yang dilakukan adalah membuat program untuk menulis "Hello World".
Pada program ini, terdapat beberapa bagian kode yang dapat dijelaskan lebih lanjut.

## Public Class Main
Pertama, pada Java diperlukan adanya sebuah class sebagai blueprint bagi objek-objek individu yang dibuat.
Sebuah class di Java merangkum atribut(data) dan perilaku(metode) yang dimiliki objek tersebut.
Pada repository ini, digunakan class Public Class Main sebagai class yang akan digunakan awal mula Java Virtual Machine (JVM) menjalankan program.
Penggunaan kata kunci "public" disini digunakan agar JVM mengenali kelas ini sebagai kelas yang dapat diakses oleh kelas lain meski pada package yang berbeda.
Hal ini penting karena JVM perlu akses pada kelas ini untuk memulai aplikasi.

## public static void main (String[] args)
Selanjutnya terdapat main method. Main method bertindak sebagai titik masuk aplikasi.
Metode ini sangat penting sehingga JVM secara spesifik akan mencari saat menjalankan aplikasi.
Jika kita bedah, main method terdiri dari beberapa kata kunci:

1. public : 
Sama seperti pada class, public memungkinkan metode ini dapat diakses secara bebas.
Hal ini perlu ditulis karena metode ini harus diakses oleh JVM yang berada diluar kelas yang memiliki metode ini.

2. static :
Kata kunci static memungkinkan main method untuk dipanggil dapat harus membuat instance kelas.
Hal ini karena main method harus dijankan untuk memulai program, bahkan sebelum kelas dapat membuat objek (instance).

3. void :
Pada Java, metode dapat mengembalikan values, namun main method tidak mengembalikan value.
Kata kunci ini mengindikasi bahwa setelah eksekusi, main method tidak mengembalikan value apapun.

4. main :
Ini adalah nama method yang dicari spesifik oleh JVM untuk memulai program.
Sehingga untuk main method perlu digunakan nama "main" untuk alasan tersebut.

5. String[] args :
Parameter ini mewakili array objek String, atau biasa dikenal dengan command-line arguments.
Melalui argumen ini kita dapat mempengaruhi perilaku program.

### System.out.println()
Pada kode ini, digunakan System.out.println untuk menampilkan Hello World melalui aplikasi.

## Cara kerja main method
Main method menjadi jembatan antara dunia statis dan dinamis pada Java.
Ketika aplikasi Java dimulai, JVM melakukan serangkaian langkah untuk memulai apliksai:

1. Class loading:
JVM memulai Main class, diantara semua kelas yang diperlukan aplikasi, ke dalam memori.

2. Linking:
Tahap ini, kelas akan diverikasi dan dipersiapkan.
Ini untuk memastikan kelas sudah benar dan siap dijalankan.

3. Initialization:
Variabel kelas akan diinisialisasi ke value default, dan semua inisialisasi statis akan berjalan.

4. Execution:
JVM mencari lokasi main method di Main class dan memanggilnya. Langkah ini memulai menjalankan aplikasi.

5. Termination:
Setelah selesai menjalankan main method, aplikasi akan diberhentikan.
Jika ada non-daemon thread yang masih berjalan, JVM akan menunggu mereka selesai sebelum mematikan aplikasi.

Sumber informasi:
[Beginner's Guide to 'public class Main' in Java](https://medium.com/@AlexanderObregon/beginners-guide-to-public-class-main-in-java-c6dc45e1b6af) by Alexander Obregon
