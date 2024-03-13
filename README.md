# Module 5
> Fathan Naufal Adhitama - 2206825965

## Refleksi
1. _Performance Testing_ yang dilakukan JMeter dan Profiling yang dilakukan IntelliJ Profiler
adalah dua hal yang berbeda secara garis besar. Performance Testing terjadi pada tingkat sistem, untuk mengukur
efektivitas dan efisiensi sistem pada berbagai jenis _load_ dan _stress_, dan memastikan sistem Anda sesuai 
dengan _Service Level Agreements_ (SLA). Sementara _Profiling_ adalah hal yang dilakukan ketika performance testing
menunjukkan masalah. Ini dapat membantu kita mengidentifikasi bagian-bagian sistem yang paling 
berpengaruh pada performance issues dan menunjukkan kita di mana bagian yang harus difokuskan untuk diperbaiki.
2. Dengan menunjukkan dan meng-_highlight_ bagian-bagian kode yang menggunakan **_resource_** paling banyak, _Profiling_
membantu developer untuk melakukan optimisasi kode dengan tepat dan cepat, untuk meningkatkan kinerja dari aplikasi.
Metode _profiling_ yang teliti ini sangat penting, terutama dalam sistem yang kompleks di mana mengidentifikasi 
_bottlenecks_ akan menjadi sulit.
3. Ya, fitur Profiler yang terintegrasi dengan IDE ini sangat membantu mempermudah saya untuk menganalisis dan
mengidentifikasi _bottlenecks_ dengan efektif. IntelliJ Profiler dapat membantu saya melihat visualisasi
hasil evaluasi performance dengan Flame Graph, Method List, dan banyak lagi. Informasi yang diberikan juga lengkap
meliputi CPU Time, Total Time, dan Memory yang digunakan oleh program. Dengan bantuan IntelliJ Profiler ini, saya
dapat mengevaluasi performa kode dengan lebih efektif dan efisien.
4. Mungkin beberapa contoh kesulitan yang saya hadapi adalah sulit memahami istilah-istilah baru seperti perbedan 
CPU Time dan Total time, Cara membaca Flame Graph, _bottlenecks_, dll. Akan tetapi, masalah tersebut dapat terselesaikan
ketika saya membaca kembali modul dengan lebih teliti dan mencari tau dengan bantuan google. Selain itu, saya juga
masih belum terlalu paham mengenai indikasi method yang sudah efektif atau belum karena yang ditunjukkan hanyalah waktu
dalam milisecond, saya belum tahu apakah waktu yang ditunjukkan oleh method ini perlu dioptimasi lagi atau tidak. Masalah ini
saya rasa dapat diselesaikan dengan memperbanyak pengalaman dalam melakukan refactoring code untuk memperbanyak
pengetahuan tentang standar standar running time dan resources yang normal dari sebuah method.
5. Beberapa keuntungan yang diberikan dengan menggunakan IntelliJ Profiler adalah mempermudah kita untuk melakukan Profiling
dengan Integrasi yang kuat antara IDE dengan Profiler. Interface yang User-Friendly juga membantu untuk memahami
hasil evaluasi yang telah dilakukan. Dengan begitu, informasi CPU Time, Total Time, dan Memory Management
yang diberikan IntelliJ Profiler juga dapat dimanfaatkan dengan baik oleh developer untuk melakukan optimasi kode.
6. Untuk kasus tersebut, saya sendiri belum pernah menjumpai kasus dimana hasil profiling dengan IntelliJ Profiler
tidak sepenuhnya konsisten dengan hasil temuan performance testing menggunakan JMeter. Akan tetapi, saya rasa 
apabila kasus tersebut terjadi, langkah pertama yang dilakukan adalah memeriksa konfigurasi dan parameter yang digunakan
dalam kedua proses tersebut. Pastikan kondisi dan konfigurasi pengujian serupa, 
lalu analisis perbedaan environment, seperti perbedaan antara environment development dan production.
Selanjutnya, teliti hasil dari kedua alat secara menyeluruh, cari pola atau anomali yang dapat menjelaskan perbedaan tersebut,
dan pertimbangkan untuk melakukan pengujian secara berulang serta berkonsultasi dengan orang lain yang lebih ahli jika diperlukan.
7. Setelah menganalisis hasil performance testing dan profiling, berikut adalah beberapa strategi yang saya
lakukan untuk mengoptimalkan kode yang ada:

   - Memperhatikan hasil *profiling* untuk mencari method yang memakan waktu paling banyak dan
   menggunakan resource paling banyak.
   - Memfokuskan untuk memahami kode tersebut untuk mencari bagian yang dapat dioptimalkan
   - Memilih algoritma dan struktur data yang paling efektif untuk method tersebut
   - Identifikasi bagian kode yang dapat dieksekusi secara bersamaan dan gunakan threading atau multiprocessing untuk parallel computating.
   
    Setelah melakukan perubahan pada kode tersebut, harus dipastikan bahwa kode/program tetap dapat berfungsi 
dengan baik dengan menjalankan testing yang telah dibuat.

***

## Screenshots of JMETER GUI Test Results
### 1. `/all-student`
- Before Optimization:
![Before Optimization](https://cdn.discordapp.com/attachments/1205832140114235463/1217440130537881651/all-student_before.jpg?ex=6604087a&is=65f1937a&hm=5b3df814f882f82b5fb788f0d5e7486a72c01d50dd6fab39c3eb76d8075cb53a&)
- After Optimization:
![After Optimization](https://cdn.discordapp.com/attachments/1205832140114235463/1217438462857449482/messageImage_1710330053824.jpg?ex=660406ec&is=65f191ec&hm=1abecd71ee0d76f28820a4ddfc64e73b1bdf23ee0ab74b8274675166fa3b1f6b&)

### 2. `/all-student-name`
- Before Optimization:
![Before Optimization](https://cdn.discordapp.com/attachments/1205832140114235463/1217440131422617630/all-student-name_before.jpg?ex=6604087a&is=65f1937a&hm=c6124d948cf580ac0b0043c82a83cb3635003baf1f02ec0bbde1ce1d24f19840&)
- After Optimization:
![After Optimization](https://cdn.discordapp.com/attachments/1205832140114235463/1217438462077042808/messageImage_1710329922419.jpg?ex=660406ec&is=65f191ec&hm=92ab1024f36a67cd1568067b2a1caa2b93d48cc28a6933841029ce7a295884f6&)
### 3. `/highest-gpa`
- Before Optimization:
![Before Optimization](https://cdn.discordapp.com/attachments/1205832140114235463/1217440130952990810/highest-gpa_before.jpg?ex=6604087a&is=65f1937a&hm=8ec163273ac69a96451f0d83716c0e40d15d0b6124afb1a9889ac276f1d4afcb&)
- After Optimization:
![After Optimization](https://cdn.discordapp.com/attachments/1205832140114235463/1217438462580363354/messageImage_1710330015239.jpg?ex=660406ec&is=65f191ec&hm=651d96f27bfbe3798c17d1d1ebb38c0134a2b4d6079b79e26d65c2c6a9918965&)

***
## Screenshots of JMETER Command Line Test Results 
### 1. `all-student`
![CLI All Student](https://cdn.discordapp.com/attachments/1205832140114235463/1217442557160849488/messageImage_1710196472809.jpg?ex=66040abc&is=65f195bc&hm=9f5a4f7813059cfc9d1c7333b3433172c12dcd9df2e5c4a567fed9cf3f92c0b2&)
### 2. `all-student-name`
![CLI All Student Name](https://cdn.discordapp.com/attachments/1205832140114235463/1217442556867121152/messageImage_1710206517344.jpg?ex=66040abc&is=65f195bc&hm=f9612139f04c23e11dce222d3dcf1a049c9e40e17e24cc97124e429b680b925a&)
### 3. `highest-gpa`
![CLI Highest GPA](https://cdn.discordapp.com/attachments/1205832140114235463/1217442556552544337/messageImage_1710206592139.jpg?ex=66040abc&is=65f195bc&hm=7e1237d7cf821ecf5495d446b526a43954ca09e147c10a54a26f66ff0343c47b&)

Berdasarkan _screenshot-screenshot_ tersebut, dapat terlihat bahwa `Sample Time` method sebelum dioptimasi lebih lama 
dibandingkan setelah optimasi. Oleh karena itu, dapat disimpulkan bahwa proses optimasi yang dilakukan dapat terbilang
berhasil untuk membuat kode lebih efektif dan efisien.