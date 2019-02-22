# Platinum-Rift-Project

Anggota kelompok :

Feroz Fernando (16518314)	
Jones Napoleon A. (16518283)	
Raisa Gautama (16918087)	
Alvian Ricardo (16918042)

Strategi : Menyebarkan pods ke segala arah adjacentzones. Secara garis besar, metode yang kami gunakan adalah brute force, dimana kami
akan terus menyebarkan pods dengan harapan akan ada pod yang mencapai markas musuh. Strategi ini kami ambil karena 2 alasan :

1. Pada umumnya, orientasi bot maupun player pada leaderboard adalah selalu meninggalkan markas tanpa satupun pod yang tersisa, sehingga
jika ada 1 pod milik kami yang bisa mencapai markas mereka, maka game bisa kita menangkan.
2. Saat terjadi kasus terburuk (misalnya area map yang sangat luas sehingga tidak memungkinkan robot menyebar dalam 250 turn), kami tetap
memiliki keunggulan poin. Hal ini disebabkan karena untuk memenangkan permainan, objective lainnya adalah dengan menguasai zona sebanyak
banyaknya. Dengan menyebarkan pods ke segala arah, implikasinya adalah zona yang dapat dikuasai akan lebih banyak.

Secara spesifik, strategi kami adalah sebagai berikut :
1. Pods akan disebar ke daerah yang belum terisi sebagai orientasi utama. Penyebaran pods akan dilakukan dengan melihat adjacent zones 
(zona yang berdekatan) dengan hex tempat pods berada. Pembagian pods akan berdasarkan jumlah adjacent zones. Misalnya ada 10 pods dengan 3
adjacent zones, maka pods akan dibagi 3 ke setiap adjacent zones dengan meninggalkan 1 pod di zona awal (menggunakan fungsi div)
2. Saat pod tersisa 1 seperti pada kasus div dengan bilangan yang bersisa tidak nol, namun ada lebih dari satu jalan yang dapat diambil,
maka jalan yang diambil adalah mengambil jalan random dari adjacent zones yang tersedia.
