## JS Array

Array merupakan tipe data yang difunakan untuk menampung banyak tipe data sekaligus. Baik itu tipe data string, iteger, boolean dll. Penulisan sysntax dasar membuat array yaitu:

let array = ["hai", 1, false]

cara akses isi array pada dasarnya kita hanya memanggil indeks data didalam arraynya. Dalam analoginya array itu sebuah kreta dan isi array itu adalah gerbongnya. 

Contonya semisal kita ingin mengakses isi dari kereta array maka panggil gerbong pertama. Jadi seperti ini:

console.log(array[1]);

maka akan keluar tampilan: hai

Jika inginmengetahui semua isi keretanya, cukup dengan:

console.log(array)

maka akan keluar tampilan:

['hai', 1, false]

JS array juga memiliki property yaitu:

1. length yang digunakan untuk menghitung banyaknya isi sebuah array.

JS array pun memiliki method yaitu:

1. push() digunakan untuk menambahkan data pada array yang diletakkannya diakhir.
2. unshift digunakan untuk menambahkan data array yang diletakkan didepan.
3. pop() digunakan untuk menghapus data array dari akhir.
4. shift() digunakan untuk menghapus awal data diarray 
5. splice() digunakan untuk menghapus dan menambahkan data ditengah pada array

![contohArraySplice](/Images/Screenshot%202022-10-07%20153121.png)

6. slice() digunakan untuk mengcopy data array.

![contohArraySlice](/Images//Screenshot%202022-10-07%20154140.png)

Menggunakan looping pada array:

1. for loop

![contohForLoopdiArray](/Images/Screenshot%202022-10-07%20160256.png)

2. For of loop. Penulisan syntaxnya yaitu:

for (variabel of iterasi){
    
    aksi
}

Hasilnya:

![contohForofLoopdiArray](/Images/Screenshot%202022-10-07%20161020.png)

3. For Each Loop

![contohForEachLoopdiArray](/Images/Screenshot%202022-10-07%20162006.png)

4. Map Loop. digunakan untuk looping, mengembalikan (return)dalam bentuk array

![contohMapLoopdiArray](/Images//Screenshot%202022-10-07%20163605.png)

Selanjutnya terdapat array multidimensi. Nah, array multidimensi ini adalah sebuah array yang didalamnnya ada array lagi. Contohnya:

![contohArrayMultidimensi](/Images//Screenshot%202022-10-07%20165504.png)

## JS Object


Pada umumnya objek itu sesuatu yang dapat dilihat dan dirasakan. Baik itu benda mati atau makhluk hidup itu dinamakan objek. Dari segi duani programming object itu adalah sebuah tipe data pada variabel yang menyimpan properti dan fungsi. sama halnya array object dapat menyimpan berbagai banyak data. 

Contohnya: semisal objek smartphone, ia memiliki properti nomor seri, warna, chip dll. Nah untuk methodnya smartphone memiliki fungsi menelpon, sms, membuat video, foto dll.

![contohObject](/Images/Screenshot%202022-10-08%20103752.png)

cara mengakses sebuah object terdapat dua macam:
1. Menggunakan dot notation. Contohnya: console.log(siswa.nama)

2. Bracket. Contohnya: console.log(siswa["nama"])

3. Memanggil property objek dengan variabel. Contoh:

let property = "umur"

console.log(siswa[property])

Cara membuat property baru disebuah object

![contohMembuatPropertybaru](/Images/Screenshot%202022-10-08%20105242.png)

kita cukup menuliskan nama objeknya, lalu tuliskan property dan value yang akan ditambahkan.

Cara assigment object:
1. Cara memasukkan value ke dalam property sebuah objek.

Contohnya: siswa.umur = 22

Jadi panggil nama objeknya, selanjutnya nama property yang akan diubah valuenya, dan isikan value terbarunya.

Cara menghapus object di JS. Menggunakan keynya yaitu delete.

Contohnya: delete siswa.umur

jadi ouputnya dalam objek siswa property umur akan terhapus.

Cara membuat object yang menampung function:

![contohobjeckNampungFunction](/Images/Screenshot%202022-10-08%20121845.png)

untuk mengaksesnya masih sama, cuma dikarenakan valuenya itu adalah function. Untuk memanggilnya property ditambahkan () yang menendakan value berisi function. Jika ingin merubah object menjadi array terdapat biult in methodnya:

console.log(Object.keys(siswa))

console.log(Object.value(siswa))

Untuk yang keys ia kan merupakan nama lain dari property, jadi ia akan membuat sebuah array yang berisikan property dari object siswa. Sedangkan untuk membuat array dari value object dengan menggunakan object.value

Cara membuat nested object:

![contohNestedobject](/Images/Screenshot%202022-10-08%20124418.png)

Cara penggunaan loop di object yaitu menggunakan for in:

![contohLoopObject](/Images/Screenshot%202022-10-08%20132414.png)

Cara menggunakan array of object: bentuk dasarnya [{}, {}, {}]

![contohArrayofObject](/Images/Screenshot%202022-10-08%20132545.png)

## JS Modules


JS modules merupakan cara untuk memisahkan kode ke file yang berbeda. Sehingga nantinya kita tidak akan membuat satu file utama js saja, melainkan terdapat beberapa file dengan satu file utama. Keuntungannya yaitu:
- Mudah untuk mengelola kode
- Kode yang ga menumpuk di satu file

Nah untuk mempelajari js modeles kita memerlukan dua keyword yaitu export dan import. 

Contohnya: kita membuat satu file utama dengan nama indonesia.js dan file lainnya jepang.js. Pada file jepang.js kita melakukan export variabel

![contohExportVariabel](/Images/Screenshot%202022-10-08%20185256.png)

Pada file utama indonesia.js kita melakukan penangkapan export dengan kata kunci import. Penulisan dasarnya import ... from ./jepang.js

![contohImportVariabel](/Images/Screenshot%202022-10-08%20185450.png)

Tidak hanya variabel saja yang dapat menggunakan export dan import. Bisa dalam bentuk object, string, number, function. Kita tidak bisa melakukan export functio, variabel dll didalam satu file js. Dianjurkan untuk memilihnya. 

Selanjutnya ada yang namanya export default.Dalam artian bahwa jepang memiliki satu produk utama yaitu entertaiment. Export default hanya memberikan 1 export di setiap file.

Contoh eport default pada file jepang.js

![contohExportDefault](/Images/Screenshot%202022-10-08%20191702.png)

Penangkpan export menggunakan imprt di file indonesia.js

![contohImportDeafult](/Images/Screenshot%202022-10-08%20192418.png)

Dan juga perlu diingat bahwa file yang menjadi file utama tidak bisa melakukan export hanya bisa menerima import. Begitu juga file lainnya hanya bisa melakukan export tidak bisa melakukan import.

## Recursive JS

Recursive ialah function yang memanggil dirinya sendiri sampai kondisi tertentu. Recursive ini termasuk paradigma pemograman. Idealnya recursive digunakan untuk menyelesaikan operasi matematika. Didalam penulisannya cukup dengan kita membuat function yang berisikan conditional yang akan memanggil si recursive itu. Kunci membuat sebuah recirsive:
1. Base case yaitu titik paling kecil / titik berhenti
2. Recursive case yaitu titik dimana ia memanggil dirinya sendiri.
Contoh:

![contohRecursive](/Images/Screenshot%202022-10-08%20195859.png)

## JS Asynchronous 

Penggunaan asycronous ketika kita akses sebuah web dan web itu memerlukan pengambilan data (loading) maka kita dapat melakukan interaksi dengan cara mengakses halaman website atau fitur website yang lain. Javascript merupakan bahasa yang memiliki konsep JS Single thread, non-blocking, dan asyncronous.
- Single thread yaitu JS hanya memiliki satu jalur proses.
- Non-blocking. Dikarenakan JS hanya memiliki single thread apabila menemui suatu proses yang membutuhkan waktu eksekusi yang lama, maka ia akn secara otomatis mempersilahkan proses lain agar lebih dahulu dieksekusi.
- asyncronous yaitu suatu proses yang dieksekusi tidak secara berurutan. 

JS asyncronous memiliki tiga kunci utama:
1. Callback merupakan function yang dijadikan sebagai argument. Contoh:

![contohCallback](/Images/Screenshot%202022-10-09%20115216.png)

2. Promise. dalam promise ada beberapa istilah utama yaitu pending, rejected dan fulfailed.

- Pending itu semisal kita janjian ketemuan hari kamis. Nah dari hari kita mengajak smpai hari kamis itu dinamakan pending/jeda
- rejected. Keadaan apabila disaat sedan pending, salah satu pihak mengabarkan batal untuk melakukan ketemuan, maka itu disebut rejected/batal
- fulfailed. Keadaan promise ketemuan itu terpenuhi

Contoh

![contohPromise](/Images/Screenshot%202022-10-09%20122613.png)

3. Async await

Penjelasan dasar sebelum membahas aync await. Yaitu mengenal tentang database, server dan cara mengambil data kemudian ditampilkan dalam bentuk html. Contoh sederhana implementasinya: Jika menemukan sekumpulan data gambar, tulisan yang banyak, maka tidak mungkin kita membuat data tersebut berulang kali langsung di hard code html. Alangkah baiknya data tersebut disimpan oleh database. Jika ingin menampilkannya maka harus request ke server kemudian server akan request ke database. Setelah diterima oleh database, hasilnya akan dikembalikan lagi ke server sampai akhirnya dapat ditampilkan pada halaman html.

Dari contoh sederhana tersebut pasti sudah mengerti keterhubungan database, server, dan html. Terdapat satu hal lagi, yaitu yang menjadi perantara html ke server dan database disebut dengan API. Untuk menangkap data dari API kita menggunakan juga Async Await. Cara penulisannya:

![contohPenulisanAyncAwait](/Images/Screenshot%202022-10-16%20150450.png)

Dari contoh penulisan diatas dapat menggunakan versi function biasa atau juga dapat menggunakan arrow function. Nah dikarenakan API itu berupa endpoint atau url, guna meminta/request layanannya membutuhkan yang dinamakan fetch. Contohnya:

![contohPenulisanAsynAwait2](/Images/Screenshot%202022-10-16%20151910.png)

Didalam contoh tersebut selain penggunaan async terdapat juga penggunaan await. Nah kedua keyword itu yang menjadi cirikhas async await. Ketika kita request ke API ia akan mengembalikan data berformat json(Javascript on notation) alias dalam bentuk array of object. Kegunaan lainnya json yaitu untuk unboxing data yang ada didalam API.

## Web Storage

dari kata Storage merupakan kata yang sudah tak asing lagi untuk didengar. Berasal dari bahasa inggris yang artinya penyimpanan. Sehingga web storage ialah sebuah penyimpanan data secara lokal yang ada di web. jadi, web memiliki penyimpanannya sendiri. selain web storage terdapat penyimpanan data lainnya via web yaitu cookie. Sebelum adanya pembaharuan HTML versi 5 penyimpanan web menggunakan cookie, jelas kalau dari segi performa lebih bagus web storage. Perantara file JS dengan web browser menggunakan web API. Apabila ingin menggunakan web storage diusahakan datanya sudah dalam bentuk terenskripsi.

Data yang dapat disimpan pada web storage:
- Data yang berguna untuk preferensi user
- Data settingan web
- Data score
- Data posisi video

Data yang tidak bisa disimpan pada web storage:
- Data sensitif (identitas, autentikasi)

Web storage memiliki dua jenis objek untuk menyimpan data:
1. localStorage. penyimpanan web yang tidak memiliki masa expire
2. Session storage. penyimpanan yang diperuntukkan buat satu sesi saja. Jadi apabila kita close tab datanya akan hilang

## Git dan Github Lanjutan


Mengapa seorang programmer wajib memiliki tools git dan Github? alasannya cukup simple sebab dua tools itu memiliki ketergantungan satu sama lain, dan hampir semua orang yang bekerja didunia programmer memilikinya untuk memudahkan pekerjaan mereka. Perbedaan dari Git dan Github sendiri yaitu git berfungsi mencatat setiap perubahan pada file proyek yang dikerjakan oleh banyak orang maupun sendiri, sedangkan github  layanan cloud yang berguna untuk menyimpan dan mengelola sebuah project yang dinamakan repository (repo git) sehingga memodahkan programmer untuk berkolaborasi menyelesaikan program

Cara membuat repository baru di git cukup mudah, dengan menggunakan perintah: mkdir (make directory) kita sudah dapat membuat directory local. Jika kita ingin melakukan 'commit' maka terlebih dahulu melakukan 'git init .' pada directory projek yang akan dihubungkan ke Github, setelah itu melakukan 'git add .', nah baru kita dapat melakukan 'git commit -m'. Fungsi dari 'git commit' yaitu memberikan pesan di terakhir perubahan yang kita buat.

di materi Git dan Github lanjutan ini saya sudah merangkum step by step mulai dari membuat repository organization sampai cara menangani jika terdapat conflict di Github:

![git&GithubLanjutan](/Images/Screenshot%202022-10-15%20123357.png)

Keterangan: Untuk tulisan yang berwarna orange merupakan tugas/step by step yang harus dilakukan oleh team leader.




