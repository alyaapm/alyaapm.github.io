ALJABAR PLOT2D
# EMT untuk Perhitungan Aljabar

Nama: Alya Putri Medilasari

Kelas : Matematika B

NIM : 23030630018
 
Pada notebook ini Anda belajar    menggunakan EMT untuk melakukan berbagai perhitungan terkait dengan materi atau topik dalam Aljabar. Kegiatan yang harus Anda lakukan adalah sebagai berikut:

1. Membaca secara cermat dan teliti notebook ini Menerjemahkan teks bahasa Inggris ke bahasa Indonesia;
2. Mencoba contoh-contoh perhitungan (perintah EMT) dengan cara meng-ENTER setiap perintah EMT yang ada (pindahkan kursor ke baris perintah)
3. Jika perlu Anda dapat memodifikasi perintah yang ada dan memberikan keterangan / penjelasan tambahan terkait hasilnya.
4. Menyisipkan baris-baris perintah baru untuk mengerjakan soal-soal Aljabar dari file PDF yang saya berikan;
5. Memberi catatan hasilnya.
6. Jika perlu tuliskan soalnya pada teks notebook (menggunakan format LaTeX).
7. Gunakan tampilan hasil semua perhitungan yang eksak atau simbolik dengan format LaTeX. (Seperti contoh-contoh pada notebook ini.)

# Contoh pertama

Menyederhanakan bentuk aljabar:
$$6x^{-3}y^5\times -7x^2y^{-9}$$>$&6\*x^(-3)\*y^5\*-7\*x^2\*y^(-9)

$$-\frac{42}{x\,y^4}$$Menjabarkan:
$$(6x^{-3}+y^5)(-7x^2-y^{-9})$$
\>$&showev('expand((6\*x^(-3)+y^5)\*(-7\*x^2-y^(-9))))

$${\it expand}\left(\left(-\frac{1}{y^9}-7\,x^2\right)\,\left(y^5+  \frac{6}{x^3}\right)\right)=-7\,x^2\,y^5-\frac{1}{y^4}-\frac{6}{x^3  \,y^9}-\frac{42}{x}$$

# Baris Perintah

Baris perintah Euler terdiri dari satu atau beberapa perintah Euler diikuti dengan titik koma ";" atau koma ",". Titik koma mencegah pencetakan hasil. Koma setelah perintah terakhir dapat dihilangkan.
Baris perintah berikut hanya akan mencetak hasil ekspresi, bukan tugas atau perintah format.

\>r:=2; h:=4; pi\*r^2\*h/3

    16.7551608191

Perintah harus dipisahkan dengan yang kosong. Baris perintah berikut mencetak dua hasilnya.

\>pi\*2\*r\*h, %+2\*pi\*r\*h 

Ingat tanda % menyatakan hasil perhitungan terakhir sebelumnya

    50.2654824574
    100.530964915

Baris perintah dieksekusi dalam urutan yang ditekan pengguna kembali. Jadi Anda mendapatkan nilai baru setiap kali Anda menjalankan baris kedua.

\>x := 1;
\>x := cos(x) 

nilai cosinus (x dalam radian)

    0.540302305868

\>x := cos(x)

    0.857553215846

Jika dua garis terhubung dengan "..." kedua garis akan selalu dieksekusi secara bersamaan.

\>x := 1.5; ...  
\>   x := (x+2/x)/2, x := (x+2/x)/2, x := (x+2/x)/2, 

    1.41666666667
    1.41421568627
    1.41421356237

Ini juga merupakan cara yang baik untuk menyebarkan long command pada dua atau lebih baris. Anda dapat menekan Ctrl+Return untuk membagi garis menjadi dua pada posisi kursor saat ini, atau Ctrl+Back untuk menggabungkan garis.

Sedangkan untuk fold semua multi-garis tekan Ctrl + L. Kemudian garis-garis berikutnya hanya akan terlihat, jika salah satunya memiliki fokus. Untuk fold satu multi-baris, mulailah baris pertama dengan "%+".

\>%+ x=4+5; ...  
\>    // This line will not be visible once the cursor is off the line

A line starting with %% will be completely invisible.

    81

Euler Math Toolbox mendukung loop di baris perintah, selama mereka masuk ke dalam satu baris atau multi-baris. Dalam program, pembatasan ini tidak berlaku, tentu saja. Untuk informasi lebih lanjut lihat pengantar berikut.

\>x=1; for i=1 to 5; x := (x+2/x)/2, end; 

menghitung akar 2

    1.5
    1.41666666667
    1.41421568627
    1.41421356237
    1.41421356237

Tidak apa-apa untuk menggunakan multi-line. Pastikan baris diakhiri
dengan "...".

\>x := 1.5; // tambahkan komentar disini seblum  ...  
\>   repeat xnew:=(x+2/x)/2; until xnew~=x; ...  
\>      x := xnew; ...  
\>   end; ...  
\>   x,

    1.41421356237

Struktur bersyarat juga berfungsi.

\>if E^pi\>pi^E; then "Thought so!", endif;

    Thought so!

Saat Anda menjalankan perintah, kursor dapat berada di posisi mana pun di baris perintah. Anda dapat kembali ke perintah sebelumnya atau melompat ke perintah berikutnya dengan tombol panah. Atau Anda dapat mengklik ke bagian komentar di atas perintah untuk menuju ke perintah.

Saat Anda menggerakkan kursor di sepanjang garis, pasangan tanda kurung atau kurung buka dan tutup akan disorot. Dan juga, perhatikan baris status. Setelah kurung buka fungsi sqrt(), baris status akan menampilkan teks bantuan untuk fungsi tersebut. Jalankan perintah dengan tombol kembali.

\>sqrt(sin(10°)/cos(20°))

    0.429875017772

Untuk melihat bantuan untuk perintah terbaru, buka jendela bantuan dengan F1. Di sana, Anda dapat memasukkan teks untuk dicari. Pada baris kosong, bantuan untuk jendela bantuan akan ditampilkan. Anda dapat menekan escape untuk menghapus garis, atau untuk menutup jendela bantuan.

Anda dapat mengklik dua kali pada perintah apa pun untuk membuka bantuan untuk perintah ini. Coba klik dua kali perintah exp di bawah ini di baris perintah.

\>exp(log(2.5))

    2.5

Anda juga dapat menyalin dan menempel di Euler. Gunakan Ctrl-C dan Ctrl-V untuk ini. Untuk menandai teks, seret mouse atau gunakan shift bersamaan dengan tombol kursor. Selain itu, Anda dapat menyalin tanda kurung yang disorot.

# Sintak Dasar

Euler Math Toolbox tahu fungsi matematika yang biasa digunakan. Seperti yang Anda lihat di atas, fungsi trigonometri bekerja dalam radian atau derajat. Untuk mengonversi ke derajat, tambahkan simbol derajat (dengan tombol F7) ke dalam nilainya, atau gunakan fungsi rad(x). Fungsi akar kuadrat disebut sqrt dalam Euler. Tentu saja, x^(1/2) juga memungkinkan.

Untuk menyetel variabel, gunakan "=" atau ":=". Demi kejelasan, pengantar ini menggunakan bentuk yang terakhir/terbaru. Spasi tidak menjadi masalah. Tetapi spasi di antara perintah sangat diharapkan.

Beberapa perintah dalam satu baris dipisahkan dengan "," atau ";". Titik koma menekan output dari perintah. Di akhir baris perintah "," diasumsikan, jika ";" hilang.

\>g:=9.81; t:=2.5; 1/2\*g\*t^2

    30.65625

EMT menggunakan sintaks pemrograman untuk ekspresi. Untuk memasukkan
$$e^2 \cdot \left( \frac{1}{3+4 \log(0.6)}+\frac{1}{7} \right)$$Anda harus mengatur tanda kurung dengan benar dan menggunakan "/" untuk pecahan. Perhatikan tanda kurung yang disorot untuk bantuan.
Perhatikan bahwa konstanta Euler e diberi nama E dalam EMT.

\>E^2\*(1/(3+4\*log(0.6))+1/7)

    8.77908249441

Untuk menghitung ekspresi rumit seperti
$$\left(\frac{\frac17 + \frac18 + 2}{\frac13 + \frac12}\right)^2 \pi$$anda harus memasukkannya dalam bentuk baris.

\>((1/7 + 1/8 + 2) / (1/3 + 1/2))^2 \* pi

    23.2671801626

Letakkan tanda kurung dengan hati-hati di sekitar sub-ekspresi yang perlu dihitung terlebih dahulu. EMT membantu Anda dengan menyorot ekspresi bahwa braket penutup selesai. Anda juga harus memasukkan nama
"pi" untuk huruf Yunani pi.

Hasil dari perhitungan ini adalah bilangan floating point. Secara default dicetak dengan akurasi sekitar 12 digit. Di baris perintah berikut, kita juga belajar bagaimana kita bisa merujuk ke hasil sebelumnya dalam baris yang sama.

\>1/3+1/7, fraction %

    0.47619047619
    10/21

Perintah Euler dapat berupa ekspresi atau perintah primitif. Ekspresi terbuat dari operator dan fungsi. Jika diperlukan, hal tersebut harus berisi tanda kurung untuk memaksa urutan eksekusi yang benar. Jika
ragu, memasang braket atau tanda kurung adalah ide yang bagus. Perhatikan bahwa EMT menunjukkan tanda kurung buka dan tutup saat mengedit baris perintah.

\>(cos(pi/4)+1)^3\*(sin(pi/4)+1)^2

    14.4978445072

Operator numerik Euler meliputi

1. + unary or operator plus  
2. - unary or operator minus
3. * operator perkalian  
4. / operator pecahan  
5. . produk matriks  
6. a^b pangkat untuk a positif atau bilangan bulat b (a**b juga berfungsi)
7. n! operator faktorial
8. dan masih banyak lagi.

Berikut adalah beberapa fungsi yang mungkin Anda butuhkan. Ada banyak lagi.
 sin,cos,tan,atan,asin,acos,rad,deg  
 log,exp,log10,sqrt,logbase  
 bin,logbin,logfac,mod,floor,ceil,round,abs,sign  
 conj,re,im,arg,conj,real,complex  
 beta,betai,gamma,complexgamma,ellrf,ellf,ellrd,elle  
 bitand,bitor,bitxor,bitnot  

Beberapa perintah memiliki alias, misalnya ln untuk log.

\>ln(E^2), arctan(tan(0.5))

    2
    0.5

\>sin(30°)

    0.5

Pastikan untuk menggunakan tanda kurung (kurung bulat), setiap kali ada keraguan tentang urutan eksekusi! Berikut ini tidak sama dengan (2^3)^4, yang merupakan default untuk 2^3^4 di EMT (beberapa sistem numerik melakukannya dengan cara lain).

\>2^3^4, (2^3)^4, 2^(3^4)

    2.41785163923e+24
    4096
    2.41785163923e+24

# Bilangan Asli

Tipe data utama dalam Euler adalah bilangan real. Real direpresentasikan dalam format IEEE dengan akurasi sekitar 16 digit desimal.

\>longest 1/3

         0.3333333333333333 

Representasi ganda internal membutuhkan 8 byte.

Representasi ganda adalah format penyimpanan untuk floating-point yang
menggunakan 64 bit(8 byte).

\>printdual(1/3)

    1.0101010101010101010101010101010101010101010101010101*2^-2

\>printhex(1/3)

    5.5555555555554*16^-1

Perbedaan 'printdual' dan 'printhex' adalah 'printdual' yakni mencetak representasi internal dari sebuah bilangan floating-point dalam format presisi ganda (pendekatan yang sangat dekat dengan nilai aslinya tetapi tidak persis sama.) meskipun ia tergantung pada konteks bahasa pemograman tertentu. sedangkan 'printhex' yakni representasi dari nilai floating-point dalam bentuk heksadesimal(basis 16), heksadesimal ini adalah cara yang lebih ringkas untuk menampilkan nilai biner karena setiap digit heksadesimal mempresentasikan empat digit biner.

# Strings

Sebuah string dalam Euler didefinisikan dengan "..."

\>"A string can contain anything."

    A string can contain anything.

String dapat digabungkan dengan | atau dengan +. Ini juga berfungsi dengan angka, yang dikonversi menjadi string dalam kasus itu.

\>"The area of the circle with radius " + 2 + " cm is " + pi\*4 + " cm^2."

    The area of the circle with radius 2 cm is 12.5663706144 cm^2.

Pada String fungsi print mengonversi angka menjadi string. Ini dapat mengambil sejumlah digit dan sejumlah tempat (0 untuk keluaran padat), dan secara optimal satu unit

\>"Golden Ratio : " + print((1+sqrt(5))/2,5,0)

    Golden Ratio : 1.61803

Ada string khusus 'none', yang tidak mencetak. Dikembalikan oleh beberapa fungsi, ketika hasilnya tidak penting. (Dikembalikan secara otomatis, jika fungsi tidak memiliki pernyataan pengembalian).

\>none

Untuk mengonversi string menjadi angka, cukup mengevaluasinya. Ini bekerja untuk ekspresi juga (lihat dibawah).

\>"1234.5"()

    1234.5

Untuk mendefinisikan vektor string, gunakan notasi vektor [...]

\>v:=["affe","charlie","bravo"]

    affe
    charlie
    bravo

Vektor string kosong dilambangkan dengan [none]. Dan vektor string dapat digabungkan dengan '|'.

\>w:=[none]; w|v|v

    affe
    charlie
    bravo
    affe
    charlie
    bravo

String dapat berisi karakter Unicode. Secara internal, string ini berisi kode UTF-8. untuk menghasilkan string seperti itu, gunakan u"..." dan salah satu entitas HTML.

String Unicode dapat digabungkan seperti string lainnya.

\>u"&alpha; = " + 45 + u"&deg;" // pdfLaTeX mungkin gagal menampilkan secara benar

    α = 45°

Dalam komentar, entitas yang sama seperti α, β etc. dapat digunakan. Ini mungkin merupakan alternatif cepat untuk Lateks. (Detail lebih lanjut pada komentar di bawah).

Ada beberapa fungsi untuk membuat atau menganalisis string unicode.

Fungsi strtochsr() akan mengenali string Unicode, dan menerjemahkannya dengan benar.

\>v=strtochar(u"&Auml; is a German letter")

    [196,  32,  105,  115,  32,  97,  32,  71,  101,  114,  109,  97,  110,
    32,  108,  101,  116,  116,  101,  114]

Perintah ini menghasilkan array atau daftar angka berupa vektor angka yang mewakili karakter dalam string dalam bentuk kode Unicode.

Fungsi kebalikannya adalah chartoutf().

\>v[1]=strtochar(u"&Uuml;")[1]; chartoutf(v)

    Ü is a German letter

Fungsi utf()dapat menerjemahkan string dengan entitas dalam variabel menjadi string Unicode.

\>s="We have &alpha;=&beta;."; utf(s) // pdfLaTeX mungkin gagal menampilkan secara benar

    We have α=β.

Memungkinkan juga untuk menggunakan entitas numerik.

\>u"&#196;hnliches"

    Ähnliches

# Nilai Boolean

Nilai boolean direpresentasikan dengan 1=true atau 0=false dalam euler. String dapat dibandingkan, seperti halnya angka.

\>2<1, "apel"<"banana"

    0
    1

"and" adalah operator "&amp;&amp;" dan "or" adalah operator "||", seperti dalam bahasa C. (kata "and" dan "or" hanya dapat digunakan dalam kondisi "if".)

\>2<E && E<3

    1

Operator Boolean mematuhi aturan bahasa matriks

\>(1:10)\>5, nonzeros(%)

    [0,  0,  0,  0,  0,  1,  1,  1,  1,  1]
    [6,  7,  8,  9,  10]

Anda dapat menggunakan fungsi nonzeros() untuk mengekstrak elemen tertentu dari sebuah vektor. Pada contoh, kita menggunakan kondisional isprime(n).

\>N=2|3:2:99 // N berisi elemen 2 dan bilangan2 ganjil dari 3 s.d. 99

    [2,  3,  5,  7,  9,  11,  13,  15,  17,  19,  21,  23,  25,  27,  29,
    31,  33,  35,  37,  39,  41,  43,  45,  47,  49,  51,  53,  55,  57,
    59,  61,  63,  65,  67,  69,  71,  73,  75,  77,  79,  81,  83,  85,
    87,  89,  91,  93,  95,  97,  99]

\>N[nonzeros(isprime(N))] //pilih anggota2 N yang prima

    [2,  3,  5,  7,  11,  13,  17,  19,  23,  29,  31,  37,  41,  43,  47,
    53,  59,  61,  67,  71,  73,  79,  83,  89,  97]

# Output Formats

Default output formats EMT adalah 12 digit. Untuk memastikan yang kita lihat adalah bentuk default, maka perlu direset format.

\>defformat; pi

    3.14159265359

Secara internal, EMT menggunakan standar IEEE (Institute of Electrical and Electronics Engineers) untuk bilangan ganda dengan sekitar 16 digit desimal. Untuk melihat bentuk digit penuh, gunakan perintah "longestformat" atau gunakan operator "longest" untuk memunculkannya.

\>longest pi

          3.141592653589793 

Berikut ini adalah repesentasi heksadesimal internal dari bilangan ganda.

\>printhex(pi)

    3.243F6A8885A30*16^0

Format output dapat diubah secara permanen dengan perintah format.

\>format(12,5); 1/3, pi, sin(1)

        0.33333 
        3.14159 
        0.84147 

Format standarnya adalah 12.

\>format(12); 1/3

    0.333333333333

Fungsi seperti “shortestformat”, “shortformat”, “longformat” bekerja untuk vektor dengan cara berikut.

\>shortestformat; random(3,8)

      0.66    0.2   0.89   0.28   0.53   0.31   0.44    0.3 
      0.28   0.88   0.27    0.7   0.22   0.45   0.31   0.91 
      0.19   0.46  0.095    0.6   0.43   0.73   0.47   0.32 

Format standar untuk skalar adalah 12, tetapi ini dapat diubah.

\>setscalarformat(5); pi

    3.1416

Fungsi “longestformat” juga menetapkan format skalar.

\>longestformat; pi

    3.141592653589793

Sebagai referensi, berikut ini daftar format output yang paling penting.
1. shortestformat shortformat longformat, longestformat
2. format(length,digits) goodformat(length)
3. fracformat(length)
4. defformat

Akurasi internal EMT adalah sekitar 16 tempat desimal, yang merupakan standar IEEE. Angka disimpan dalam format internal ini.

Tetapi format output EMT dapat diatur dengan cara yang fleksibel.

\>longestformat; pi,

    3.141592653589793

\>format(10,5); pi

      3.14159 

The default is defformat().

\>defformat; // default

Ada operator pendek yang hanya mencetak satu nilai. Operator “longest” akan mencetak semua digit angka yang valid.

\>longest pi^2/2

          4.934802200544679 

Ada juga operator singkat untuk mencetak hasil dalam format pecahan. Kami sudah menggunakannya di atas.

\>fraction 1+1/2+1/3+1/4

    25/12

Karena format internal menggunakan cara biner untuk menyimpan angka, maka nilai 0,1 tidak akan terwakili dengan tepat. Kesalahan bertambah sedikit, seperti yang Anda lihat dalam perhitungan berikut ini.

\>longest 0.1+0.1+0.1+0.1+0.1+0.1+0.1+0.1+0.1+0.1-1

     -1.110223024625157e-16 

Tetapi, dengan “longformat” default, Anda tidak akan melihat hal ini. Untuk kenyamanan, output angka yang sangat kecil adalah 0.

\>0.1+0.1+0.1+0.1+0.1+0.1+0.1+0.1+0.1+0.1-1

    0

# Expressions

Strings atau names dapat digunakan untuk menyimpan ekspresi matematika, yang dapat dievaluasi oleh EMT. Untuk ini, gunakan tanda kurung setelah ekspresi. Jika Anda bermaksud menggunakan string sebagai ekspresi, gunakan konvensi untuk menamainya “fx” atau “fxy”, dll. Ekspresi lebih diutamakan daripada fungsi.

Variabel global dapat digunakan dalam evaluasi.

\>r:=2; fx:="pi\*r^2"; longest fx()

          12.56637061435917 

Parameter ditetapkan ke x, y, dan z dalam urutan tersebut. Parameter tambahan dapat ditambahkan dengan menggunakan parameter yang ditetapkan.

\>fx:="a\*sin(x)^2"; fx(5,a=-1)

    -0.919535764538

Perhatikan bahwa ekspresi akan selalu menggunakan variabel global, meskipun ada variabel dalam fungsi dengan nama yang sama. (Jika tidak, evaluasi ekspresi dalam fungsi dapat memberikan hasil yang sangat membingungkan bagi pengguna yang memanggil fungsi tersebut).

\>at:=4; function f(expr,x,at) := expr(x); ...  

\>   f("at\*x^2",3,5) // computes 4\*3^2 not 5\*3^2

    36

Jika Anda ingin menggunakan nilai lain untuk “at” selain nilai global, Anda perlu menambahkan “at=value”.

\>at:=4; function f(expr,x,a) := expr(x,at=a); ...  

\>   f("at\*x^2",3,5)

    45

Sebagai referensi, kami menyatakan bahwa koleksi panggilan (dibahas di tempat lain) dapat berisi ekspresi. Jadi kita dapat membuat contoh di atas sebagai berikut.

\>at:=4; function f(expr,x) := expr(x); ...  

\>   f({{"at\*x^2",at=5}},3)

    45

Ekspresi dalam x sering digunakan seperti halnya fungsi.

Perhatikan bahwa mendefinisikan fungsi dengan nama yang sama seperti ekspresi simbolik global akan menghapus variabel ini untuk menghindari kebingungan antara ekspresi simbolik dan fungsi.

\>f &= 5\*x;

\>function f(x) := 6\*x;

\>f(2)

    12

Sesuai dengan konvensi, ekspresi simbolik atau numerik harus diberi nama fx, fxy, dll. Skema penamaan ini tidak boleh digunakan untuk fungsi.

\>fx &= diff(x^x,x); $&fx
$$x^{x}\,\left(\log x+1\right)$$Bentuk khusus dari sebuah ekspresi memungkinkan variabel apa pun sebagai parameter tanpa nama untuk evaluasi ekspresi, bukan hanya “x”, “y”, dll. Untuk ini, mulailah ekspresi dengan “@(variabel)...”.

\>"@(a,b) a^2+b^2", %(4,5)

    @(a,b) a^2+b^2
    41

Hal ini memungkinkan untuk memanipulasi ekspresi dalam variabel lain untuk fungsi EMT yang membutuhkan ekspresi dalam “x”.

Cara paling dasar untuk mendefinisikan fungsi sederhana adalah dengan menyimpan rumusnya dalam ekspresi simbolik atau numerik. Jika variabel utamanya adalah x, ekspresi tersebut dapat dievaluasi seperti halnya
sebuah fungsi.

Seperti yang Anda lihat pada contoh berikut, variabel global terlihat selama evaluasi 

\>fx &= x^3-a\*x;  ...  
\>   a=1.2; fx(0.5)

    -0.475

Semua variabel lain dalam ekspresi dapat ditentukan dalam evaluasi menggunakan parameter yang ditetapkan.

\>fx(0.5,a=1.1)

    -0.425

Sebuah ekspresi tidak perlu simbolis. Ini diperlukan, jika ekspresi berisi fungsi, yang hanya diketahui di kernel numerik, bukan di Maxima.

# Symbolic Mathematics

EMT melakukan matematika simbolik dengan bantuan Maxima. Untuk detailnya, mulailah dengan tutorial berikut ini, atau telusuri referensi untuk Maxima. Para ahli dalam Maxima harus mencatat bahwa ada perbedaan dalam sintaks antara sintaks asli Maxima dan sintaks default ekspresi simbolik dalam EMT.

Matematika simbolik diintegrasikan dengan mulus ke dalam Euler dengan &amp;. Setiap ekspresi yang dimulai dengan &amp; adalah ekspresi simbolik. Ekspresi ini dievaluasi dan dicetak oleh Maxima.

Pertama-tama, Maxima memiliki aritmatika "tak terbatas" yang dapat menangani angka yang sangat besar.

\>$&44!
$$2658271574788448768043625811014615890319638528000000000$$Dengan cara ini, kita dapat menghitung hasil yang besar dengan tepat.
Mari kita hitung !
$$C(44,10) = \frac{44!}{34! \cdot 10!}$$\>$& 44!/(34!\*10!) // nilai C(44,10)
$$2481256778$$Tentu saja, Maxima memiliki fungsi yang lebih efisien untuk hal ini (seperti halnya bagian numerik EMT).

\>$binomial(44,10) //menghitung C(44,10) menggunakan fungsi binomial()
$$2481256778$$Untuk mempelajari lebih lanjut tentang fungsi tertentu klik dua kali di atasnya. Misalnya, coba klik dua kali pada "&amp;binomial" di baris perintah sebelumnya. Ini membuka dokumentasi Maxima seperti yang
disediakan oleh penulis program itu.

Anda akan belajar bahwa yang berikut ini juga berfungsi.
$$C(x,3)=\frac{x!}{(x-3)!3!}=\frac{(x-2)(x-1)x}{6}$$\>$binomial(x,3) // C(x,3)
$$\frac{\left(x-2\right)\,\left(x-1\right)\,x}{6}$$Jika Anda ingin mengganti x dengan nilai tertentu, gunakan “with”.

\>$&binomial(x,3) with x=10 // substitusi x=10 ke C(x,3)
$$120$$Dengan begitu, Anda dapat menggunakan solusi dari sebuah persamaan dalam persamaan lain.

Ekspresi simbolik dicetak oleh Maxima dalam bentuk 2D. Alasannya adalah sebuah bendera simbolik khusus dalam string.
Seperti yang telah Anda lihat pada contoh sebelumnya dan contoh berikut, jika Anda telah menginstal LaTeX, Anda dapat mencetak ekspresi simbolik dengan Latex. Jika tidak, perintah berikut ini akan mengeluarkan pesan kesalahan.
Untuk mencetak ekspresi simbolik dengan LaTeX, gunakan $ di depan &amp; (atau Anda dapat menghilangkan &amp;) sebelum perintah. Jangan jalankan perintah Maxima dengan $, jika Anda tidak memiliki LaTeX.

\>$(3+x)/(x^2+1)
$$\frac{x+3}{x^2+1}$$Ekspresi simbolik diuraikan oleh Euler. Jika Anda membutuhkan sintaks yang kompleks dalam satu ekspresi, Anda dapat mengapit ekspresi dalam “...”. Menggunakan lebih dari satu ekspresi sederhana dimungkinkan, tetapi sangat tidak disarankan.

\>&"v := 5; v^2"
    
                                      25    

Untuk kelengkapan, kami menyatakan bahwa ekspresi simbolik dapat digunakan dalam program, tetapi harus diapit dengan tanda kutip. Selain itu, akan jauh lebih efektif untuk memanggil Maxima pada saat kompilasi jika memungkinkan.

\>$&expand((1+x)^4), $&factor(diff(%,x)) // diff: turunan, factor: faktor
$$4\,\left(x+1\right)^3$$
Sekali lagi, % mengacu pada hasil sebelumnya.

Untuk mempermudah, kita menyimpan solusi ke dalam sebuah variabel simbolik. Variabel simbolik didefinisikan dengan “&amp;=”.

\>fx &= (x+1)/(x^4+1); $&fx
$$\frac{x+1}{x^4+1}$$Ekspresi simbolik dapat digunakan dalam ekspresi simbolik lainnya.

\>$&factor(diff(fx,x))
$$\frac{-3\,x^4-4\,x^3+1}{\left(x^4+1\right)^2}$$Masukan langsung dari perintah Maxima juga tersedia. Mulai baris perintah dengan “::”. Sintaks Maxima disesuaikan dengan sintaks EMT (disebut “mode kompatibilitas”).

\>&factor(20!)

                             2432902008176640000
    
\>::: factor(10!)
    
                                   8  4  2
                                  2  3  5  7
    
\>:: factor(20!)

                            18  8  4  2
                           2   3  5  7  11 13 17 19
    
Jika Anda adalah seorang ahli dalam Maxima, Anda mungkin ingin menggunakan sintaks asli Maxima. Anda dapat melakukan ini dengan “:::”.

\>::: av:g$ av^2;
    
                                       2
                                      g
    
\>fx &= x^3\*exp(x), $fx
    
                                     3  x
                                    x  E

$$x^3\,e^{x}$$Variabel tersebut dapat digunakan dalam ekspresi simbolik lainnya. Perhatikan, bahwa pada perintah berikut ini, sisi kanan dari &amp;= dievaluasi sebelum penugasan ke Fx.

\>&(fx with x=5), $%, &float(%)
    
                                         5
                                    125 E
$$125\,e^5$$
                              18551.64488782208
    
\>fx(5)

    18551.6448878

Untuk mengevaluasi ekspresi dengan nilai variabel tertentu, Anda dapat menggunakan operator “with”.
Baris perintah berikut ini juga mendemonstrasikan bahwa Maxima dapat mengevaluasi sebuah ekspresi secara numerik dengan float().

\>&(fx with x=10)-(fx with x=5), &float(%)
    
                                    10        5
                              1000 E   - 125 E
    
    
                             2.20079141499189e+7
    
\>$factor(diff(fx,x,2))
$$x\,\left(x^2+6\,x+6\right)\,e^{x}$$Untuk mendapatkan kode Latex untuk sebuah ekspresi, Anda dapat menggunakan perintah tex.

\>tex(fx)

    x^3\,e^{x}

Ekspresi simbolik dapat dievaluasi seperti halnya ekspresi numerik.

\>fx(0.5)

    0.206090158838

Dalam ekspresi simbolik, hal ini tidak dapat dilakukan, karena Maxima tidak mendukungnya. Sebagai gantinya, gunakan sintaks “with” (bentuk yang lebih baik dari perintah at(...) pada Maxima).

\>$&fx with x=1/2
$$\frac{\sqrt{e}}{8}$$Penugasan ini juga bisa bersifat simbolis.

\>$&fx with x=1+t

$$\left(t+1\right)^3\,e^{t+1}$$Perintah "solve" menyelesaikan ekspresi simbolik untuk sebuah variabel di Maxima. Hasilnya adalah sebuah vektor solusi.

\>$&solve(x^2+x=4,x)

$\left[ x=\frac{-\sqrt{17}-1}{2} , x=\frac{\sqrt{17}-1}{2} \right] $$

Bandingkan dengan perintah “solve” numerik di Euler, yang membutuhkan nilai awal, dan secara opsional nilai target.

\>solve("x^2+x",1,y=4)

    1.56155281281

Nilai numerik dari solusi simbolik dapat dihitung dengan evaluasi hasil simbolik. Euler akan membaca penugasan x= dst. Jika Anda tidak membutuhkan hasil numerik untuk perhitungan lebih lanjut, Anda juga bisa membiarkan Maxima menemukan nilai numeriknya

\>sol &= solve(x^2+2\*x=4,x); $&sol, sol(), $&float(sol)

$\left[ x=-\sqrt{5}-1 , x=\sqrt{5}-1 \right] $$    [-3.23607,  1.23607]

$\left[ x=-3.23606797749979 , x=1.23606797749979 \right] $$

Untuk mendapatkan solusi simbolik yang spesifik, seseorang dapat
menggunakan “with” dan indeks.

\>$&solve(x^2+x=1,x), x2 &= x with %[2]; $&x2
$$\frac{\sqrt{5}-1}{2}$$

Untuk menyelesaikan sistem persamaan, gunakan vektor persamaan.
Hasilnya adalah vektor solusi.

\>sol &= solve([x+y=3,x^2+y^2=5],[x,y]); $&sol, $&x\*y with sol[1]
$$2$$
Ekspresi simbolik dapat memiliki flags, yang menunjukkan perlakuan khusus di Maxima. Beberapa flag dapat digunakan sebagai perintah juga, namun ada juga yang tidak. Flags ditambahkan dengan “|” (bentuk yang lebih baik dari “ev(...,flags)”)

\>$& diff((x^3-1)/(x+1),x) //turunan bentuk pecahan
$$\frac{3\,x^2}{x+1}-\frac{x^3-1}{\left(x+1\right)^2}$$\>$& diff((x^3-1)/(x+1),x) | ratsimp //menyederhanakan pecahan
$$\frac{2\,x^3+3\,x^2+1}{x^2+2\,x+1}$$\>$&factor(%)
$$\frac{2\,x^3+3\,x^2+1}{\left(x+1\right)^2}$$

# Fungsi

Di EMT fungsi adalah program yang didefenisikan dengan perintah "function". Fungsi dapat menjadi fungsi satu baris atau fungsi multi baris. Fungsi satu baris dapat berupa numerik atau simbolis. Fungsi satu baris didefinisikan oleh ":=".

\>function f(x) := x\*sqrt(x^2+1)

Sebagai gambaran umum, kami menunjukkan semua definisi yang mungkin untuk fungsi satu baris. Sebuah fungsi dapat dievaluasi seperti halnya fungsi Euler bawaan.

\>f(2)

    4.472135955

Fungsi ini dapat digunakan juga dalam vektor, dengan mengikuti aturan bahasa matrik Euler, karena ekspresi yang digunakan dalam fungsi divektorkan.Kita akan mencobanya menggunakan fungsi f di atas.

\>f(0:0.1:1)

    [0,  0.100499,  0.203961,  0.313209,  0.430813,  0.559017,  0.699714,
    0.854459,  1.0245,  1.21083,  1.41421]

Fungsi juga dapat menjadi plot, hanya dengan memberikan nama fungsi.
Berbeda dengan ekpresi simbolik atau numerik, nama fungsi harus diberikan dalam string.

\>solve("f",1,y=1)

    0.786151377757

Secara default, jika Anda perlu menimpa fungsi built-in, Anda harus menambahkan kata kunci “overwrite”. Menimpa fungsi bawaan berbahaya dan dapat menyebabkan masalah bagi fungsi lain yang bergantung pada fungsi tersebut.
Anda masih dapat memanggil fungsi bawaan sebagai “_...”, jika fungsi tersebut merupakan fungsi dalam inti Euler.

\>function overwrite sin (x) := \_sin(x°) // redine sine in degrees

\>sin(45)

    0.707106781187

Jika ingin menghapus definisi dari sin dan mendefinisikannya ulang, menggunakan perintah "forget"

\>forget sin; sin(pi/4)

    0.707106781187

# Default Parameters

Parameter default adalah fungsi parameter yang memiliki nilai awal.
Fungsi numerik dapat memiliki parameter default.

\>function f(x,a=1) := a\*x^2

Menghilangkan parameter ini menggunakan nilai default.

\>f(4)

    16

Menetapkannya akan menimpa nilai default.

\>f(4,5)

    80

Parameter yang ditetapkan juga menimpanya. Ini digunakan oleh banyak fungsi Euler seperti plot2d, plot3d.

\>f(4,a=1)

    16

Jika sebuah variabel bukan parameter, maka variabel tersebut harus bersifat global. Fungsi satu baris dapat melihat variabel global.

\>function f(x) := a\*x^2
\>a=6; f(2)

    24

Tetapi parameter yang ditetapkan akan menggantikan nilai global. Jika argumen tidak ada dalam daftar parameter yang telah ditetapkan sebelumnya, argumen tersebut harus dideklarasikan dengan “:=”!

\>f(2,a:=5)

    20

Fungsi simbolik didefinisikan dengan “&amp;=”. Fungsi-fungsi ini didefinisikan dalam Euler dan Maxima, dan dapat digunakan di kedua bahasa tersebut. Ekspresi pendefinisian dijalankan melalui Maxima sebelum definisi.

\>function g(x) &= x^3-x\*exp(-x); $&g(x)
$$x^3-x\,e^ {- x }$$Fungsi simbolik dapat digunakan dalam ekspresi simbolik

\>$&diff(g(x),x), $&% with x=4/3
$$\frac{e^ {- \frac{4}{3} }}{3}+\frac{16}{3}$$

Itu juga dapat digunakan dalam ekspresi numerik. Tentu saja, ini hanya akan berfungsi jika EMT dapat mengintrepertasikan semua yang ada di dalam fungsi tersebut.

\>g(5+g(1))

    178.635099908

Itu juga dapat digunakan untuk mendefinisikan fungsi atau ekspresi simbolik lainnya.

\>function G(x) &= factor(integrate(g(x),x)); $&G(c) // integrate: mengintegralkan
$$\frac{e^ {- c }\,\left(c^4\,e^{c}+4\,c+4\right)}{4}$$\>solve(&g(x),0.5)

    0.703467422498

Berikut ini juga berfungsi, karena Euler menggunakan ekspresi simbolis dalam fungsi g, jika tidak menemukan variabel simbolik g, dan jika ada fungsi simbolis g.

\>solve(&g,0.5)

    0.703467422498

\>function P(x,n) &= (2\*x-1)^n; $&P(x,n)
$$\left(2\,x-1\right)^{n}$$\>function Q(x,n) &= (x+2)^n; $&Q(x,n)
$$\left(x+2\right)^{n}$$\>$&P(x,4), $&expand(%)
$$16\,x^4-32\,x^3+24\,x^2-8\,x+1$

\>P(3,4)

    625

\>$&P(x,4)+ Q(x,3), $&expand(%)
$$16\,x^4-31\,x^3+30\,x^2+4\,x+9$$

\>$&P(x,4)-Q(x,3), $&expand(%), $&factor(%)
$$16\,x^4-33\,x^3+18\,x^2-20\,x-7$$

\>$&P(x,4)\*Q(x,3), $&expand(%), $&factor(%)
$$\left(x+2\right)^3\,\left(2\,x-1\right)^4$$


\>$&P(x,4)/Q(x,1), $&expand(%), $&factor(%)
$$\frac{\left(2\,x-1\right)^4}{x+2}$$
\>function f(x) &= x^3-x; $&f(x)
$$x^3-x$$Dengan &amp;= fungsinya simbolis, dan dapat digunakan dalam ekspresi simbolik lainnya. Contohnya dalam integral tak tentu sebagai berikut.

\>$&integrate(f(x),x)
$$\frac{x^4}{4}-\frac{x^2}{2}$$Dengan := fungsinya numerik. Contoh yang baik adalah integral tak tentu seperti
$$f(x) = \int_1^x t^t \, dt,$$
yang tidak dapat dievaluasi secara simbolik.

Jika kita mendefinisikan ulang fungsi tersebut dengan kata kunci “map”, maka fungsi ini dapat digunakan untuk vektor x. Secara internal, fungsi ini dipanggil untuk semua nilai x satu kali, dan hasilnya disimpan dalam sebuah vektor. 

\>function map f(x) := integrate("x^x",1,x)
\>f(0:0.5:2)

    [-0.783431,  -0.410816,  0,  0.676863,  2.05045]

Fungsi dapat memiliki nilai default untuk parameter.

\>function mylog (x,base=10) := ln(x)/ln(base);

Sekarang fungsi dapat dipanggil dengan menggunakan suatau parameter "base" maupun tidak.

\>mylog(100), mylog(2^6.7,2)

    2
    6.7

Selain itu, dimungkinkan untuk menggunakan parameter yang ditetapkan.

\>mylog(E^2,base=E)

    2

Sering kali, kita ingin menggunakan fungsi untuk vektor di satu tempat, dan untuk elemen individual di tempat lain. Ini tapat terjadi dengan vektor parameter.

\>function f([a,b]) &= a^2+b^2-a\*b+b; $&f(a,b), $&f(x,y)
$$y^2-x\,y+y+x^2$$

Fungsi simbolik seperti itu dapat digunakan untuk variabel simbolik.
Tetapi fungsi ini juga dapat digunakan untuk vektor numerik.

\>v=[3,4]; f(v)

    17

Ada juga fungsi yang murni simbolis, yang tidak dapat digunakan secara numerik.

\>function lapl(expr,x,y) &&= diff(expr,x,2)+diff(expr,y,2)//turunan parsial kedua
    
                     diff(expr, y, 2) + diff(expr, x, 2)
    
\>$&realpart((x+I\*y)^4), $&lapl(%,x,y)
$$0$$

Tetapi tentu saja, mereka dapat digunakan dalam ekspresi simbolis atau dalam definisi fungsi simbolis.

\>function f(x,y) &= factor(lapl((x+y^2)^5,x,y)); $&f(x,y)
$$10\,\left(y^2+x\right)^3\,\left(9\,y^2+x+2\right)$$Ringkasan: 
1. &amp;= mendefinisikan fungsi simbolis,
2. := mendefinisikan fungsi numerik,
3. &amp;&amp;= mendefinisikan fungsi simbolis murni

# Memecahkan Ekspresi

Ekspresi dapat diselesaikan secara numerik dan simbolis. Untuk menyelesaikan ekspresi sederhana dari satu variabel, kita dapat menggunakan fungsi solve(). Perlu nilai awal untuk memulai pencarian. Secara internal, solve() menggunakan metode secant.

\>solve("x^2-2",1)

    1.41421356237

Ini juga berfungsi untuk fungsi simbolik, perhatikan fungsi berikut ini.

\>$&solve(x^2=2,x)

$\left[ x=-\sqrt{2} , x=\sqrt{2} \right] $$

\>$&solve(x^2-2,x)

$\left[ x=-\sqrt{2} , x=\sqrt{2} \right] $$

\>$&solve(a\*x^2+b\*x+c=0,x)

$\left[ x=\frac{-\sqrt{b^2-4\,a\,c}-b}{2\,a} , x=\frac{\sqrt{b^2-4\,  a\,c}-b}{2\,a} \right] $$

\>$&solve([a\*x+b\*y=c,d\*x+e\*y=f],[x,y])

$\left[ \left[ x=-\frac{c\,e}{b\,\left(d-5\right)-a\,e} , y=\frac{c  \,\left(d-5\right)}{b\,\left(d-5\right)-a\,e} \right]  \right] $$

\>px &= 4\*x^8+x^7-x^4-x; $&px
$$4\,x^8+x^7-x^4-x$$Sekarang kita mencari titik, di mana polinomialnya adalah 2. Dalam solve(), nilai target default y=0 dapat diubah dengan variabel yang ditetapkan.

Kami menggunakan y=2 dan memeriksa dengan mengevaluasi polinomial pada hasil sebelumnya.

\>solve(px,1,y=2), px(%)

    0.966715594851
    2

Memecahkan ekspresi simbolis dalam bentuk simbolis mengembalikan daftar solusi. Kami menggunakan pemecah simbolik solve() yang disediakan oleh Maxima.

\>sol &= solve(x^2-x-1,x); $&sol

$\left[ x=\frac{1-\sqrt{5}}{2} , x=\frac{\sqrt{5}+1}{2} \right] $$

Cara termudah untuk mendapatkan nilai numerik adalah dengan mengevaluasi solusi secara numerik seperti ekspresi.

\>longest sol()

        -0.6180339887498949       1.618033988749895 

Untuk menggunakan solusi secara simbolis dalam ekspresi lain, cara termudah adalah "with".

\>$&x^2 with sol[1], $&expand(x^2-x-1 with sol[2])
$$0$$

Memecahkan sistem persamaan secara simbolis dapat dilakukan dengan vektor persamaan dan solver simbolis solve(). Hasilnya dalam bentuk persamaan.

\>$&solve([x+y=2,x^3+2\*y+x=4],[x,y])

$\left[ \left[ x=-1 , y=3 \right]  , \left[ x=1 , y=1 \right]  ,   \left[ x=0 , y=2 \right]  \right] $$

Fungsi f() dapat melihat variabel global. Namun seringkali kita ingin menggunakan parameter lokal.
$$a^x-x^a = 0.1$$dengan a=3.
\>function f(x,a) := x^a-a^x;

Salah satu cara untuk mengoper parameter tambahan ke f() adalah dengan menggunakan sebuah daftar dengan nama fungsi dan parameternya (cara-cara lainnya adalah parameter titik koma).

\>solve({{"f",3}},2,y=0.1)

    2.54116291558

Ini juga bekerja dengan ekspresi. Tapi daftar elemen yang ada harus digunakan. (Lebih lanjut tentang daftar dalam tutorial tentang sintaks EMT).

\>solve({{"x^a-a^x",a=3}},2,y=0.1)

    2.54116291558

# Menyelesaikan Pertidaksamaan

Untuk menyelesaikan pertidaksamaan, EMT tidak akan dapat melakukannya, melainkan dengan bantuan Maxima, artinya secara eksak (simbolik). Perintah Maxima yang digunakan adalah fourier_elim(), yang harus dipanggil dengan perintah "load(fourier_elim)" terlebih dahulu.

\>&load(fourier\_elim)

            D:/Euler x64/maxima/share/maxima/5.35.1/share/fourier_elim/fo\
    urier_elim.lisp
    
\>$&fourier\_elim([x^2 - 1\>0],[x]) // x^2-1 \> 0

$\left[ 1<x \right] \lor \left[ x<-1 \right] $$

\>$&fourier\_elim([x^2 - 1<0],[x]) // x^2-1 < 0

$\left[ -1<x , x<1 \right] $$

\>$&fourier\_elim([x^2 - 1 # 0],[x]) // x^-1 <\> 0

$\left[ -1<x , x<1 \right] \lor \left[ 1<x \right] \lor \left[ x<-1   \right] $$

\>$&fourier\_elim([x # 6],[x])

$\left[ x<6 \right] \lor \left[ 6<x \right] $$

\>$&fourier\_elim([x < 1, x \> 1],[x]) // tidak memiliki penyelesaian
$${\it emptyset}$$\>$&fourier\_elim([minf < x, x < inf],[x]) // solusinya R
$${\it universalset}$$\>$&fourier\_elim([x^3 - 1 \> 0],[x])

$\left[ 1<x , x^2+x+1>0 \right] \lor \left[ x<1 , -x^2-x-1>0   \right] $$

\>$&fourier\_elim([cos(x) < 1/2],[x]) // ??? gagal

$\left[ 1-2\,\cos x>0 \right] $$

\>$&fourier\_elim([y-x < 5, x - y < 7, 10 < y],[x,y]) // sistem pertidaksamaan

$\left[ y-5<x , x<y+7 , 10<y \right] $$

\>$&fourier\_elim([y-x < 5, x - y < 7, 10 < y],[y,x])

$\left[ {\it max}\left(10 , x-7\right)<y , y<x+5 , 5<x \right] $$

\>$&fourier\_elim((x + y < 5) and (x - y \>8),[x,y])

$\left[ y+8<x , x<5-y , y<-\frac{3}{2} \right] $$

\>$&fourier\_elim(((x + y < 5) and x < 1) or  (x - y \>8),[x,y])

$\left[ y+8<x \right] \lor \left[ x<{\it min}\left(1 , 5-y\right)   \right] $$

\>&fourier\_elim([max(x,y) \> 6, x # 8, abs(y-1) \> 12],[x,y])
    
            [6 &lt; x, x &lt; 8, y &lt; - 11] or [8 &lt; x, y &lt; - 11]
     or [x &lt; 8, 13 &lt; y] or [x = y, 13 &lt; y] or [8 &lt; x, x &lt; y, 13 &lt; y]
     or [y &lt; x, 13 &lt; y]    

\>$&fourier\_elim([(x+6)/(x-9) <= 6],[x])

$\left[ x=12 \right] \lor \left[ 12<x \right] \lor \left[ x<9   \right] $$ 

# Bahasa Matriks

Dokumentasi inti EMT berisi diskusi terperinci tentang bahasa matriks Euler.
Vektor dan matriks dimasukkan dengan tanda kurung siku, elemen dipisahkan dengan koma, baris dipisahkan dengan titik koma.

\>A=[1,2;3,4]

                1             2 
                3             4 

Hasil kali matriks dilambangkan dengan sebuah titik.

\>b=[3;4]

                3 
                4 

\>b' // transpose b

    [3,  4]

\>inv(A) //inverse A

               -2             1 
              1.5          -0.5 

\>A.b //perkalian matriks

               11 
               25 

\>A.inv(A)

                1             0 
                0             1 

Poin utama dari bahasa matriks adalah bahwa semua fungsi dan operator bekerja elemen demi elemen.

\>A.A

                7            10 
               15            22 

\>A^2 //perpangkatan elemen2 A

                1             4 
                9            16 

\>A.A.A

               37            54 
               81           118 

\>power(A,3) //perpangkatan matriks

               37            54 
               81           118 

\>A/A //pembagian elemen-elemen matriks yang seletak

                1             1 
                1             1 

\>A/b //pembagian elemen2 A oleh elemen2 b kolom demi kolom (karena b vektor kolom)

         0.333333      0.666667 
             0.75             1 

\>A\\b // hasilkali invers A dan b, A^(-1)b 

               -2 
              2.5 

\>inv(A).b

               -2 
              2.5 

\>A\\A   //A^(-1)A

                1             0 
                0             1 

\>inv(A).A

                1             0 
                0             1 

\>A\*A //perkalin elemen-elemen matriks seletak

                1             4 
                9            16 

Ini bukan hasil kali matriks, tetapi perkalian elemen demi elemen. Hal yang sama berlaku untuk vektor.

\>b^2 // perpangkatan elemen-elemen matriks/vektor

                9 
               16 

Jika salah satu operan adalah vektor atau skalar, maka operan tersebut akan diperluas dengan cara alami.

\>2\*A

                2             4 
                6             8 

Misalnya, jika operan adalah vektor kolom, elemen-elemennya diterapkan ke semua baris A.

\>[1,2]\*A

                1             4 
                3             8 

Jika operan adalah vektor baris, elemen-elemennya diterapkan ke semua kolom A.

\>A\*[2,3]

                2             6 
                6            12 

Kita dapat membayangkan perkalian ini seolah-olah vektor baris v telah diduplikasi untuk membentuk matriks dengan ukuran yang sama dengan A.

\>dup([1,2],2) // dup: menduplikasi/menggandakan vektor [1,2] sebanyak 2 kali (baris)

                1             2 
                1             2 

\>A\*dup([1,2],2) 

                1             4 
                3             8 

Hal ini juga berlaku untuk dua vektor di mana satu vektor adalah vektor baris dan yang lainnya adalah vektor kolom. Kami menghitung i*j untuk i, j dari 1 sampai 5. Caranya adalah dengan mengalikan 1:5 dengan transposenya. Bahasa matriks Euler secara otomatis menghasilkan sebuah tabel nilai.

\>(1:5)\*(1:5)' // hasilkali elemen-elemen vektor baris dan vektor kolom

                1             2             3             4             5 
                2             4             6             8            10 
                3             6             9            12            15 
                4             8            12            16            20 
                5            10            15            20            25 

Sekali lagi, ingatlah bahwa ini bukan produk matriks!

\>(1:5).(1:5)' // hasilkali vektor baris dan vektor kolom

    55

\>sum((1:5)\*(1:5)) // sama hasilnya

    55

Bahkan operator seperti &lt; atau == bekerja dengan cara yang sama.

\>(1:10)<6 // menguji elemen-elemen yang kurang dari 6

    [1,  1,  1,  1,  1,  0,  0,  0,  0,  0]

Sebagai contoh, kita dapat menghitung jumlah elemen yang memenuhi kondisi tertentu dengan fungsi sum().

\>sum((1:10)<6) // banyak elemen yang kurang dari 6

    5

Euler memiliki operator perbandingan, seperti “==”, yang memeriksa kesetaraan.
Kita mendapatkan vektor 0 dan 1, di mana 1 berarti benar.

\>t=(1:10)^2; t==25 //menguji elemen2 t yang sama dengan 25 (hanya ada 1)

    [0,  0,  0,  0,  1,  0,  0,  0,  0,  0]

Dari vektor seperti itu, “nonzeros” memilih elemen bukan nol.
Dalam hal ini, kita mendapatkan indeks semua elemen yang lebih besar dari 50.

\>nonzeros(t\>50) //indeks elemen2 t yang lebih besar daripada 50

    [8,  9,  10]

Tentu saja, kita dapat menggunakan vektor indeks ini untuk mendapatkan nilai yang sesuai dalam t.

\>t[nonzeros(t\>50)] //elemen2 t yang lebih besar daripada 50

    [64,  81,  100]

Sebagai contoh, mari kita cari semua kuadrat dari angka 1 sampai 1000, yaitu 5 modulo 11 dan 3 modulo 13.

\>t=1:1000; nonzeros(mod(t^2,11)==5 && mod(t^2,13)==3)

    [4,  48,  95,  139,  147,  191,  238,  282,  290,  334,  381,  425,
    433,  477,  524,  568,  576,  620,  667,  711,  719,  763,  810,  854,
    862,  906,  953,  997]

EMT tidak sepenuhnya efektif untuk komputasi bilangan bulat. EMT menggunakan floating point presisi ganda secara internal. Akan tetapi, hal ini sering kali sangat berguna.

Kita dapat memeriksa bilangan prima. Mari kita cari tahu, berapa banyak kuadrat ditambah 1 yang merupakan bilangan prima.

\>t=1:1000; length(nonzeros(isprime(t^2+1)))

    112

Fungsi nonzeros() hanya bekerja untuk vektor. Untuk matriks, ada mnonzeros().

\>seed(2); A=random(3,4)

         0.765761      0.401188      0.406347      0.267829 
          0.13673      0.390567      0.495975      0.952814 
         0.548138      0.006085      0.444255      0.539246 

Ini mengembalikan indeks elemen, yang bukan nol.

\>k=mnonzeros(A<0.4) //indeks elemen2 A yang kurang dari 0,4

                1             4 
                2             1 
                2             2 
                3             2 

Indeks ini dapat digunakan untuk menetapkan elemen ke suatu nilai.

\>mset(A,k,0) //mengganti elemen2 suatu matriks pada indeks tertentu

         0.765761      0.401188      0.406347             0 
                0             0      0.495975      0.952814 
         0.548138             0      0.444255      0.539246 

Fungsi mset() juga dapat mengatur elemen-elemen pada indeks ke entri-entri matriks lain.

\>mset(A,k,-random(size(A)))

         0.765761      0.401188      0.406347     -0.126917 
        -0.122404     -0.691673      0.495975      0.952814 
         0.548138     -0.483902      0.444255      0.539246 

Dan dimungkinkan untuk mendapatkan elemen-elemen dalam vektor.

\>mget(A,k)

    [0.267829,  0.13673,  0.390567,  0.006085]

Fungsi lain yang berguna adalah extrema, yang mengembalikan nilai minimal dan maksimal di setiap baris matriks dan posisinya.

\>ex=extrema(A)

         0.267829             4      0.765761             1 
          0.13673             1      0.952814             4 
         0.006085             2      0.548138             1 

Kita bisa menggunakan ini untuk mengekstrak nilai maksimal dalam setiap baris.

\>ex[,3]'

    [0.765761,  0.952814,  0.548138]

Ini, tentu saja, sama dengan fungsi max().

\>max(A)'

    [0.765761,  0.952814,  0.548138]

Tetapi dengan mget(), kita dapat mengekstrak indeks dan menggunakan informasi ini untuk mengekstrak elemen-elemen pada posisi yang sama dari matriks yang lain.

\>j=(1:rows(A))'|ex[,4], mget(-A,j)

                1             1 
                2             4 
                3             1 
    [-0.765761,  -0.952814,  -0.548138]

# Fungsi Matriks Lainnya

Untuk membangun matriks, kita dapat menumpuk satu matriks di atas yang lain. Jika keduanya tidak memiliki jumlah kolom yang sama, kolom yang lebih pendek akan diisi dengan 0.

\>v=1:3; v\_v

                1             2             3 
                1             2             3 

Demikian juga, kita dapat melampirkan matriks ke matriks lain secara berdampingan, jika keduanya memiliki jumlah baris yang sama.

\>A=random(3,4); A|v'

         0.032444     0.0534171      0.595713      0.564454             1 
          0.83916      0.175552      0.396988       0.83514             2 
        0.0257573      0.658585      0.629832      0.770895             3 

Jika keduanya tidak memiliki jumlah baris yang sama, matriks yang lebih pendek diisi dengan 0.
Ada pengecualian untuk aturan ini. Bilangan real yang dilampirkan pada sebuah matriks akan digunakan sebagai kolom yang diisi dengan bilangan real tersebut.

\>A|1

         0.032444     0.0534171      0.595713      0.564454             1 
          0.83916      0.175552      0.396988       0.83514             1 
        0.0257573      0.658585      0.629832      0.770895             1 

Dimungkinkan untuk membuat matriks vektor baris dan kolom.

\>[v;v]

                1             2             3 
                1             2             3 

\>[v',v']

                1             1 
                2             2 
                3             3 

Tujuan utama dari hal ini adalah untuk menginterpretasikan vektor ekspresi untuk vektor kolom.

\>"[x,x^2]"(v')

                1             1 
                2             4 
                3             9 

Untuk mendapatkan ukuran A, kita dapat menggunakan fungsi berikut ini.

\>C=zeros(2,4); rows(C), cols(C), size(C), length(C)

    2
    4
    [2,  4]
    4

yaitu menggunakan perintah length().

\>length(2:10)

    9

Ada banyak fungsi lain yang menghasilkan matriks.

\>ones(2,2)

                1             1 
                1             1 

Ini juga dapat digunakan dengan satu parameter. Untuk mendapatkan vektor dengan angka selain 1, gunakan yang berikut ini.

\>ones(5)\*6

    [6,  6,  6,  6,  6]

Matriks angka acak juga dapat dibuat dengan acak (distribusi seragam) atau normal (Gauß distribution).

\>random(2,2)

          0.66566      0.831835 
            0.977      0.544258 

Berikut ini adalah fungsi lain yang berguna, yang merestrukturisasi elemen-elemen matriks menjadi matriks lain.

\>redim(1:9,3,3) // menyusun elemen2 1, 2, 3, ..., 9 ke bentuk matriks 3x3

                1             2             3 
                4             5             6 
                7             8             9 

Dengan fungsi berikut, kita dapat menggunakan fungsi ini dan fungsi dup untuk menulis fungsi rep(), yang mengulang sebuah vektor sebanyak n kali.

\>function rep(v,n) := redim(dup(v,n),1,n\*cols(v))

Mari kita coba

\>rep(1:3,5)

    [1,  2,  3,  1,  2,  3,  1,  2,  3,  1,  2,  3,  1,  2,  3]

Fungsi multdup() menduplikasi elemen-elemen sebuah vektor.

\>multdup(1:3,5), multdup(1:3,[2,3,2])

    [1,  1,  1,  1,  1,  2,  2,  2,  2,  2,  3,  3,  3,  3,  3]
    [1,  1,  2,  2,  2,  3,  3]

Fungsi flipx() dan flipy() membalik urutan baris atau kolom dari sebuah matriks. Misalnya, fungsi flipx() membalik secara horizontal.

\>flipx(1:5) //membalik elemen2 vektor baris

    [5,  4,  3,  2,  1]

Untuk rotasi, Euler memiliki rotleft() dan rotright().

\>rotleft(1:5) // memutar elemen2 vektor baris

    [2,  3,  4,  5,  1]

Fungsi khusus adalah drop(v,i), yang menghapus elemen dengan indeks di i dari vektor v.

\>drop(10:20,3)

    [10,  11,  13,  14,  15,  16,  17,  18,  19,  20]

Perhatikan bahwa vektor i dalam drop(v,i) merujuk pada indeks elemen dalam v, bukan nilai elemen. Jika Anda ingin menghapus elemen, Anda harus menemukan elemen-elemen tersebut terlebih dahulu. Fungsi indexof(v,x) dapat digunakan untuk menemukan elemen x dalam vektor terurut v.

\>v=primes(50), i=indexof(v,10:20), drop(v,i)

    [2,  3,  5,  7,  11,  13,  17,  19,  23,  29,  31,  37,  41,  43,  47]
    [0,  5,  0,  6,  0,  0,  0,  7,  0,  8,  0]
    [2,  3,  5,  7,  23,  29,  31,  37,  41,  43,  47]

Seperti yang Anda lihat, tidak ada salahnya menyertakan indeks di luar jangkauan (seperti 0), indeks ganda, atau indeks yang tidak diurutkan.

\>drop(1:10,shuffle([0,0,5,5,7,12,12]))

    [1,  2,  3,  4,  6,  8,  9,  10]

Ada beberapa fungsi khusus untuk mengatur diagonal atau menghasilkan matriks diagonal.
Kita mulai dengan matriks identitas.

\>A=id(5) // matriks identitas 5x5

                1             0             0             0             0 
                0             1             0             0             0 
                0             0             1             0             0 
                0             0             0             1             0 
                0             0             0             0             1 

Kemudian, kami menetapkan diagonal bawah (-1) ke 1:4.

\>setdiag(A,-1,1:4) //mengganti diagonal di bawah diagonal utama

                1             0             0             0             0 
                1             1             0             0             0 
                0             2             1             0             0 
                0             0             3             1             0 
                0             0             0             4             1 

Perhatikan bahwa kita tidak mengubah matriks A. Kita mendapatkan sebuah matriks baru sebagai hasil dari setdiag().

Berikut adalah sebuah fungsi yang mengembalikan sebuah matriks tri-diagonal.

\>function tridiag (n,a,b,c) := setdiag(setdiag(b\*id(n),1,c),-1,a); ...  
\>   tridiag(5,1,2,3)

                2             3             0             0             0 
                1             2             3             0             0 
                0             1             2             3             0 
                0             0             1             2             3 
                0             0             0             1             2 

Diagonal sebuah matriks juga dapat diekstrak dari matriks. Untuk mendemonstrasikan hal ini, kami merestrukturisasi vektor 1:9 menjadi matriks 3x3.

\>A=redim(1:9,3,3)

                1             2             3 
                4             5             6 
                7             8             9 

Sekarang kita bisa mengekstrak diagonal.

\>d=getdiag(A,0)

    [1,  5,  9]

Contoh: Kita dapat membagi matriks dengan diagonalnya. Bahasa matriks memperhatikan bahwa vektor kolom d diterapkan ke matriks baris demi baris.

\>fraction A/d'

            1         2         3 
          4/5         1       6/5 
          7/9       8/9         1 

# Vectorization

Hampir semua fungsi di Euler juga berfungsi untuk input matriks dan vektor, kapan pun ini masuk akal.
Misalnya, fungsi sqrt() menghitung akar kuadrat dari semua elemen vektor atau matriks. 

\>sqrt(1:3)

    [1,  1.41421,  1.73205]

Jadi, kamu dapat dengan mudah membuat tabel nilai. Ini adalah salah satu cara untuk memplot suatu fungsi(alternatifnya menggunakan ekspresi).

\>x=1:0.01:5; y=log(x)/x^2; // terlalu panjang untuk ditampikan

Dengan ini dan operator titik dua a:delta:b, vektor nilai fungsi dapat dihasilkan dengan mudah.
Pada contoh berikut, kita menghasilkan vektor nilai t[i] dengan jarak 0,1 dari -1 hingga 1. Kemudian kita menghasilkan vektor nilai dari fungsi.
$$s = t^3-t$$\>t=-1:0.1:1; s=t^3-t

    [0,  0.171,  0.288,  0.357,  0.384,  0.375,  0.336,  0.273,  0.192,
    0.099,  0,  -0.099,  -0.192,  -0.273,  -0.336,  -0.375,  -0.384,
    -0.357,  -0.288,  -0.171,  0]

EMT memperluas operator untuk skalar, vektor, dan matriks dengan cara yang jelas.

Misalnya, vektor kolom dikalikan vektor baris diperluas menjadi matriks, jika operator diterapkan. Berikut ini, v' adalah vektor yang ditransposisikan (vektor kolom).

\>shortest (1:5)\*(1:5)'

         1      2      3      4      5 
         2      4      6      8     10 
         3      6      9     12     15 
         4      8     12     16     20 
         5     10     15     20     25 

Perhatikan, bahwa ini sangat berbeda dari produk matriks. Produk matriks dilambangkan dengan titik "." di EMT.

\>(1:5).(1:5)'
 
    55

Secara default, vektor baris dicetak dalam format yang ringkas.

\>[1,2,3,4]

    [1,  2,  3,  4]

Untuk matriks operator khusus . menunjukkan perkalian matriks, dan A' menunjukkan transpos. Matriks 1x1 dapat digunakan seperti bilangan real.

\>v:=[1,2]; v.v', %^2

    5
    25

Untuk mentranspos matriks kita menggunakan apostrof,

\>v=1:4; v'

                1 
                2 
                3 
                4 

Jadi kita dapat menghitung matriks A dikali vektor b.

\>A=[1,2,3,4;5,6,7,8]; A.v'

               30 
               70 

Perhatikan bahwa v masih merupakan vektor baris, Jadi v'.v berbeda dengan v.v'.

\>v'.v

                1             2             3             4 
                2             4             6             8 
                3             6             9            12 
                4             8            12            16 

v.v' menghitung norma v kuadrat untuk vektor baris v. Hasilnya adalah vektor 1x1, yang bekerja seperti bilangan real.

\>v.v'

    30

Ada juga fungsi norma (bersama dengan banyak fungsi lain dari Aljabar Linier).

\>norm(v)^2

    30

Operator dan fungsi mematuhi bahasa matriks Euler. Berikut ringkasan aturannya.

1. Fungsi yang diterapkan ke vektor atau matriks diterapkan ke setiap elemen.
2. Operator yang beroperasi pada dua matriks dengan ukuran yang sama diterapkan berpasangan ke elemen matriks.
3. jika kedua matriks memiliki dimensi yang berbeda, keduanya diperluas dengan cara yang masuk akal, sehingga memiliki ukuran yang sama. Misalnya, nilai skalar kali vektor mengalikan nilai dengan setiap elemen vektor. Atau matriks kali vektor (dengan *, bukan.) memperluas vektor ke ukuran matriks dengan menduplikasikan.
   
Berikut ini adalah kasus sederhana dengan operator^.

\>[1,2,3]^2

    [1,  4,  9]

Berikut adalah kasus yang lebih rumit. Vektor baris dikalikan dengan vektor kolom mengembang keduanya dengan menduplikasi.

\>v:=[1,2,3]; v\*v'

                1             2             3 
                2             4             6 
                3             6             9 

Perhatikan bahwa produk skalar menggunakan produk matriks, bukan *!

\>v.v'

    14

Ada banyak fungsi matriks. Kami memberikan daftar singkat. Anda harus berkonsultasi dengan dokumentasi untuk informasi lebih lanjut tentang perintah ini.

  sum,prod menghitung jumlah dan produk dari baris  
  cumsum,cumprod melakukan hal yang sama secara kumulatif menghitung nilai ekstrem dari setiap baris  
  extrema mengembalikan vektor dengan informasi ekstrim  
  diag(A,i) mengembalikan diagonal ke-i  
  setdiag(A,i,v) mengatur diagonal  ke-i  
  id(n) matriks identitas  
  det(A) penentu  
  charpoly(A) polinomial  karakteristik  
  nilai eigen(A) nilai eigen.  

\>v\*v, sum(v\*v), cumsum(v\*v)

    [1,  4,  9]
    14
    [1,  5,  14]

Operator : menghasilkan vektor baris spasi yang sama, opsional dengan ukuran langkah.

\>1:4, 1:2:10

    [1,  2,  3,  4]
    [1,  3,  5,  7,  9]

Untuk menggabungkan matriks dan vektor, terdapat operator “|” dan “_”.

\>[1,2,3]|[4,5], [1,2,3]\_1

    [1,  2,  3,  4,  5]
                1             2             3 
                1             1             1 

Elemen-elemen dari sebuah matriks disebut dengan “A[i,j]”.

\>A:=[1,2,3;4,5,6;7,8,9]; A[2,3]

    6

Untuk vektor baris atau kolom, v[i] adalah elemen ke-i dari vektor. Untuk matriks, ini mengembalikan baris ke-i lengkap dari matriks.

\>v:=[2,4,6,8]; v[3], A[3]

    6
    [7,  8,  9]

Indeks juga bisa menjadi vektor baris dari indeks. : menunjukkan semua indeks.

\>v[1:2], A[:,2]

    [2,  4]
                2 
                5 
                8 

Bentuk singkat untuk : adalah menghilangkan indeks sepenuhnya.

\>A[,2:3]

                2             3 
                5             6 
                8             9 

Untuk tujuan vektorisasi, elemen matriks dapat diakses seolah-olah mereka adalah vektor.

\>A{4}

    4

Matriks juga dapat diratakan, menggunakan fungsi redim(). Ini diimplementasikan dalam fungsi flatten().

\>redim(A,1,prod(size(A))), flatten(A)
 
    [1,  2,  3,  4,  5,  6,  7,  8,  9]
    [1,  2,  3,  4,  5,  6,  7,  8,  9]

Untuk menggunakan matriks untuk tabel, mari kita reset ke format default, dan menghitung tabel nilai sinus dan kosinus. Perhatikan bahwa sudut dalam radian secara default.

\>defformat; w=0°:45°:360°; w=w'; deg(w)

                0 
               45 
               90 
              135 
              180 
              225 
              270 
              315 
              360 

Sekarang kita menambahkan kolom ke matriks.

\>M = deg(w)|w|cos(w)|sin(w)

                0             0             1             0 
               45      0.785398      0.707107      0.707107 
               90        1.5708             0             1 
              135       2.35619     -0.707107      0.707107 
              180       3.14159            -1             0 
              225       3.92699     -0.707107     -0.707107 
              270       4.71239             0            -1 
              315       5.49779      0.707107     -0.707107 
              360       6.28319             1             0 

Dengan menggunakan bahasa matriks, kita dapat menghasilkan beberapa tabel dari beberapa fungsi sekaligus.
Dalam contoh berikut, kita menghitung t[j]^i untuk i dari 1 hingga n. Kami mendapatkan matriks, di mana setiap baris adalah tabel t^i untuk satu i. Yaitu, matriks memiliki elemen
$$a_{i,j} = t_j^i, \quad 1 \le j \le 101, \quad 1 \le i \le n$$Fungsi yang tidak berfungsi untuk input vektor harus "vectorized". Ini dapat dicapai dengan kata kunci "map" dalam definisi fungsi.Kemudian fungsi tersebut akan dievaluasi untuk setiap elemen dari parameter vektor.
Integrasi numerik terintegrasi() hanya berfungsi untuk batas interval skalar. Jadi kita perlu membuat vektor.

\>function map f(x) := integrate("x^x",1,x)

Kata kunci "map" membuat vektor fungsi. Fungsinya sekarang akan bekerja untuk vektor bilangan.

\>f([1:5])

    [0,  2.05045,  13.7251,  113.336,  1241.03]

# Sub-Matrices dan Matrix-Elements

Untuk mengakses elemen matriks, gunakan notasi braket.

\>A=[1,2,3;4,5,6;7,8,9], A[2,2]

                1             2             3 
                4             5             6 
                7             8             9 
    5

Kita dapat mengakses satu baris matriks yang lengkap.

\>A[2]

    [4,  5,  6]

Dalam kasus vektor baris atau kolom, ini mengembalikan elemen vektor.

\>v=1:3; v[2]

    2

Untuk memastikan, Anda mendapatkan baris pertama untuk matriks 1xn dan mxn, tentukan semua kolom menggunakan indeks kedua kosong.

\>A[2,]

    [4,  5,  6]

Jika indeks adalah vektor indeks, Euler akan mengembalikan baris matriks yang sesuai.
Di sini kita ingin baris pertama dan kedua dari A.

\>A[[1,2]]

                1             2             3 
                4             5             6 

Kita bahkan dapat menyusun ulang A menggunakan vektor indeks. Tepatnya, kami tidak mengubah A disini, tetapi menghitung versi A yang disusun ulang.

\>A[[3,2,1]]

                7             8             9 
                4             5             6 
                1             2             3 

Trik indeks bekerja dengan kolom juga.
Contoh ini memilih semua baris A dan kolom kedua dan ketiga.

\>A[1:3,2:3]

                2             3 
                5             6 
                8             9 

Untuk singkatan ":" menunjukkan semua indeks baris atau kolom.

\>A[:,3]

                3 
                6 
                9 

Atau, biarkan indeks pertama kosong.

\>A[,2:3]

                2             3 
                5             6 
                8             9 

Kita juga bisa mendapatkan baris terakhir dari A.

\>A[-1]

    [7,  8,  9]

Sekarang mari kita ubah elemen A dengan menetapkan submatriks A ke beberapa nilai. Ini sebenarnya mengubah matriks A yang disimpan.

\>A[1,1]=4

                4             2             3 
                4             5             6 
                7             8             9 

Kita juga dapat menetapkan nilai pada deretan A.

\>A[1]=[-1,-1,-1]

               -1            -1            -1 
                4             5             6 
                7             8             9 

Kami bahkan dapat menetapkan sub-matriks jika memiliki ukuran yang tepat.

\>A[1:2,1:2]=[5,6;7,8]

                5             6            -1 
                7             8             6 
                7             8             9 

Selain itu, beberapa jalan pintas diperbolehkan.

\>A[1:2,1:2]=0

                0             0            -1 
                0             0             6 
                7             8             9 

Peringatan: Indeks di luar batas mengembalikan matriks kosong, atau pesan kesalahan, tergantung pada pengaturan sistem. Standarnya adalah pesan kesalahan. Ingat, bagaimanapun, bahwa indeks negatif dapat digunakan untuk mengakses elemen matriks yang dihitung dari akhir.

\>A[4]

    Row index 4 out of bounds!
    Error in:
    A[4] ...
        ^

# Menyortir dan mengacak

Fungsi sort() mengurutkan vektor baris

\>sort([5,6,4,8,1,9])

    [1,  4,  5,  6,  8,  9]

Seringkali perlu untuk mengetahui indeks dari vektor yang diurutkan dalam vektor aslinya. Ini dapat digunakan untuk menyusun ulang vektor lain dengan cara yang sama.
Mari kita mengacak vektor.

\>v=shuffle(1:10)

    [4,  5,  10,  6,  8,  9,  1,  7,  2,  3]

Indeks berisi urutan yang tepat dari v.

\>{vs,ind}=sort(v); v[ind]

    [1,  2,  3,  4,  5,  6,  7,  8,  9,  10]

Hal ini juga berlaku untuk vektor string.

\>s=["a","d","e","a","aa","e"]

    a
    d
    e
    a
    aa
    e

\>{ss,ind}=sort(s); ss

    a
    a
    aa
    d
    e
    e

Seperti yang Anda lihat, posisi entri ganda agak acak.

\>ind

    [4,  1,  5,  2,  6,  3]

Fungsi unique mengembalikan daftar terurut dari elemen unik sebuah vektor.

\>intrandom(1,10,10), unique(%)

    [4,  4,  9,  2,  6,  5,  10,  6,  5,  1]
    [1,  2,  4,  5,  6,  9,  10]

Hal ini juga berlaku untuk vektor string.

\>unique(s)

    a
    aa
    d
    e

# Aljabar Linier

EMT memiliki banyak fungsi untuk menyelesaikan sistem linier, sistem sparse, atau masalah regresi.

Untuk sistem linier Ax=b,dengan A adalah matriks koefisien, x adalah vektor solusi yang ingin kita cari dan b adalah vektor hasil yang diberikan.Anda dapat menggunakan algoritma Gauss, matriks invers atau kecocokan linier. 

Operator A\b menggunakan versi algoritma Gauss.

Operator backslash \ digunakan untuk menyelesaikan sistem persamaan linier ini. Ketika menulis A\b, perangkat lunak akan menghitung solusi yang memenuhi persamaan Ax=b. Operator ini secara otomatis menggunakan algoritma eliminasi Gauss atau metode numerik serupa untuk menemukan solusi.

\>A=[1,2;3,4]; b=[5;6]; A\\b

               -4 
              4.5 

Untuk contoh lain, kami membuat matriks 200x200 dan jumlah barisnya. Kemudian kita selesaikan Ax=b menggunakan matriks invers. Kami mengukur kesalahan sebagai deviasi maksimal semua elemen dari 1,yang tentu saja merupakan solusi yang benar.

\>A=normal(200,200); b=sum(A); longest totalmax(abs(inv(A).b-1))

      8.790745908981989e-13 

Jika sistem tidak memiliki solusi, kecocokan linier meminimalkan norma kesalahan Ax-b.

\>A=[1,2,3;4,5,6;7,8,9]

                1             2             3 
                4             5             6 
                7             8             9 

Determinan matriks ini adalah 0.

\>det(A)

    0

# Matriks Simbolik

Maxima memiliki matriks simbolis. Tentu saja, Maxima dapat digunakan untuk masalah aljabar linier sederhana seperti itu. Kita dapat mendefinisikan matriks untuk Euler dan Maxima dengan &amp;:=, dan kemudian menggunakannya dalam ekspresi simbolis. Bentuk [...] biasa untuk mendefinisikan matriks dapat digunakan di Euler untuk mendefinisikan matriks simbolik.

\>A &= [a,1,1;1,a,1;1,1,a]; $A
$$\begin{pmatrix}a & 1 & 1 \\ 1 & a & 1 \\ 1 & 1 & a \\ \end{pmatrix}$$\>$&det(A), $&factor(%)
$$\left(a-1\right)^2\,\left(a+2\right)$$![s/EMT%20untuk%20Perhitungan%20Aljabar_Isni%20Azizah%20Utami_23030630016-089.png](s/EMT%20untuk%20Perhitungan%20Aljabar_Isni%20Azizah%20Utami_23030630016-089.png)

\>$&invert(A) with a=0
$$\begin{pmatrix}-\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\ \frac{1  }{2} & -\frac{1}{2} & \frac{1}{2} \\ \frac{1}{2} & \frac{1}{2} & -  \frac{1}{2} \\ \end{pmatrix}$$\>A &= [1,a;b,2]; $A
$$\begin{pmatrix}1 & a \\ b & 2 \\ \end{pmatrix}$$dengan

1. `det(A)` menghitung determinan matriks A.
2. `factor(% )` memberikan faktor-faktor dari determinan.
3. `invert(A)` memberikan invers dari matriks A.

Seperti semua variabel simbolik, matriks ini dapat digunakan dalam ekspresi simbolik lainnya.

\>$&det(A-x\*ident(2)), $&solve(%,x)

$\left[ x=\frac{3-\sqrt{4\,a\,b+1}}{2} , x=\frac{\sqrt{4\,a\,b+1}+3  }{2} \right] $$

Nilai eigen juga dapat dihitung secara otomatis. Hasilnya adalah vektor dengan dua vektor nilai eigen dan multiplisitas.

\>$&eigenvalues([a,1;1,a])

$\left[ \left[ a-1 , a+1 \right]  , \left[ 1 , 1 \right]  \right] $$

Untuk mengekstrak vektor eigen tertentu perlu pengindeksan yang cermat.

\>$&eigenvectors([a,1;1,a]), &%[2][1][1]

$\left[ \left[ \left[ a-1 , a+1 \right]  , \left[ 1 , 1 \right]    \right]  , \left[ \left[ \left[ 1 , -1 \right]  \right]  , \left[   \left[ 1 , 1 \right]  \right]  \right]  \right] $$
                                   [1, - 1]
    
Matriks simbolik dapat dievaluasi dalam Euler secara numerik sepert ekspresi simbolik lainnya.

\>A(a=4,b=5)

                1             4 
                5             2 

Dalam ekspresi simbolik, gunakan "with".

\>$&A with [a=4,b=5]
$$\begin{pmatrix}1 & 4 \\ 5 & 2 \\ \end{pmatrix}$$Akses ke baris matriks simbolik bekerja seperti halnya dengan matriks numerik.

\>$&A[1]

$\left[ 1 , a \right] $$

Ekspresi simbolis dapat berisi tugas. Dan itu mengubah matriks A.

\>&A[1,1]:=t+1; $&A
$$\begin{pmatrix}t+1 & a \\ b & 2 \\ \end{pmatrix}$$Terdapat fungsi-fungsi simbolik dalam Maxima untuk membuat vektor dan matriks. Untuk hal ini, lihat dokumentasi Maxima atau tutorial tentang Maxima di EMT.

\>v &= makelist(1/(i+j),i,1,3); $v

$\left[ \frac{1}{j+1} , \frac{1}{j+2} , \frac{1}{j+3} \right] $$

\>B &:= [1,2;3,4]; $B, $&invert(B)
$$\begin{pmatrix}-2 & 1 \\ \frac{3}{2} & -\frac{1}{2} \\   \end{pmatrix}$$

Hasilnya dapat dievaluasi secara numerik dalam Euler. Untuk informasi lebih lanjut tentang Maxima, lihat pengantar Maxima.

\>$&invert(B)()

               -2             1 
              1.5          -0.5 

Euler juga memiliki fungsi xinv() yang kuat, yang membuat upaya lebih besar dan mendapatkan hasil yang lebih tepat. Perhatikan, bahwa dengan &amp;:= matriks B telah didefinisikan sebagai simbolik dalam ekspresi simbolik dan sebagai numerik dalam ekspresi numerik. Jadi kita bisa menggunakannya di sini.

\>longest B.xinv(B)

                          1                       0 
                          0                       1 

Misalnya. nilai eigen dari A dapat dihitung secara numerik.

\>A=[1,2,3;4,5,6;7,8,9]; real(eigenvalues(A))

    [16.1168,  -1.11684,  0]

Atau secara simbolis. Lihat tutorial tentang Maxima untuk detailnya.

\>$&eigenvalues(@A)

$\left[ \left[ \frac{15-3\,\sqrt{33}}{2} , \frac{3\,\sqrt{33}+15}{2}   , 0 \right]  , \left[ 1 , 1 , 1 \right]  \right] $$

# Nilai Numerik dalam Ekspresi simbolis 

Ekspresi simbolis hanyalah string yang berisi ekspresi. Jika kita ingin mendefinisikan nilai baik untuk ekspresi simbolik maupun ekspresi numerik, kita harus menggunakan "&amp;:=".

\>A &:= [1,pi;4,5]

                1       3.14159 
                4             5 

Masih ada perbedaan antara bentuk numerik dan simbolik. Saat mentransfer matriks ke bentuk simbolis, pendekatan fraksional untuk real akan digunakan.

\>$&A
$$\begin{pmatrix}1 & \frac{1146408}{364913} \\ 4 & 5 \\ \end{pmatrix}$$Untuk menghindarinya, ada fungsi "mxmset(variable)".

\>mxmset(A); $&A

$$\begin{pmatrix}1 & 3.141592653589793 \\ 4 & 5 \\ \end{pmatrix}$$Maxima juga dapat menghitung dengan angka floating point, dan bahkan dengan angka floating besar dengan 32 digit. Namun, evaluasinya jauh lebih lambat.

\>$&bfloat(sqrt(2)), $&float(sqrt(2))

$$1.414213562373095$$

Ketepatan angka floating point besar dapat diubah.

\>&fpprec:=100; &bfloat(pi)

            3.14159265358979323846264338327950288419716939937510582097494\
    4592307816406286208998628034825342117068b0
    

Variabel numerik dapat digunakan dalam ekspresi simbolis apa pun menggunakan "@var". Perhatikan bahwa ini hanya diperlukan, jika variabel telah didefinisikan dengan ":=" atau "=" sebagai variabel numerik.

\>B:=[1,pi;3,4]; $&det(@B)

$$-5.424777960769379$$

# Demo - Suku Bunga

Di bawah ini, kami menggunakan Euler Math Toolbox (EMT) untuk perhitungan suku bunga. Kami melakukannya secara numerik dan simbolis untuk menunjukkan kepada Anda bagaimana Euler dapat digunakan untuk memecahkan masalah kehidupan nyata.

Asumsikan Anda memiliki modal awal 5000 (katakanlah dalam dolar).

\>K=5000

    5000

Sekarang kita asumsikan tingkat bunga 3% per tahun. Mari kita tambahkan satu tarif sederhana dan hitung hasilnya.

\>K\*1.03

    5150

Euler akan memahami sintaks berikut juga.

\>K+K\*3%

    5150

Tetapi lebih mudah menggunakan faktornya.

\>q=1+3%, K\*q

    1.03
    5150

Selama 10 tahun, kita cukup mengalikan faktornya dan mendapatkan nilai akhir dengan suku bunga majemuk.

\>K\*q^10

    6719.58189672

Untuk tujuan kita, kita dapat mengatur format menjadi 2 digit setelah titik desimal.

\>format(12,2); K\*q^10

        6719.58 

Mari kita cetak yang dibulatkan menjadi 2 digit dalam kalimat lengkap.

\>"Starting from " + K + "$ you get " + round(K\*q^10,2) + "$."

    Starting from 5000$ you get 6719.58$.

Bagaimana jika kita ingin mengetahui hasil antara dari tahun 1 sampai tahun 9? Untuk ini, bahasa matriks Euler sangat membantu. Anda tidak harus menulis loop, tetapi cukup masukkan.

\>K\*q^(0:10)

    Real 1 x 11 matrix
    
        5000.00     5150.00     5304.50     5463.64     ...

Bagaimana keajaiban ini bekerja? Pertama ekspresi 0:10 mengembalikan vektor bilangan bulat.

\>short 0:10

    [0,  1,  2,  3,  4,  5,  6,  7,  8,  9,  10]

Kemudian semua operator dan fungsi dalam Euler dapat diterapkan pada elemen vektor untuk elemen. jadi

\>short q^(0:10)

    [1,  1.03,  1.0609,  1.0927,  1.1255,  1.1593,  1.1941,  1.2299,
    1.2668,  1.3048,  1.3439]

adalah vektor faktor qˆ0 sampai qˆ10. Ini dikalikan dengan K, dan kami mendapatkan vektor nilai.

\>VK=K\*q^(0:10);

Tentu saja, cara realistis untuk menghitung suku bunga ini adalah dengan membulatkan ke sen terdekat setelah setiap tahun. Mari kita tambahkan fungsi untuk ini.

\>function oneyear (K) := round(K\*q,2)

Mari kita bandingkan kedua hasil tersebut, dengan dan tanpa pembulatan.

\>longest oneyear(1234.57), longest 1234.57\*q

                    1271.61 
                  1271.6071 

Sekarang tidak ada rumus sederhana untuk tahun ke-n, dan kita harus mengulang selama bertahun-tahun. Euler memberikan banyak solusi untuk ini.

Cara termudah adalah iterasi fungsi, yang mengulangi fungsi tertentu
beberapa kali.

\>VKr=iterate("oneyear",5000,10)

    Real 1 x 11 matrix
    
        5000.00     5150.00     5304.50     5463.64     ...

Kami dapat mencetaknya dengan cara yang ramah, menggunakan format kami dengan tempat desimal tetap.

\>VKr'

        5000.00 
        5150.00 
        5304.50 
        5463.64 
        5627.55 
        5796.38 
        5970.27 
        6149.38 
        6333.86 
        6523.88 
        6719.60 

Untuk mendapatkan elemen tertentu dari vektor, kami menggunakan indeks dalam tanda kurung siku.

\>VKr[2], VKr[1:3]

        5150.00 
        5000.00     5150.00     5304.50 

Anehnya, kita juga bisa menggunakan vektor indeks. Ingat bahwa 1:3 menghasilkan vektor [1,2,3].

Mari kita bandingkan elemen terakhir dari nilai yang dibulatkan dengan
nilai penuh.

\>VKr[-1], VK[-1]

        6719.60 
        6719.58 

Perbedaannya sangat kecil.

# Memecahkan Persamaan

Sekarang kita mengambil fungsi yang lebih maju, yang menambahkan tingkat uang tertentu setiap tahun.

\>function onepay (K) := K\*q+R

Kita tidak perlu menentukan q atau R untuk definisi fungsi. Hanya jika kita menjalankan perintah, kita harus mendefinisikan nilai-nilai ini. Kami memilih R=200.

\>R=200; iterate("onepay",5000,10)

    Real 1 x 11 matrix
    
        5000.00     5350.00     5710.50     6081.82     ...

Bagaimana jika kita menghapus jumlah yang sama setiap tahun?

\>R=-200; iterate("onepay",5000,10)

    Real 1 x 11 matrix
    
        5000.00     4950.00     4898.50     4845.45     ...

Kami melihat bahwa uang berkurang. Jelas, jika kita hanya mendapatkan 150 bunga di tahun pertama, tetapi menghapus 200, kita kehilangan uang setiap tahun.

Bagaimana kita bisa menentukan berapa tahun uang itu akan bertahan? Kita harus menulis loop untuk ini. Cara termudah adalah dengan iterasi cukup lama.

\>VKR=iterate("onepay",5000,50)

    Real 1 x 51 matrix
    
        5000.00     4950.00     4898.50     4845.45     ...

Dengan menggunakan bahasa matriks, kita dapat menentukan nilai negatif pertama dengan cara berikut.

\>min(nonzeros(VKR<0))

          48.00 

Alasan untuk ini adalah bahwa nonzeros(VKR&lt;0) mengembalikan vektor indeks i, di mana VKR[i]&lt;0,dan min menghitung indeks minimal.

Karena vektor selalu dimulai dengan indeks 1, jawabannya adalah 47 tahun.

Fungsi iterate() memiliki satu trik lagi. Itu bisa mengambil kondisi akhir sebagai argumen. Kemudian akan mengembalikan nilai dan jumlah iterasi.

\>{x,n}=iterate("onepay",5000,till="x<0"); x, n,

         -19.83 
          47.00 

Mari kita coba menjawab pertanyaan yang lebih ambigu. Asumsikan kita tahu bahwa nilainya adalah 0 setelah 50 tahun. Apa yang akan menjadi tingkat bunga?

Ini adalah pertanyaan yang hanya bisa dijawab dengan angka. Di bawah ini, kita akan mendapatkan formula yang diperlukan. Kemudian Anda akan melihat bahwa tidak ada formula yang mudah untuk tingkat bunga.
Tapi untuk saat ini, kami bertujuan untuk solusi numerik.

Langkah pertama adalah mendefinisikan fungsi yang melakukan iterasi sebanyak n kali. Kami menambahkan semua parameter ke fungsi ini.

\>function f(K,R,P,n) := iterate("x\*(1+P/100)+R",K,n;P,R)[-1]

Iterasinya sama seperti di atas.
$$x_{n+1} = x_n \cdot \left(1+ \frac{P}{100}\right) + R$$
Tapi kami tidak lagi menggunakan nilai global R dalam ekspresi kami.

Fungsi seperti iterate() memiliki trik khusus di Euler. Anda dapat meneruskan nilai variabel dalam ekspresi sebagai parameter titik koma. Dalam hal ini P dan R.

Selain itu, kami hanya tertarik pada nilai terakhir. Jadi kita ambil indeks [-1].

Mari kita coba tes.

\>f(5000,-200,3,47)

         -19.83 

Sekarang kita bisa menyelesaikan masalah kita.

\>solve("f(5000,-200,x,50)",3)

           3.15 

Rutin memecahkan memecahkan ekspresi=0 untuk variabel x. Jawabannya adalah 3,15% per tahun. Kami mengambil nilai awal 3% untuk algoritma. Fungsi solve() selalu membutuhkan nilai awal.
Kita dapat menggunakan fungsi yang sama untuk menyelesaikan pertanyaan berikut:

Berapa banyak yang dapat kita keluarkan per tahun sehingga modal awal habis setelah 20 tahun dengan asumsi tingkat bunga 3% per tahun.

\>solve("f(5000,x,3,20)",-200)

        -336.08 

Perhatikan bahwa Anda tidak dapat memecahkan jumlah tahun, karena fungsi kami mengasumsikan n sebagai nilai integer.

# Solusi Simbolik untuk Masalah Suku Bunga

Kita dapat menggunakan bagian simbolik dari Euler untuk mempelajari masalah tersebut. Pertama kita mendefinisikan fungsi onepay() kita secara simbolis.

\>function op(K) &= K\*q+R; $&op(K)
$$R+q\,K$$Kita sekarang dapat mengulangi ini.

\>$&op(op(op(op(K)))), $&expand(%)
$$q^3\,R+q^2\,R+q\,R+R+q^4\,K$$

Kami melihat sebuah pola. Setelah n periode yang kita miliki$$K_n = q^n K + R (1+q+\ldots+q^{n-1}) = q^n K + \frac{q^n-1}{q-1} R$$Rumusnya adalah rumus untuk jumlah geometri, yang diketahui Maxima.

\>&sum(q^k,k,0,n-1); $& % = ev(%,simpsum)
$$\sum_{k=0}^{n-1}{q^{k}}=\frac{q^{n}-1}{q-1}$$Ini agak rumit. Jumlahnya dievaluasi dengan bendera ”simpsum” untuk menguranginya menjadi hasil bagi.
Mari kita membuat fungsi untuk ini.

Rumusnya adalah rumus untuk jumlah geometri, yang diketahui Maxima.

\>function fs(K,R,P,n) &= (1+P/100)^n\*K + ((1+P/100)^n-1)/(P/100)\*R; $&fs(K,R,P,n)
$$\frac{100\,\left(\left(\frac{P}{100}+1\right)^{n}-1\right)\,R}{P}+K  \,\left(\frac{P}{100}+1\right)^{n}$$Fungsi tersebut melakukan hal yang sama seperti fungsi f kita sebelumnya. Tapi itu lebih efektif.

\>longest f(5000,-200,3,47), longest fs(5000,-200,3,47)

         -19.82504734650985 
         -19.82504734652684 

Kita sekarang dapat menggunakannya untuk menanyakan waktu n. Kapan modal kita habis? Dugaan awal kami adalah 30 tahun.

fungsi untuk ini. Rumusnya adalah rumus untuk jumlah geometri, yang diketahui Maxima.

\>solve("fs(5000,-330,3,x)",30)

          20.51 

Jawaban ini mengatakan bahwa itu akan menjadi negatif setelah 21 tahun.

Kita juga dapat menggunakan sisi simbolis Euler untuk menghitung formula pembayaran. Asumsikan kita mendapatkan pinjaman sebesar K, dan membayar n pembayaran sebesar R (dimulai setelah tahun pertama) meninggalkan sisa hutang sebesar Kn (pada saat pembayaran terakhir). Rumus untuk ini jelas.

\>equ &= fs(K,R,P,n)=Kn; $&equ
$$\frac{100\,\left(\left(\frac{P}{100}+1\right)^{n}-1\right)\,R}{P}+K  \,\left(\frac{P}{100}+1\right)^{n}={\it Kn}$$Biasanya rumus ini diberikan dalam bentuk.
$$i = \frac{P}{100}$$\>equ &= (equ with P=100\*i); $&equ
$$\frac{\left(\left(i+1\right)^{n}-1\right)\,R}{i}+\left(i+1\right)^{  n}\,K={\it Kn}$$Kita dapat memecahkan tingkat R secara simbolis.

\>$&solve(equ,R)

$\left[ R=\frac{i\,{\it Kn}-i\,\left(i+1\right)^{n}\,K}{\left(i+1  \right)^{n}-1} \right] $$

Seperti yang Anda lihat dari rumus, fungsi ini mengembalikan kesalahan titik mengambang untuk i=0. Euler tetap merencanakannya. Tentu saja, kami memiliki batas beriku

\>$&limit(R(5000,0,x,10),x,0)
$$\lim_{x\rightarrow 0}{R\left(5000 , 0 , x , 10\right)}$$Jelas, tanpa bunga kita harus membayar kembali 10 tarif 500. Persamaan juga dapat diselesaikan untuk n. Kelihatannya lebih bagus, jika kita menerapkan beberapa penyederhanaan untuk itu.

\>fn &= solve(equ,n) | ratsimp; $&fn

$\left[ n=\frac{\log \left(\frac{R+i\,{\it Kn}}{R+i\,K}\right)}{  \log \left(i+1\right)} \right] $$

# Latihan Soal 

## R.2 Exercise set
Soal No 49
Menyederhanakan:$$\left(\frac{24a^{10}b^{-8}c^7}{12a^6b^{-3}c^5}\right)^{-5}$$\>$& ((24\*a^(10)\*b^(-8)\*c^7)/(12\*a^(6)\*b^(-3)\*c^5))^(-5)
$$\frac{b^{25}}{32\,a^{20}\,c^{10}}$$Soal No 50
Menyederhanakan:
$$\left(\frac{125p^{12}q^{-14}r^{22}}{25p^8q^6r^{-15}}\right)^{-4}$$\>$& ((125\*p^(12)\*q^(-14)\*r^(22))/(25\*p^(8)\*q^(6)\*r^(-15)))^-4
$$\frac{q^{80}}{625\,p^{16}\,r^{148}}$$Soal No 90
calculate$$2^6*2^{-3}/2^{10}/2^{-8}$$\>$&  2^(6)\*2^(-3)/2^10/2^-8

$2$

Soal No 91
Calculate
$$\left(\frac{4(8-6)^2-4\times3+2\times8}{3^1+9^0}\right)$$\>$& (4\*(8-6)^2 - 4\*3 + 2\*8)/(3^1+19^0)
$$5$$Soal No 92
Calculate
$$\left(\frac{[4(8-6)^2+4](3-2*8)}{2^2(2^5+5)}\right)$$\>((4\*(8-6)^2+4)\*3-2\*8)/(3^1+9^0)

    11

## R.3 Exercise Set 

Perform the indicated operations.
no 27
$$(x+3)^2$$\>$& expand((x+3)^2)
$$x^2+6\,x+9$$no 29
$$(y-5)^2$$\>$& expand((y-5)^2)
$$y^2-10\,y+25$$no 33
$$(2x+3y)^2$$\>$& expand((2\*x+3\*y)^2)
$$9\,y^2+12\,x\,y+4\,x^2$$no 39
$$(3y+4)(3y-4)$$\>$& expand ((3\*y+4)\*(3\*y-4))
$$9\,y^2-16$$no 42
$$(3x+5y)(3x-5y)$$\>$& expand ((3\*x+5\*y)\*(3\*x-5\*y))
$$9\,x^2-25\,y^2$$
## R.4 Exercise set

Faktor the trinomial
no 23
$$t^2+8t+15$$\>$& solve (t^2+8\*t+15)

$\left[ t=-3 , t=-5 \right] $$

no 24.
$$y^2+12y+27$$\>$& solve(y^2+12\*y+27)

$\left[ y=-9 , y=-3 \right] $$

Factor the difference of squares
no 47
$$z^2-81$$\>$& solve(z^2-81)

$\left[ z=-9 , z=9 \right] $$

no 48$$m^2-4$$\>$& solve(m^2-4)

$\left[ m=-2 , m=2 \right] $$

no 49$$16x^2-9$$\>$& solve(16\*x^2-9)

$\left[ x=-\frac{3}{4} , x=\frac{3}{4} \right] $$

## R.5 Exercise set

no 31
Tentukan nilai x!$$7(3x+6)=11-(x+2)$$\>$& solve(7\*(3\*x+6)=11-(x+2))

$\left[ x=-\frac{3}{2} \right] $$

no 37
Tentukan nilai x!$$x^2+5x=0$$\>$& solve(x^2+5\*x=0)

$\left[ x=-5 , x=0 \right] $$

no 42
Tentukan nilai y!$$y^2+25=10y$$\>$& solve(y^2+25=10\*y)

$\left[ y=5 \right] $$

no 47
Tentukan nilai z!$$12z^2+z=6$$\>$& solve(12\*z^(2)+z=6)

$\left[ z=-\frac{3}{4} , z=\frac{2}{3} \right] $$

no 60
Tentukan nilai x!$$5x^2-75$$\>$& solve(5\*x^2-75)

$\left[ x=-\sqrt{15} , x=\sqrt{15} \right] $$

## R.6 Exercise set

Sederhanakan!

no 9

\>$& ((x^2-4)/(x^2-4\*x+4)), $&factor(%)
$$\frac{x+2}{x-2}$$
no 10

\>$& ((x^2+2\*x-3)/(x^2-9)), $&factor(%)
$$\frac{x-1}{x-3}$$

no 11

\>$& ((x^3-6\*x^2+9\*x)/(x^3-3\*x^2)), $&factor(%)
$$\frac{x-3}{x}$$

no 12

\>$& ((y^5-5\*y^4+4\*y^3)/(y^3-6\*y^2+8\*y)), $&factor(%)
$$\frac{\left(y-1\right)\,y^2}{y-2}$$

no 13

\>$& ((6\*y^2+12\*y-48)/(3\*y^2-9\*y+6)), $&factor(%)
$$\frac{2\,\left(y+4\right)}{y-1}$$


Nama   : Alya Putri Medilasari

NIM    : 23030630018

Kelas  : Matematika B 2023

# Menggambar Grafik 2D dengan EMT

Notebook ini menjelaskan tentang cara menggambar berbagaikurva dan grafik 2D dengan software EMT. EMT menyediakan fungsi plot2d() untuk menggambar berbagai kurva dan grafik dua dimensi (2D)

## Plot Dasar

Ada fungsi yang sangat mendasar dari plot. Ada koordinat layar, yang selalu berkisar dari 0 hingga 1024 di setiap sumbu, tidak peduli
apakah layarnya persegi atau tidak. Semut ada koordinat plot, yang dapat diatur dengan setplot(). Pemetaan antara koordinat tergantung
pada jendela plot saat ini. Misalnya, shrinkwindow() default menyisakan ruang untuk label sumbu dan judul plot.
 
Dalam contoh, kita hanya menggambar beberapa garis acak dalam berbagai warna. Untuk detail tentang fungsi ini, pelajari fungsi inti EMT.

\>clg; // clear screen 
\>window(0,0,1024,1024); // use all of the window 
\>setplot(0,1,0,1); // set plot coordinates 
\>hold on; // start overwrite mode 
\>n=100; X=random(n,2); Y=random(n,2);  // get random points 
\>colors=rgb(random(n),random(n),random(n)); // get random colors 
\>loop 1 to n; color(colors[#]); plot(X[#],Y[#]); end; // plot 
\>hold off; // end overwrite mode 
\>insimg; // insert to notebook 
\>reset;

Grafik perlu ditahan, karena perintah plot() akan menghapus jendela plot.

Untuk menghapus semua yang kami lakukan, kami menggunakan reset().

Untuk menampilkan gambar hasil plot di layar notebook, perintah plot2d() dapat diakhiri dengan titik dua (:). Cara lain adalah
perintah plot2d() diakhiri dengan titik koma (;), kemudian menggunakan perintah insimg() untuk menampilkan gambar hasil plot.

Untuk contoh lain, kami menggambar plot sebagai sisipan di plot lain. Ini dilakukan dengan mendefinisikan jendela plot yang lebih kecil.
Perhatikan bahwa jendela ini tidak menyediakan ruang untuk label sumbu di luar jendela plot. Kita harus menambahkan beberapa margin untuk ini sesuai kebutuhan. Perhatikan bahwa kami menyimpan dan memulihkan jendela penuh, dan menahan plot saat ini saat kami memplot inset.

\>plot2d("x^3-x");

\>xw=200; yw=100; ww=300; hw=300;

\>ow=window();

\>window(xw,yw,xw+ww,yw+hw);

\>hold on;

\>barclear(xw-50,yw-10,ww+60,ww+60);

\>plot2d("x^4-x",grid=6):

\>hold off;

\>window(ow);

Plot dengan banyak angka dicapai dengan cara yang sama. Ada fungsi figure() utilitas untuk ini.

## Aspek Plot

Plot default menggunakan jendela plot persegi. Anda dapat mengubah ini dengan fungsi aspek(). Jangan lupa untuk mengatur ulang aspek nanti. Anda juga dapat mengubah default ini di menu dengan "Set Aspect" ke
rasio aspek tertentu atau ke ukuran jendela grafis saat ini. 

Tetapi Anda juga dapat mengubahnya untuk satu plot. Untuk ini, ukuran area plot saat ini diubah, dan jendela diatur sehingga label memiliki cukup ruang. 

\>aspect(2); // rasio panjang dan lebar 2:1

\>plot2d(["sin(x)","cos(x)"],0,2pi):

\>aspect();

\>reset;

Fungsi reset() mengembalikan default plot termasuk rasio aspek.

# Plot 2D di Euler

EMT Math Toolbox memiliki plot dalam 2D, baik untuk data maupun
fungsi. EMT menggunakan fungsi plot2d. Fungsi ini dapat memplot fungsi
dan data.

Dimungkinkan untuk membuat plot di Maxima menggunakan Gnuplot atau dengan Python menggunakan Math Plot Lib.

Euler dapat memplot plot 2D dari
- ekspresi
- fungsi, variabel, atau kurva parameter,
- vektor nilai x-y,
- awan titik di pesawat,
- kurva implisit dengan level atau wilayah level.
- Fungsi kompleks

Gaya plot mencakup berbagai gaya untuk garis dan titik, plot batangdan plot berbayang.

# Plot Ekspresi atau Variabel

Ekspresi tunggal dalam "x" (mis. "4*x^2") atau nama fungsi (mis. "f") menghasilkan grafik fungsi.

Berikut adalah contoh paling dasar, yang menggunakan rentang default dan menetapkan rentang y yang tepat agar sesuai dengan plot fungsi. 

Catatan: Jika Anda mengakhiri baris perintah dengan titik dua ":", plot akan dimasukkan ke dalam jendela teks. Jika tidak, tekan TAB untuk melihat plot jika jendela plot tertutup.

\>plot2d("x^2"):

\>aspect(1.5); plot2d("x^3-x"):

\>a:=5.6; plot2d("exp(-a\*x^2)/a"); insimg(30); // menampilkan gambar hasil plot setinggi 25 baris

Dari beberapa contoh sebelumnya Anda dapat melihat bahwa aslinya gambar plot menggunakan sumbu X dengan rentang nilai dari -2 sampai dengan 2. Untuk mengubah rentang nilai X dan Y, Anda dapat menambahkan nilai-nilai batas X (dan Y) di belakang ekspresi yang digambar.

Rentang plot diatur dengan parameter yang ditetapkan sebagai berikut
* a,b: rentang x (default -2,2)
* c,d: rentang y (default: skala dengan nilai)
* r: alternatifnya radius di sekitar pusat plot
* cx,cy: koordinat pusat plot (default 0,0)

\>plot2d("x^3-x",-1,2):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-001.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-001.png)
\>plot2d("sin(x)",-2\*pi,2\*pi): // plot sin(x) pada interval [-2pi, 2pi]

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-002.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-002.png)
\>plot2d("cos(x)","sin(3\*x)",xmin=0,xmax=2pi):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-003.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-003.png)

Alternatif untuk titik dua adalah perintah insimg(baris), yang menyisipkan plot yang menempati sejumlah baris teks tertentu.

Dalam opsi, plot dapat diatur untuk muncul
* di jendela terpisah yang dapat diubah ukurannya,
* di jendela buku catatan.

Lebih banyak gaya dapat dicapai dengan perintah plot tertentu. Bagaimanapun, tekan tombol tabulator untuk melihat plot, jika disembunyikan.

Untuk membagi jendela menjadi beberapa plot, gunakan perintah figure(). Dalam contoh, kami memplot x^1 hingga x^4 menjadi 4 bagian jendela. figure(0) mengatur ulang jendela default.

\>reset;
\>figure(2,2); ...  
\>   for n=1 to 4; figure(n); plot2d("x^"+n); end; ...  
\>   figure(0):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-004.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-004.png)

Di plot2d(), ada gaya alternatif yang tersedia dengan grid=x. Untuk gambaran umum, kami menunjukkan berbagai gaya kisi dalam satu gambar (lihat di bawah untuk perintah figure()). Gaya kisi=0 tidak
disertakan. Ini menunjukkan tidak ada grid dan tidak ada bingkai.

\>figure(3,3); ...  
\>   for k=1:9; figure(k); plot2d("x^3-x",-2,1,grid=k); end; ...  
\>   figure(0):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-005.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-005.png)
Jika argumen ke plot2d() adalah ekspresi yang diikuti oleh empat angka, angka-angka ini adalah rentang x dan y untuk plot.

Atau, a, b, c, d dapat ditentukan sebagai parameter yang ditetapkan sebagai a=... dll.

Dalam contoh berikut, kita mengubah gaya kisi, menambahkan label, dan menggunakan label vertikal untuk sumbu y.

\>aspect(1.5); plot2d("sin(x)",0,2pi,-1.2,1.2,grid=3,xl="x",yl="sin(x)"):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-006.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-006.png)

\>plot2d("sin(x)+cos(2\*x)",0,4pi):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-007.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-007.png)

Gambar yang dihasilkan dengan memasukkan plot ke dalam jendela teks disimpan di direktori yang sama dengan buku catatan, secara default di subdirektori bernama "gambar". Mereka juga digunakan oleh ekspor HTML.

Anda cukup menandai gambar apa saja dan menyalinnya ke clipboard dengan Ctrl-C. Tentu saja, Anda juga dapat mengekspor grafik saat ini dengan fungsi di menu File.

Fungsi atau ekspresi dalam plot2d dievaluasi secara adaptif. Untuk kecepatan lebih, matikan plot adaptif dengan &lt;adaptive dan tentukan jumlah subinterval dengan n=... Ini hanya diperlukan dalam kasus yang
jarang terjadi.

\>plot2d("sign(x)\*exp(-x^2)",-1,1,<adaptive,n=10000):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-008.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-008.png)
\>plot2d("x^x",r=1.2,cx=1,cy=1):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-009.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-009.png)
Perhatikan bahwa x^x tidak didefinisikan untuk x&lt;=0. Fungsi plot2d menangkap kesalahan ini, dan mulai merencanakan segera setelah fungsi didefinisikan. Ini berfungsi untuk semua fungsi yang mengembalikan NAN keluar dari jangkauan definisinya.

\>plot2d("log(x)",-0.1,2):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-010.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-010.png)
Parameter square=true (atau &gt;square) memilih y-range secara otomatis sehingga hasilnya adalah jendela plot persegi. Perhatikan bahwa secara default, Euler menggunakan ruang persegi di dalam jendela plot.

\>plot2d("x^3-x",\>square):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-011.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-011.png)

\>plot2d(''integrate("sin(x)\*exp(-x^2)",0,x)'',0,2): // plot integral

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-012.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-012.png)
Jika Anda membutuhkan lebih banyak ruang untuk label-y, panggil shrinkwindow() dengan parameter yang lebih kecil, atau tetapkan nilai positif untuk "lebih kecil" di plot2d().

\>plot2d("gamma(x)",1,10,yl="y-values",smaller=6,<vertical):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-013.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-013.png)

Ekspresi simbolik juga dapat digunakan, karena disimpan sebagai ekspresi string sederhana.

\>x=linspace(0,2pi,1000); plot2d(sin(5x),cos(7x)):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-014.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-014.png)
\>a:=5.6; expr &= exp(-a\*x^2)/a; // define expression
\>plot2d(expr,-2,2): // plot from -2 to 2

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-015.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-015.png)
\>plot2d(expr,r=1,thickness=2): // plot in a square around (0,0)

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-016.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-016.png)
\>plot2d(&diff(expr,x),\>add,style="--",color=red): // add another plot

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-017.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-017.png)
\>plot2d(&diff(expr,x,2),a=-2,b=2,c=-2,d=1): // plot in rectangle

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-018.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-018.png)
\>plot2d(&diff(expr,x),a=-2,b=2,\>square): // keep plot square
![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-019.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-019.png)
\>plot2d("x^2",0,1,steps=1,color=red,n=10):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-020.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-020.png)
\>plot2d("x^2",\>add,steps=2,color=blue,n=10):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-021.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-021.png)
# Fungsi dalam satu Parameter

Fungsi plot yang paling penting untuk plot planar adalah plot2d().
Fungsi ini diimplementasikan dalam bahasa Euler dalam file "plot.e", yang dimuat di awal program.

Berikut adalah beberapa contoh menggunakan fungsi. Seperti biasa di EMT, fungsi yang berfungsi untuk fungsi atau ekspresi lain, Anda dapat meneruskan parameter tambahan (selain x) yang bukan variabel global ke fungsi dengan parameter titik koma atau dengan koleksi panggilan.

\>function f(x,a) := x^2/a+a\*x^2-x; // define a function

\>a=0.3; plot2d("f",0,1;a): // plot with a=0.3

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-022.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-022.png)

\>plot2d("f",0,1;0.4): // plot with a=0.4

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-023.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-023.png)
\>plot2d({{"f",0.2}},0,1): // plot with a=0.2

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-024.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-024.png)
\>plot2d({{"f(x,b)",b=0.1}},0,1): // plot with 0.1

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-025.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-025.png)
\>function f(x) := x^3-x; ...  
\>   plot2d("f",r=1):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-026.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-026.png)
Berikut adalah ringkasan dari fungsi yang diterima
* ekspresi atau ekspresi simbolik dalam x
* fungsi atau fungsi simbolis dengan nama sebagai "f"
* fungsi simbolis hanya dengan nama 

Fungsi plot2d() juga menerima fungsi simbolis. Untuk fungsi simbolis, nama saja yang berfungsi.

\>function f(x) &= diff(x^x,x)
    
                                x
                               x  (log(x) + 1)
    
\>plot2d(f,0,2):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-027.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-027.png)
Tentu saja, untuk ekspresi atau ekspresi simbolik, nama variabel sudah cukup untuk memplotnya.

\>expr &= sin(x)\*exp(-x)

                                  - x
                                 E    sin(x)
    
\>plot2d(expr,0,3pi):
![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-028.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-028.png)
\>function f(x) &= x^x;

\>plot2d(f,r=1,cx=1,cy=1,color=blue,thickness=2);

\>plot2d(&diff(f(x),x),\>add,color=red,style="-.-"):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-029.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-029.png)
Untuk gaya garis ada berbagai pilihan.
* gaya="...". Pilih dari "-", "--", "-.", ".", ".-.", "-.-".
* warna: Lihat di bawah untuk warna.
* ketebalan: Default adalah 1.
  
Warna dapat dipilih sebagai salah satu warna default, atau sebagai warna RGB.
* 0.15: indeks warna default.
* konstanta warna: putih, hitam, merah, hijau, biru, cyan, zaitun,
* abu-abu muda, abu-abu, abu-abu tua, oranye, hijau muda, pirus, biru
* muda, oranye terang, kuning
* rgb(merah, hijau, biru): parameter adalah real dalam [0,1].

\>plot2d("exp(-x^2)",r=2,color=red,thickness=3,style="--"):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-030.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-030.png)
Berikut adalah tampilan warna EMT yang telah ditentukan sebelumnya.

\>aspect(2); columnsplot(ones(1,16),lab=0:15,grid=0,color=0:15):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-031.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-031.png)
Tapi Anda bisa menggunakan warna apa saja.

\>columnsplot(ones(1,16),grid=0,color=rgb(0,0,linspace(0,1,15))):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-032.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-032.png)
# Menggambar Beberapa Kurva pada bidang koordinat yang sama

Plot lebih dari satu fungsi (multiple function) ke dalam satu jendela dapat dilakukan dengan berbagai cara. Salah satu metode menggunakan &gt;add untuk beberapa panggilan ke plot2d secara keseluruhan, tetapi panggilan pertama. Kami telah menggunakan fitur ini dalam contoh di
atas.

\>aspect(); plot2d("cos(x)",r=2,grid=6); plot2d("x",style=".",\>add):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-033.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-033.png)
\>aspect(1.5); plot2d("sin(x)",0,2pi); plot2d("cos(x)",color=blue,style="--",\>add):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-034.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-034.png)
Salah satu kegunaan &gt;add adalah untuk menambahkan titik pada kurva.

\>plot2d("sin(x)",0,pi); plot2d(2,sin(2),\>points,\>add):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-035.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-035.png)
Kami menambahkan titik persimpangan dengan label (pada posisi "cl" untuk kiri tengah), dan memasukkan hasilnya ke dalam notebook. Kami juga menambahkan judul ke plot.

\>plot2d(["cos(x)","x"],r=1.1,cx=0.5,cy=0.5, ...  
\>     color=[black,blue],style=["-","."], ...  
\>     grid=1);
\>x0=solve("cos(x)-x",1);  ...  
\>     plot2d(x0,x0,\>points,\>add,title="Intersection Demo");  ...  
\>     label("cos(x) = x",x0,x0,pos="cl",offset=20):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-036.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-036.png)

Dalam demo berikut, kami memplot fungsi sinc(x)=sin(x)/x dan ekspansi Taylor ke-8 dan ke-16. Kami menghitung ekspansi ini menggunakan Maxima melalui ekspresi simbolis.

Plot ini dilakukan dalam perintah multi-baris berikut dengan tiga panggilan ke plot2d(). Yang kedua dan yang ketiga memiliki set flag &gt;add, yang membuat plot menggunakan rentang sebelumnya.

Kami menambahkan kotak label yang menjelaskan fungsi.

\>$taylor(sin(x)/x,x,0,4)
$$\frac{x^4}{120}-\frac{x^2}{6}+1$$\>plot2d("sinc(x)",0,4pi,color=green,thickness=2); ...  
\>     plot2d(&taylor(sin(x)/x,x,0,8),\>add,color=blue,style="--"); ...  
\>     plot2d(&taylor(sin(x)/x,x,0,16),\>add,color=red,style="-.-"); ...  
\>     labelbox(["sinc","T8","T16"],styles=["-","--","-.-"], ...  
\>       colors=[black,blue,red]):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-038.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-038.png)

Dalam contoh berikut, kami menghasilkan Bernstein-Polinomial.

\>plot2d("(1-x)^10",0,1); // plot first function

\>for i=1 to 10; plot2d("bin(10,i)\*x^i\*(1-x)^(10-i)",\>add); end;

\>insimg;

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-039.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-039.png)
Metode kedua menggunakan pasangan matriks nilai-x dan matriks nilai-y
yang berukuran sama.

Kami menghasilkan matriks nilai dengan satu Polinomial Bernstein di setiap baris. Untuk ini, kita cukup menggunakan vektor kolom i. Lihat pengantar tentang bahasa matriks untuk mempelajari lebih detail.

\>x=linspace(0,1,500);

\>n=10; k=(0:n)'; // n is row vector, k is column vector

\>y=bin(n,k)\*x^k\*(1-x)^(n-k); // y is a matrix then

\>plot2d(x,y):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-040.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-040.png)
Perhatikan bahwa parameter warna dapat berupa vektor. Kemudian setiap warna digunakan untuk setiap baris matriks.

\>x=linspace(0,1,200); y=x^(1:10)'; plot2d(x,y,color=1:10):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-041.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-041.png)
Metode lain adalah menggunakan vektor ekspresi (string). Anda kemudian dapat menggunakan larik warna, larik gaya, dan larik ketebalan dengan panjang yang sama.

\>plot2d(["sin(x)","cos(x)"],0,2pi,color=4:5): 

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-042.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-042.png)
\>plot2d(["sin(x)","cos(x)"],0,2pi): // plot vector of expressions

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-043.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-043.png)
Kita bisa mendapatkan vektor seperti itu dari Maxima menggunakan makelist() dan mxm2str().

\>v &= makelist(binomial(10,i)\*x^i\*(1-x)^(10-i),i,0,10) // make list

                   10            9              8  2             7  3
           [(1 - x)  , 10 (1 - x)  x, 45 (1 - x)  x , 120 (1 - x)  x , 
               6  4             5  5             4  6             3  7
    210 (1 - x)  x , 252 (1 - x)  x , 210 (1 - x)  x , 120 (1 - x)  x , 
              2  8              9   10
    45 (1 - x)  x , 10 (1 - x) x , x  ]
    

\>mxm2str(v) // get a vector of strings from the symbolic vector

    (1-x)^10
    10*(1-x)^9*x
    45*(1-x)^8*x^2
    120*(1-x)^7*x^3
    210*(1-x)^6*x^4
    252*(1-x)^5*x^5
    210*(1-x)^4*x^6
    120*(1-x)^3*x^7
    45*(1-x)^2*x^8
    10*(1-x)*x^9
    x^10

\>plot2d(mxm2str(v),0,1): // plot functions

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-044.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-044.png)

Alternatif lain adalah dengan menggunakan bahasa matriks Euler.

Jika ekspresi menghasilkan matriks fungsi, dengan satu fungsi di setiap baris, semua fungsi ini akan diplot ke dalam satu plot.

Untuk ini, gunakan vektor parameter dalam bentuk vektor kolom. Jika array warna ditambahkan, itu akan digunakan untuk setiap baris plot.

\>n=(1:10)'; plot2d("x^n",0,1,color=1:10):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-045.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-045.png)

Ekspresi dan fungsi satu baris dapat melihat variabel global.

Jika Anda tidak dapat menggunakan variabel global, Anda perlu menggunakan fungsi dengan parameter tambahan, dan meneruskan parameter ini sebagai parameter titik koma.

Berhati-hatilah, untuk meletakkan semua parameter yang ditetapkan di akhir perintah plot2d. Dalam contoh kita meneruskan a=5 ke fungsi f, yang kita plot dari -10 hingga 10.

\>function f(x,a) := 1/a\*exp(-x^2/a); ...  
\>   plot2d("f",-10,10;5,thickness=2,title="a=5"):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-046.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-046.png)
Atau, gunakan koleksi dengan nama fungsi dan semua parameter tambahan. Daftar khusus ini disebut koleksi panggilan, dan itu adalah cara yang lebih disukai untuk meneruskan argumen ke fungsi yang dengan sendirinya diteruskan sebagai argumen ke fungsi lain.

Dalam contoh berikut, kami menggunakan loop untuk memplot beberapa fungsi (lihat tutorial tentang pemrograman untuk loop).

\>plot2d({{"f",1}},-10,10); ...  
\>   for a=2:10; plot2d({{"f",a}},\>add); end:

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-047.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-047.png)
Kami dapat mencapai hasil yang sama dengan cara berikut menggunakan bahasa matriks EMT. Setiap baris matriks f(x,a) adalah satu fungsi. Selain itu, kita dapat mengatur warna untuk setiap baris matriks. Klik dua kali pada fungsi getspectral() untuk penjelasannya.

\>x=-10:0.01:10; a=(1:10)'; plot2d(x,f(x,a),color=getspectral(a/10)):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-048.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-048.png)
## Label Teks

Dekorasi sederhana bisa
* judul dengan judul="..."
* x- dan y-label dengan xl="...", yl="..."
* label teks lain dengan label("...",x,y)

Perintah label akan memplot ke dalam plot saat ini pada koordinat plot(x,y). Itu bisa mengambil argumen posisi.

\>plot2d("x^3-x",-1,2,title="y=x^3-x",yl="y",xl="x"):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-049.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-049.png)
\>expr := "log(x)/x"; ...  
\>     plot2d(expr,0.5,5,title="y="+expr,xl="x",yl="y"); ...  
\>     label("(1,0)",1,0); label("Max",E,expr(E),pos="lc"):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-050.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-050.png)
Ada juga fungsi labelbox(), yang dapat menampilkan fungsi dan teks. Dibutuhkan vektor string dan warna, satu item untuk setiap fungsi.

\>function f(x) &= x^2\*exp(-x^2);  ...  
\>   plot2d(&f(x),a=-3,b=3,c=-1,d=1);  ...  
\>   plot2d(&diff(f(x),x),\>add,color=blue,style="--"); ...  
\>   labelbox(["function","derivative"],styles=["-","--"], ...  
\>      colors=[black,blue],w=0.4):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-051.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-051.png)

Kotak ditambatkan di kanan atas secara default, tetapi &gt; kiri menambatkannya di kiri atas. Anda dapat memindahkannya ke tempat yang Anda suka. Posisi jangkar adalah sudut kanan atas kotak, dan angkanya adalah pecahan dari ukuran jendela grafik. Lebarnya otomatis.

Untuk plot titik, kotak label juga berfungsi. Tambahkan parameter &gt;points, atau vektor flag, satu untuk setiap label.

Dalam contoh berikut, hanya ada satu fungsi. Jadi kita bisa menggunakan string sebagai pengganti vektor string. Kami mengatur warna teks menjadi hitam untuk contoh ini.

\>n=10; plot2d(0:n,bin(n,0:n),\>addpoints); ...  
\>   labelbox("Binomials",styles="[]",\>points,x=0.1,y=0.1, ...  
\>   tcolor=black,\>left):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-052.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-052.png)

Gaya plot ini juga tersedia di statplot(). Seperti di plot2d() warna dapat diatur untuk setiap baris plot. Ada lebih banyak plot khusus untuk keperluan statistik (lihat tutorial tentang statistik).

\>statplot(1:10,random(2,10),color=[red,blue]):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-053.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-053.png)
Fitur serupa adalah fungsi textbox().

Lebar secara default adalah lebar maksimal dari baris teks. Tapi itu bisa diatur oleh pengguna juga.

\>function f(x) &= exp(-x)\*sin(2\*pi\*x); ...  
\>   plot2d("f(x)",0,2pi); ...  
\>   textbox(latex("\\text{Example of a damped oscillation}\\ f(x)=e^{-x}sin(2\\pi x)"),w=0.85):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-054.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-054.png)
Label teks, judul, kotak label, dan teks lainnya dapat berisi string Unicode (lihat sintaks EMT untuk mengetahui lebih lanjut tentang string Unicode).

\>plot2d("x^3-x",title=u"x &rarr; x&sup3; - x"):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-055.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-055.png)

Label pada sumbu x dan y bisa vertikal, begitu juga sumbunya.
\>plot2d("sinc(x)",0,2pi,xl="x",yl=u"x &rarr; sinc(x)",\>vertical):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-056.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-056.png)

## LaTeX

Anda juga dapat memplot rumus LaTeX jika Anda telah menginstal sistem
LaTeX. Saya merekomendasikan MiKTeX. Jalur ke biner "lateks" dan "dvipng" harus berada di jalur sistem, atau Anda harus mengatur LaTeX di menu opsi.

Perhatikan, bahwa penguraian LaTeX lambat. Jika Anda ingin menggunakan LaTeX dalam plot animasi, Anda harus memanggil latex() sebelum loop sekali dan menggunakan hasilnya (gambar dalam matriks RGB).

Dalam plot berikut, kami menggunakan LaTeX untuk label x dan y, label,
kotak label, dan judul plot.

\>plot2d("exp(-x)\*sin(x)/x",a=0,b=2pi,c=0,d=1,grid=6,color=blue, ...  
\>     title=latex("\\text{Function $\\Phi$}"), ...  
\>     xl=latex("\\phi"),yl=latex("\\Phi(\\phi)")); ...  
\>   textbox( ...  
\>     latex("\\Phi(\\phi) = e^{-\\phi} \\frac{\\sin(\\phi)}{\\phi}"),x=0.8,y=0.5); ...  
\>   label(latex("\\Phi",color=blue),1,0.4):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-057.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-057.png)

Seringkali, kami menginginkan spasi dan label teks non-konformal pada sumbu x. Kita dapat menggunakan xaxis() dan yaxis() seperti yang akan kita tunjukkan nanti.

Cara termudah adalah dengan membuat plot kosong dengan bingkai menggunakan grid=4, lalu menambahkan grid dengan ygrid() dan xgrid(). Dalam contoh berikut, kami menggunakan tiga string LaTeX untuk label pada sumbu x dengan xtick().

\>plot2d("sinc(x)",0,2pi,grid=4,<ticks); ...  
\>   ygrid(-2:0.5:2,grid=6); ...  
\>   xgrid([0:2]\*pi,<ticks,grid=6);  ...  
\>   xtick([0,pi,2pi],["0","\\pi","2\\pi"],\>latex):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-058.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-058.png)
Tentu saja, fungsi juga dapat digunakan.
\>function map f(x) ...

    if x>0 then return x^4
    else return x^2
    endif
    endfunction
</pre>
Parameter "peta" membantu menggunakan fungsi untuk vektor. Untuk plot, itu tidak perlu. Tetapi untuk mendemonstrasikan vektorisasi itu berguna, kami menambahkan beberapa poin kunci ke plot di x=-1, x=0 dan x=1.

Pada plot berikut, kami juga memasukkan beberapa kode LaTeX. Kami menggunakannya untuk dua label dan kotak teks. Tentu saja, Anda hanya akan dapat menggunakan LaTeX jika Anda telah menginstal LaTeX dengan benar.

\>plot2d("f",-1,1,xl="x",yl="f(x)",grid=6);  ...  
\>   plot2d([-1,0,1],f([-1,0,1]),\>points,\>add); ...  
\>   label(latex("x^3"),0.72,f(0.72)); ...  
\>   label(latex("x^2"),-0.52,f(-0.52),pos="ll"); ...  
\>   textbox( ...  
\>     latex("f(x)=\\begin{cases} x^3 & x\>0 \\\\ x^2 & x \\le 0\\end{cases}"), ...  
\>     x=0.7,y=0.2):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-059.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-059.png)
## Interaksi pengguna

Saat memplot fungsi atau ekspresi, parameter &gt;user memungkinkan pengguna untuk memperbesar dan menggeser plot dengan tombol kursor atau mouse. Pengguna dapat
* perbesar dengan + atau -
* pindahkan plot dengan tombol kursor
* pilih jendela plot dengan mouse
* atur ulang tampilan dengan spasi
* keluar dengan kembali

Tombol spasi akan mengatur ulang plot ke jendela plot asli.
Saat memplot data, flag &gt;user hanya akan menunggu penekanan tombol.

\>plot2d({{"x^3-a\*x",a=1}},\>user,title="Press any key!"):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-060.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-060.png)

\>plot2d("exp(x)\*sin(x)",user=true, ...  
\>     title="+/- or cursor keys (return to exit)"):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-061.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-061.png)

Berikut ini menunjukkan cara interaksi pengguna tingkat lanjut (lihat tutorial tentang pemrograman untuk detailnya)

Fungsi bawaan mousedrag() menunggu event mouse atau keyboard. Ini melaporkan mouse ke bawah, mouse dipindahkan atau mouse ke atas, dan penekanan tombol. Fungsi dragpoints() memanfaatkan ini, dan memungkinkan pengguna menyeret titik mana pun dalam plot.

Kita membutuhkan fungsi plot terlebih dahulu. Sebagai contoh, kita interpolasi dalam 5 titik dengan polinomial. Fungsi harus diplot ke area plot tetap.

\>function plotf(xp,yp,select) ...

      d=interp(xp,yp);
      plot2d("interpval(xp,d,x)";d,xp,r=2);
      plot2d(xp,yp,>points,>add);
      if select>0 then
        plot2d(xp[select],yp[select],color=red,>points,>add);
      endif;
      title("Drag one point, or press space or return!");
    endfunction
</pre>
Perhatikan parameter titik koma di plot2d (d dan xp), yang diteruskan ke evaluasi fungsi interp(). Tanpa ini, kita harus menulis fungsi plotinterp() terlebih dahulu, mengakses nilai secara global. 
Sekarang kita menghasilkan beberapa nilai acak, dan membiarkan pengguna menyeret poin.

\>t=-1:0.5:1; dragpoints("plotf",t,random(size(t))-0.5):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-062.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-062.png)
Ada juga fungsi, yang memplot fungsi lain tergantung pada vektor parameter, dan memungkinkan pengguna menyesuaikan parameter ini.

Pertama kita membutuhkan fungsi plot.

\>function plotf([a,b]) := plot2d("exp(a\*x)\*cos(2pi\*b\*x)",0,2pi;a,b);

Kemudian kita membutuhkan nama untuk parameter, nilai awal dan matriks rentang nx2, opsional baris judul.

Ada slider interaktif, yang dapat mengatur nilai oleh pengguna. Fungsi dragvalues() menyediakan ini.

\>dragvalues("plotf",["a","b"],[-1,2],[[-2,2];[1,10]], ...  
\>     heading="Drag these values:",hcolor=black):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-063.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-063.png)

Dimungkinkan untuk membatasi nilai yang diseret ke bilangan bulat. Sebagai contoh, kita menulis fungsi plot, yang memplot polinomial Taylor derajat n ke fungsi kosinus.

\>function plotf(n) ...

    plot2d("cos(x)",0,2pi,>square,grid=6);
    plot2d(&"taylor(cos(x),x,0,@n)",color=blue,>add);
    textbox("Taylor polynomial of degree "+n,0.1,0.02,style="t",>left);
    endfunction
</pre>
Sekarang kami mengizinkan derajat n bervariasi dari 0 hingga 20 dalam 20 pemberhentian. Hasil dragvalues() digunakan untuk memplot sketsa dengan n ini, dan untuk memasukkan plot ke dalam buku catatan.

\>nd=dragvalues("plotf","degree",2,[0,20],20,y=0.8, ...  
\>      heading="Drag the value:"); ...  
\>   plotf(nd):


![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-064.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-064.png)
Berikut ini adalah demonstrasi sederhana dari fungsi tersebut.
Pengguna dapat menggambar di atas jendela plot, meninggalkan jejak
poin.

\>function dragtest ...

      plot2d(none,r=1,title="Drag with the mouse, or press any key!");
      start=0;
      repeat
        {flag,m,time}=mousedrag();
        if flag==0 then return; endif;
        if flag==2 then
          hold on; mark(m[1],m[2]); hold off;
        endif;
      end
    endfunction
</pre>
\>dragtest // lihat hasilnya dan cobalah lakukan!

## Gaya Plot 2D

Secara default, EMT menghitung tick sumbu otomatis dan menambahkan label ke setiap tick. Ini dapat diubah dengan parameter grid. Gaya default sumbu dan label dapat dimodifikasi. Selain itu, label dan
judul dapat ditambahkan secara manual. Untuk mengatur ulang ke gaya default, gunakan reset().

\>aspect();

\>figure(3,4); ...  
\>    figure(1); plot2d("x^3-x",grid=0); ... // no grid, frame or axis

\> figure(2); plot2d("x^3-x",grid=1); ... // x-y-axis

\> figure(3); plot2d("x^3-x",grid=2); ... // default ticks

\> figure(4); plot2d("x^3-x",grid=3); ... // x-y- axis with labels inside

\> figure(5); plot2d("x^3-x",grid=4); ... // no ticks, only labels

\> figure(6); plot2d("x^3-x",grid=5); ... // default, but no margin

\> figure(7); plot2d("x^3-x",grid=6); ... // axes only

\> figure(8); plot2d("x^3-x",grid=7); ... // axes only, ticks at axis

\> figure(9); plot2d("x^3-x",grid=8); ... // axes only, finer ticks at axis

\> figure(10); plot2d("x^3-x",grid=9); ... // default, small ticks inside

\> figure(11); plot2d("x^3-x",grid=10); ...// no ticks, axes only

\> figure(0):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-065.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-065.png)

Parameter &lt;frame mematikan frame, dan framecolor=blue mengatur frame ke warna biru.

Jika Anda ingin centang sendiri, Anda dapat menggunakan style=0, dan menambahkan semuanya nanti.

\>aspect(1.5); 

\>plot2d("x^3-x",grid=0); // plot

\>frame; xgrid([-1,0,1]); ygrid(0): // add frame and grid

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-066.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-066.png)
Untuk judul plot dan label sumbu, lihat contoh berikut.

\>plot2d("exp(x)",-1,1);

\>textcolor(black); // set the text color to black

\>title(latex("y=e^x")); // title above the plot

\>xlabel(latex("x")); // "x" for x-axis

\>ylabel(latex("y"),\>vertical); // vertical "y" for y-axis

\>label(latex("(0,1)"),0,1,color=blue): // label a point

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-067.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-067.png)
Sumbu dapat digambar secara terpisah dengan xaxis() dan yaxis().

\>plot2d("x^3-x",<grid,<frame);

\>xaxis(0,xx=-2:1,style="-\>"); yaxis(0,yy=-5:5,style="-\>"):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-068.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-068.png)

Teks pada plot dapat diatur dengan label(). Dalam contoh berikut, "lc" berarti tengah bawah. Ini mengatur posisi label relatif terhadap koordinat plot.

\>function f(x) &= x^3-x

                                     3
                                    x  - x
    
\>plot2d(f,-1,1,\>square);

\>x0=fmin(f,0,1); // compute point of minimum

\>label("Rel. Min.",x0,f(x0),pos="lc"): // add a label there


![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-069.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-069.png)
Ada juga kotak teks.

\>plot2d(&f(x),-1,1,-2,2); // function

\>plot2d(&diff(f(x),x),\>add,style="--",color=red); // derivative

\>labelbox(["f","f'"],["-","--"],[black,red]): // label box

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-070.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-070.png)
\>plot2d(["exp(x)","1+x"],color=[black,blue],style=["-","-.-"]):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-071.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-071.png)

\>gridstyle("-\>",color=gray,textcolor=gray,framecolor=gray);  ...  
\>    plot2d("x^3-x",grid=1);   ...  
\>    settitle("y=x^3-x",color=black); ...  
\>    label("x",2,0,pos="bc",color=gray);  ...  
\>    label("y",0,6,pos="cl",color=gray); ...  
\>    reset():


![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-072.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-072.png)

Untuk kontrol lebih, sumbu x dan sumbu y dapat dilakukan secara
manual.

Perintah fullwindow() memperluas jendela plot karena kita tidak lagi membutuhkan tempat untuk label di luar jendela plot. Gunakan shrinkwindow() atau reset() untuk mengatur ulang ke default.

\>fullwindow; ...  
\>    gridstyle(color=darkgray,textcolor=darkgray); ...  
\>    plot2d(["2^x","1","2^(-x)"],a=-2,b=2,c=0,d=4,<grid,color=4:6,<frame); ...  
\>    xaxis(0,-2:1,style="-\>"); xaxis(0,2,"x",<axis); ...  
\>    yaxis(0,4,"y",style="-\>"); ...  
\>    yaxis(-2,1:4,\>left); ...  
\>    yaxis(2,2^(-2:2),style=".",<left); ...  
\>    labelbox(["2^x","1","2^-x"],colors=4:6,x=0.8,y=0.2); ...  
\>    reset:

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-073.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-073.png)

Berikut adalah contoh lain, di mana string Unicode digunakan dan sumbu
di luar area plot.

\>aspect(1.5); 

\>plot2d(["sin(x)","cos(x)"],0,2pi,color=[red,green],<grid,<frame); ...  
\>    xaxis(-1.1,(0:2)\*pi,xt=["0",u"&pi;",u"2&pi;"],style="-",\>ticks,\>zero);  ...  
\>    xgrid((0:0.5:2)\*pi,<ticks); ...  
\>    yaxis(-0.1\*pi,-1:0.2:1,style="-",\>zero,\>grid); ...  
\>    labelbox(["sin","cos"],colors=[red,green],x=0.5,y=0.2,\>left); ...  
\>    xlabel(u"&phi;"); ylabel(u"f(&phi;)"):


![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-074.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-074.png)

# Merencanakan Data 2D

Jika x dan y adalah vektor data, data ini akan digunakan sebagai koordinat x dan y dari suatu kurva. Dalam hal ini, a, b, c, dan d, atau radius r dapat ditentukan, atau jendela plot akan menyesuaikan
secara otomatis dengan data. Atau, &gt;persegi dapat diatur untuk menjaga rasio aspek persegi.

Memplot ekspresi hanyalah singkatan untuk plot data. Untuk plot data, Anda memerlukan satu atau beberapa baris nilai x, dan satu atau beberapa baris nilai y. Dari rentang dan nilai-x, fungsi plot2d akan
menghitung data yang akan diplot, secara default dengan evaluasi fungsi yang adaptif. Untuk plot titik gunakan "&gt;titik", untuk garis campuran dan titik gunakan "&gt;tambahan".

Tapi Anda bisa memasukkan data secara langsung.
* Gunakan vektor baris untuk x dan y untuk satu fungsi.
* Matriks untuk x dan y diplot baris demi baris.
  
Berikut adalah contoh dengan satu baris untuk x dan y.

\>x=-10:0.1:10; y=exp(-x^2)\*x; plot2d(x,y):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-075.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-075.png)
Data juga dapat diplot sebagai titik. Gunakan poin=true untuk ini. Plotnya bekerja seperti poligon, tetapi hanya menggambar sudut-sudutnya.
* style="...": Pilih dari "[]", "&lt;&gt;", "o", ".", "..", "+", "*", "[]#",
* "&lt; &gt;#", "o#", "..#", "#", "|".

Untuk memplot set poin gunakan &gt;points. Jika warna adalah vektor warna, setiap titik mendapat warna yang berbeda. Untuk matriks koordinat dan vektor kolom, warna berlaku untuk baris matriks.

Parameter &gt;addpoints menambahkan titik ke segmen garis untuk plot data.

\>xdata=[1,1.5,2.5,3,4]; ydata=[3,3.1,2.8,2.9,2.7]; // data

\>plot2d(xdata,ydata,a=0.5,b=4.5,c=2.5,d=3.5,style="."); // lines

\>plot2d(xdata,ydata,\>points,\>add,style="o"): // add points


![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-076.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-076.png)

\>p=polyfit(xdata,ydata,1); // get regression line

\>plot2d("polyval(p,x)",\>add,color=red): // add plot of line


![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-077.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-077.png)

# Menggambar Daerah Yang Dibatasi Kurva

Plot data benar-benar poligon. Kita juga dapat memplot kurva atau
kurva terisi.
* terisi=benar mengisi plot.
* style="...": Pilih dari "#", "/", "\", "\/".
* fillcolor: Lihat di atas untuk warna yang tersedia.

Warna isian ditentukan oleh argumen "fillcolor", dan pada &lt;outline opsional mencegah menggambar batas untuk semua gaya kecuali yang default.

\>t=linspace(0,2pi,1000); // parameter for curve

\>x=sin(t)\*exp(t/pi); y=cos(t)\*exp(t/pi); // x(t) and y(t)

\>figure(1,2); aspect(16/9)

\>figure(1); plot2d(x,y,r=10); // plot curve

\>figure(2); plot2d(x,y,r=10,\>filled,style="/",fillcolor=red); // fill curve

\>figure(0):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-078.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-078.png)

Dalam contoh berikut kami memplot elips terisi dan dua segi enam terisi menggunakan kurva tertutup dengan 6 titik dengan gaya isian berbeda.

\>x=linspace(0,2pi,1000); plot2d(sin(x),cos(x)\*0.5,r=1,\>filled,style="/"):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-079.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-079.png)
\>t=linspace(0,2pi,6); ...  
\>   plot2d(cos(t),sin(t),\>filled,style="/",fillcolor=red,r=1.2):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-080.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-080.png)

\>t=linspace(0,2pi,6); plot2d(cos(t),sin(t),\>filled,style="#"):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-081.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-081.png)

Contoh lainnya adalah segi empat, yang kita buat dengan 7 titik pada lingkaran satuan.

\>t=linspace(0,2pi,7);  ...  
\>    plot2d(cos(t),sin(t),r=1,\>filled,style="/",fillcolor=red):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-082.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-082.png)

Berikut ini adalah himpunan nilai maksimal dari empat kondisi linier yang kurang dari atau sama dengan 3. Ini adalah A[k].v&lt;=3 untuk semua baris A. Untuk mendapatkan sudut yang bagus, kita menggunakan n yang relatif besar.

\>A=[2,1;1,2;-1,0;0,-1];

\>function f(x,y) := max([x,y].A');

\>plot2d("f",r=4,level=[0;3],color=green,n=111):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-083.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-083.png)
Poin utama dari bahasa matriks adalah memungkinkan untuk menghasilkan tabel fungsi dengan mudah.

\>t=linspace(0,2pi,1000); x=cos(3\*t); y=sin(4\*t);

Kami sekarang memiliki vektor x dan y nilai. plot2d() dapat memplot nilai-nilai ini sebagai kurva yang menghubungkan titik-titik. Plotnya bisa diisi. Pada kasus ini ini menghasilkan hasil yang bagus karena aturan lilitan, yang digunakan untuk isi.

\>plot2d(x,y,<grid,<frame,\>filled):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-084.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-084.png)

Sebuah vektor interval diplot terhadap nilai x sebagai daerah terisi antara nilai interval bawah dan atas.

Hal ini dapat berguna untuk memplot kesalahan perhitungan. Tapi itu bisa juga digunakan untuk memplot kesalahan statistik.

\>t=0:0.1:1; ...  
\>    plot2d(t,interval(t-random(size(t)),t+random(size(t))),style="|");  ...  
\>    plot2d(t,t,add=true):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-085.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-085.png)

Jika x adalah vektor yang diurutkan, dan y adalah vektor interval, maka plot2d akan memplot rentang interval yang terisi dalam bidang. Gaya isian sama dengan gaya poligon.

\>t=-1:0.01:1; x=~t-0.01,t+0.01~; y=x^3-x;

\>plot2d(t,y):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-086.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-086.png)

Dimungkinkan untuk mengisi wilayah nilai untuk fungsi tertentu. Untuk ini, level harus berupa matriks 2xn. Baris pertama adalah batas bawah dan baris kedua berisi batas atas.

\>expr := "2\*x^2+x\*y+3\*y^4+y"; // define an expression f(x,y)

\>plot2d(expr,level=[0;1],style="-",color=blue): // 0 <= f(x,y) <= 1


![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-087.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-087.png)
Kami juga dapat mengisi rentang nilai seperti

\>plot2d("(x^2+y^2)^2-x^2+y^2",r=1.2,level=[-1;0],style="/"):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-088.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-088.png)

\>plot2d("cos(x)","sin(x)^3",xmin=0,xmax=2pi,\>filled,style="/"):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-089.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-089.png)

# Grafik Fungsi Parametrik

Nilai-x tidak perlu diurutkan. (x,y) hanya menggambarkan kurva. Jika x diurutkan, kurva tersebut merupakan grafik fungsi.

Dalam contoh berikut, kami memplot spiral

Kita perlu menggunakan banyak titik untuk tampilan yang halus atau fungsi adaptif() untuk mengevaluasi ekspresi (lihat fungsi adaptif() untuk lebih jelasnya).

\>t=linspace(0,1,1000); ...  
\>   plot2d(t\*cos(2\*pi\*t),t\*sin(2\*pi\*t),r=1):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-090.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-090.png)

Atau, dimungkinkan untuk menggunakan dua ekspresi untuk kurva. Berikut ini plot kurva yang sama seperti di atas.

\>plot2d("x\*cos(2\*pi\*x)","x\*sin(2\*pi\*x)",xmin=0,xmax=1,r=1):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-091.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-091.png)
\>t=linspace(0,1,1000); r=exp(-t); x=r\*cos(2pi\*t); y=r\*sin(2pi\*t);

\>plot2d(x,y,r=1):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-092.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-092.png)
Dalam contoh berikutnya, kami memplot kurva dengan

\>t=linspace(0,2pi,1000); r=1+sin(3\*t)/2; x=r\*cos(t); y=r\*sin(t); ...  
\>   plot2d(x,y,\>filled,fillcolor=red,style="/",r=1.5):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-093.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-093.png)

# Menggambar Grafik Bilangan Kompleks

Array bilangan kompleks juga dapat diplot. Kemudian titik-titik grid akan terhubung. Jika sejumlah garis kisi ditentukan (atau vektor garis kisi 1x2) dalam argumen cgrid, hanya garis kisi tersebut yang
terlihat.

Matriks bilangan kompleks akan secara otomatis diplot sebagai kisi di bidang kompleks. 
Dalam contoh berikut, kami memplot gambar lingkaran satuan di bawah fungsi eksponensial. Parameter cgrid menyembunyikan beberapa kurva grid.

\>aspect(); r=linspace(0,1,50); a=linspace(0,2pi,80)'; z=r\*exp(I\*a);...  
\>   plot2d(z,a=-1.25,b=1.25,c=-1.25,d=1.25,cgrid=10):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-094.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-094.png)

\>aspect(1.25); r=linspace(0,1,50); a=linspace(0,2pi,200)'; z=r\*exp(I\*a);

\>plot2d(exp(z),cgrid=[40,10]):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-095.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-095.png)

\>r=linspace(0,1,10); a=linspace(0,2pi,40)'; z=r\*exp(I\*a);

\>plot2d(exp(z),\>points,\>add):


![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-096.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-096.png)

Sebuah vektor bilangan kompleks secara otomatis diplot sebagai kurva pada bidang kompleks dengan bagian real dan bagian imajiner.

Dalam contoh, kami memplot lingkaran satuan dengan

\>t=linspace(0,2pi,1000); ...  
\>   plot2d(exp(I\*t)+exp(4\*I\*t),r=2):


![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-097.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-097.png)

# Plot Statistik

Ada banyak fungsi yang dikhususkan pada plot statistik. Salah satu plot yang sering digunakan adalah plot kolom.

Jumlah kumulatif dari nilai terdistribusi 0-1-normal menghasilkan jalan acak.

\>plot2d(cumsum(randnormal(1,1000))):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-098.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-098.png)

Menggunakan dua baris menunjukkan jalan dalam dua dimensi.

\>X=cumsum(randnormal(2,1000)); plot2d(X[1],X[2]):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-099.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-099.png)

\>columnsplot(cumsum(random(10)),style="/",color=blue):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-100.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-100.png)

Itu juga dapat menampilkan string sebagai label.

\>months=["Jan","Feb","Mar","Apr","May","Jun", ...  
\>     "Jul","Aug","Sep","Oct","Nov","Dec"];

\>values=[10,12,12,18,22,28,30,26,22,18,12,8];

\>columnsplot(values,lab=months,color=red,style="-");

\>title("Temperature"):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-101.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-101.png)

\>k=0:10;

\>plot2d(k,bin(10,k),\>bar):


![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-102.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-102.png)
\>plot2d(k,bin(10,k)); plot2d(k,bin(10,k),\>points,\>add):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-103.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-103.png)

\>plot2d(normal(1000),normal(1000),\>points,grid=6,style=".."):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-104.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-104.png)

\>plot2d(normal(1,1000),\>distribution,style="O"):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-105.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-105.png)

\>plot2d("qnormal",0,5;2.5,0.5,\>filled):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-106.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-106.png)

Untuk memplot distribusi statistik eksperimental, Anda dapat
menggunakan distribution=n dengan plot2d.
\>w=randexponential(1,1000); // exponential distribution

\>plot2d(w,\>distribution): // or distribution=n with n intervals

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-107.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-107.png)
Atau Anda dapat menghitung distribusi dari data dan memplot hasilnya dengan &gt;bar di plot3d, atau dengan plot kolom.

\>w=normal(1000); // 0-1-normal distribution

\>{x,y}=histo(w,10,v=[-6,-4,-2,-1,0,1,2,4,6]); // interval bounds v

\>plot2d(x,y,\>bar):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-108.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-108.png)
Fungsi statplot() menyetel gaya dengan string sederhana.

\>statplot(1:10,cumsum(random(10)),"b"):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-109.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-109.png)

\>n=10; i=0:n; ...  
\>   plot2d(i,bin(n,i)/2^n,a=0,b=10,c=0,d=0.3); ...  
\>   plot2d(i,bin(n,i)/2^n,points=true,style="ow",add=true,color=blue):


![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-110.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-110.png)

Selain itu, data dapat diplot sebagai batang. Dalam hal ini, x harus diurutkan dan satu elemen lebih panjang dari y. Bilah akan memanjang dari x[i] ke x[i+1] dengan nilai y[i]. Jika x memiliki ukuran yang
sama dengan y, maka akan diperpanjang satu elemen dengan spasi terakhir.

Gaya isian dapat digunakan seperti di atas.

\>n=10; k=bin(n,0:n); ...  
\>   plot2d(-0.5:n+0.5,k,bar=true,fillcolor=lightgray):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-111.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-111.png)

Data untuk plot batang (bar=1) dan histogram (histogram=1) dapat dinyatakan secara eksplisit dalam xv dan yv, atau dapat dihitung dari distribusi empiris dalam xv dengan &gt;distribusi (atau distribusi=n).
Histogram nilai xv akan dihitung secara otomatis dengan &gt;histogram. Jika &gt;genap ditentukan, nilai xv akan dihitung dalam interval bilangan bulat.

\>plot2d(normal(10000),distribution=50):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-112.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-112.png)

\>k=0:10; m=bin(10,k); x=(0:11)-0.5; plot2d(x,m,\>bar):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-113.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-113.png)

\>columnsplot(m,k):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-114.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-114.png)

\>plot2d(random(600)\*6,histogram=6):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-115.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-115.png)

Untuk distribusi, ada parameter distribusi=n, yang menghitung nilai
secara otomatis dan mencetak distribusi relatif dengan n sub-interval.

\>plot2d(normal(1,1000),distribution=10,style="\\/"):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-116.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-116.png)

Dengan parameter even=true, ini akan menggunakan interval integer.

\>plot2d(intrandom(1,1000,10),distribution=10,even=true):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-117.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-117.png)

Perhatikan bahwa ada banyak plot statistik, yang mungkin berguna. Silahkan lihat tutorial tentang statistik.

\>columnsplot(getmultiplicities(1:6,intrandom(1,6000,6))):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-118.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-118.png)

\>plot2d(normal(1,1000),\>distribution); ...  
\>     plot2d("qnormal(x)",color=red,thickness=2,\>add):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-119.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-119.png)

Ada juga banyak plot khusus untuk statistik. Sebuah boxplot menunjukkan kuartil dari distribusi ini dan banyak dari outlier. Menurut definisi, outlier dalam boxplot adalah data yang melebihi 1,5 kali kisaran 50% tengah plot.

\>M=normal(5,1000); boxplot(quartiles(M)):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-120.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-120.png)

# Fungsi Implisit

Plot implisit menunjukkan garis level yang menyelesaikan f(x,y)=level, di mana "level" dapat berupa nilai tunggal atau vektor nilai. Jika level="auto", akan ada garis level nc, yang akan menyebar antara
fungsi minimum dan maksimum secara merata. Warna yang lebih gelap atau lebih terang dapat ditambahkan dengan &gt;hue untuk menunjukkan nilai fungsi. Untuk fungsi implisit, xv harus berupa fungsi atau ekspresi dari parameter x dan y, atau, sebagai alternatif, xv dapat berupa
matriks nilai.

Euler dapat menandai garis level dari fungsi apapun.

Untuk menggambar himpunan f(x,y)=c untuk satu atau lebih konstanta c, Anda dapat menggunakan plot2d() dengan plot implisitnya di dalam bidang. Parameter untuk c adalah level=c, di mana c dapat berupa vektor garis level. Selain itu, skema warna dapat digambar di latar belakang untuk menunjukkan nilai fungsi untuk setiap titik dalam plot. Parameter "n" menentukan kehalusan plot.

\>aspect(1.5); 

\>plot2d("x^2+y^2-x\*y-x",r=1.5,level=0,contourcolor=red):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-121.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-121.png)

\>expr := "2\*x^2+x\*y+3\*y^4+y"; // define an expression f(x,y)
\>plot2d(expr,level=0): // Solutions of f(x,y)=0

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-122.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-122.png)

\>plot2d(expr,level=0:0.5:20,\>hue,contourcolor=white,n=200): // nice

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-123.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-123.png)

\>plot2d(expr,level=0:0.5:20,\>hue,\>spectral,n=200,grid=4): // nicer

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-124.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-124.png)

Ini berfungsi untuk plot data juga. Tetapi Anda harus menentukan rentangnya untuk label sumbu.

\>x=-2:0.05:1; y=x'; z=expr(x,y);

\>plot2d(z,level=0,a=-1,b=2,c=-2,d=1,\>hue):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-125.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-125.png)

\>plot2d("x^3-y^2",\>contour,\>hue,\>spectral):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-126.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-126.png)

\>plot2d("x^3-y^2",level=0,contourwidth=3,\>add,contourcolor=red):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-127.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-127.png)

\>z=z+normal(size(z))\*0.2;
\>plot2d(z,level=0.5,a=-1,b=2,c=-2,d=1):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-128.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-128.png)

\>plot2d(expr,level=[0:0.2:5;0.05:0.2:5.05],color=lightgray):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-129.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-129.png)

\>plot2d("x^2+y^3+x\*y",level=1,r=4,n=100):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-130.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-130.png)

\>plot2d("x^2+2\*y^2-x\*y",level=0:0.1:10,n=100,contourcolor=white,\>hue):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-131.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-131.png)

Juga dimungkinkan untuk mengisi set dengan rentang tingkat.

Dimungkinkan untuk mengisi wilayah nilai untuk fungsi tertentu. Untuk ini, level harus berupa matriks 2xn. Baris pertama adalah batas bawah dan baris kedua berisi batas atas.

\>plot2d(expr,level=[0;1],style="-",color=blue): // 0 <= f(x,y) <= 1

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-132.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-132.png)

Plot implisit juga dapat menunjukkan rentang level. Kemudian level harus berupa matriks 2xn dari interval level, di mana baris pertama berisi awal dan baris kedua adalah akhir dari setiap interval. Atau,
vektor baris sederhana dapat digunakan untuk level, dan parameter dl memperluas nilai level ke interval.

\>plot2d("x^4+y^4",r=1.5,level=[0;1],color=blue,style="/"):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-133.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-133.png)

\>plot2d("x^2+y^3+x\*y",level=[0,2,4;1,3,5],style="/",r=2,n=100):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-134.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-134.png)

\>plot2d("x^2+y^3+x\*y",level=-10:20,r=2,style="-",dl=0.1,n=100):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-135.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-135.png)

\>plot2d("sin(x)\*cos(y)",r=pi,\>hue,\>levels,n=100):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-136.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-136.png)

Dimungkinkan juga untuk menandai suatu wilayah

Ini dilakukan dengan menambahkan level dengan dua baris.

\>plot2d("(x^2+y^2-1)^3-x^2\*y^3",r=1.3, ...  
\>     style="#",color=red,<outline, ...  
\>     level=[-2;0],n=100):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-137.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-137.png)

Dimungkinkan untuk menentukan level tertentu. Misalnya, kita dapat memplot solusi persamaan seperti

\>plot2d("x^3-x\*y+x^2\*y^2",r=6,level=1,n=100):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-138.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-138.png)

\>function starplot1 (v, style="/", color=green, lab=none) ...

      if !holding() then clg; endif;
      w=window(); window(0,0,1024,1024);
      h=holding(1);
      r=max(abs(v))*1.2;
      setplot(-r,r,-r,r);
      n=cols(v); t=linspace(0,2pi,n);
      v=v|v[1]; c=v*cos(t); s=v*sin(t);
      cl=barcolor(color); st=barstyle(style);
      loop 1 to n
        polygon([0,c[#],c[#+1]],[0,s[#],s[#+1]],1);
        if lab!=none then
          rlab=v[#]+r*0.1;
          {col,row}=toscreen(cos(t[#])*rlab,sin(t[#])*rlab);
          ctext(""+lab[#],col,row-textheight()/2);
        endif;
      end;
      barcolor(cl); barstyle(st);
      holding(h);
      window(w);
    endfunction
</pre>
Tidak ada kotak atau sumbu kutu di sini. Selain itu, kami menggunakan
jendela penuh untuk plot.

Kami memanggil reset sebelum kami menguji plot ini untuk mengembalikan default grafis. Ini tidak perlu, jika Anda yakin plot Anda berhasil.

\>reset; starplot1(normal(1,10)+5,color=red,lab=1:10):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-139.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-139.png)

Terkadang, Anda mungkin ingin merencanakan sesuatu yang tidak dapat dilakukan plot2d, tetapi hampir. 

Dalam fungsi berikut, kami melakukan plot impuls logaritmik. plot2d dapat melakukan plot logaritmik, tetapi tidak untuk batang impuls.

\>function logimpulseplot1 (x,y) ...

      {x0,y0}=makeimpulse(x,log(y)/log(10));
      plot2d(x0,y0,>bar,grid=0);
      h=holding(1);
      frame();
      xgrid(ticks(x));
      p=plot();
      for i=-10 to 10;
        if i<=p[4] and i>=p[3] then
           ygrid(i,yt="10^"+i);
        endif;
      end;
      holding(h);
    endfunction
</pre>
Mari kita uji dengan nilai yang terdistribusi secara eksponensial.

\>aspect(1.5); x=1:10; y=-log(random(size(x)))\*200; ...  
\>   logimpulseplot1(x,y):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-140.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-140.png)

Mari kita menganimasikan kurva 2D menggunakan plot langsung. Perintah plot(x,y) hanya memplot kurva ke jendela plot. setplot(a,b,c,d) mengatur jendela ini.

Fungsi wait(0) memaksa plot untuk muncul di jendela grafik. Jika tidak, menggambar ulang terjadi dalam interval waktu yang jarang. 

\>function animliss (n,m) ...

    t=linspace(0,2pi,500);
    f=0;
    c=framecolor(0);
    l=linewidth(2);
    setplot(-1,1,-1,1);
    repeat
      clg;
      plot(sin(n*t),cos(m*t+f));
      wait(0);
      if testkey() then break; endif;
      f=f+0.02;
    end;
    framecolor(c);
    linewidth(l);
    endfunction
</pre>
Tekan sembarang tombol untuk menghentikan animasi ini.

\>animliss(2,3); // lihat hasilnya, jika sudah puas, tekan ENTER

# Plot Logaritmik

EMT menggunakan parameter "logplot" untuk skala logaritmik.

Plot logaritma dapat diplot baik menggunakan skala logaritma dalam y dengan logplot=1, atau menggunakan skala logaritma dalam x dan y dengan logplot=2, atau dalam x dengan logplot=3.
* logplot=1: y-logaritma
* logplot=2: x-y-logaritma 
* logplot=3: x-logaritma
 
\>plot2d("exp(x^3-x)\*x^2",1,5,logplot=1):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-141.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-141.png)

\>plot2d("exp(x+sin(x))",0,100,logplot=1):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-142.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-142.png)

\>plot2d("exp(x+sin(x))",10,100,logplot=2):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-143.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-143.png)

\>plot2d("gamma(x)",1,10,logplot=1):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-144.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-144.png)

\>plot2d("log(x\*(2+sin(x/100)))",10,1000,logplot=3):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-145.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-145.png)

Ini juga berfungsi dengan plot data.
\>x=10^(1:20); y=x^2-x;
\>plot2d(x,y,logplot=2):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-146.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-146.png)

# Rujukan Lengkap Fungsi plot2d() function plot2d (xv, yv, btest, a,

b, c, d, xmin, xmax, r, n, ..

logplot, kisi, bingkai, warna bingkai, kotak, warna, ketebalan, gaya,
..

otomatis, tambahkan, pengguna, delta, poin, titik tambahan, gaya
titik, bilah, histogram, ..

distribusi, genap, langkah, sendiri, adaptif, rona, level, kontur, ..

nc, terisi, fillcolor, outline, title, xl, yl, maps, contourcolor, ..

contourwidth, ticks, margin, clipping, cx, cy, insimg, spectral, ..

cgrid, vertikal, lebih kecil, dl, niveau, level)

Fungsi plot serbaguna untuk plot di pesawat (plot 2D). Fungsi ini
dapat melakukan plot fungsi satu variabel, plot data, kurva bidang, plot batang,
kisi-kisi bilangan kompleks, dan plot implisit fungsi dua variabel.

Parameter

x,y          : persamaan, fungsi atau vektor data

a,b,c,d      : Area plot (default a=-2,b=2)

r            : jika r diset, maka a=cx-r, b=cx+r, c=cy-r, d=cy+r

               r dapat berupa vektor [rx,ry] atau vektor
[rx1,rx2,ry1,ry2].

xmin,xmax    : rentang parameter untuk kurva

auto         : Menentukan y-range secara otomatis (default)

kuadrat      : jika benar, coba pertahankan rentang x-y persegi

n            : jumlah interval (default adaptif)

kisi         :      0 = tidak ada kisi dan label

                    1 = sumbu saja,
                    2 = grid normal (lihat di bawah untuk jumlah garis grid)
                    3 = sumbu dalam
                    4 = tidak ada kisi-kisi
                    5 = kisi penuh termasuk margin
                    6 = kutu di bingkai
                    7 = sumbu saja
                    8 = sumbu saja, sub-centang

bingkai      : 0 = tanpa bingkai

framecolor   : warna bingkai dan kisi

margin       : angka antara 0 dan 0,4 untuk margin di sekitar plot

warna        : Warna kurva. Jika ini adalah vektor warna,

            itu akan digunakan untuk setiap baris matriks plot. Dalam
kasus plot titik, itu harus berupa vektor kolom. Jika vektor baris atau matriks penuh warna digunakan untuk plot titik, itu akan digunakan untuk setiap titik data.
ketebalan: ketebalan garis untuk kurva

            Nilai ini bisa lebih kecil dari 1 untuk garis yang sangat tipis.

style        : Plot style untuk garis, spidol, dan isian.

            Untuk poin gunakan
            "[]", "&lt;&gt;", ".", "..", "...",

            "*", "+", "|", "-", "o"

            "[]#", "&lt;&gt;#", "o#" (bentuk terisi)

            "[]w", "&lt;&gt;w", "ow" (tidak transparan)

            Untuk penggunaan garis

            "-", "--", "-.", ".", ".-.", "-.-", "-&gt;"

            Untuk poligon terisi atau plot batang gunakan

            "#", "#O", "O", "/", "\", "\/",

            "+", "|", "-", "t"

poin         : plot titik tunggal alih-alih segmen garis

addpoints    : jika benar, plot segmen garis dan titik

add          : menambahkan plot ke plot yang ada

pengguna     : aktifkan interaksi pengguna untuk fungsi

delta        : ukuran langkah untuk interaksi pengguna

bar          : plot batang (x adalah batas interval, y nilai interval)

histogram    : memplot frekuensi x dalam n subinterval

distribusi=n : memplot distribusi x dengan n subinterval

even         : gunakan nilai antar untuk histogram otomatis.

langkah      : memplot fungsi sebagai fungsi langkah (langkah=1,2)

adaptif      : gunakan plot adaptif (n adalah jumlah langkah minimal)

level        : plot garis level dari fungsi implisit dua variabel

outline      : menggambar batas rentang level.

Jika nilai level adalah matriks 2xn, rentang lvel akan ditarik dalam warna menggunakan gaya isian yag diberikan. Jika garis besar benar, itu akan digambar dalam warna kontur. Dengan menggunakan fitur ini,
wilayah

f(x,y) antara batas dapat ditandai. 

hue          : tambahkan warna hue ke plot level untuk menunjukkan fungsinya

            nilai

kontur       : Gunakan plot level dengan level otomatis

nc           : jumlah garis level otomatis

judul        : judul plot (default "")

xl, yl       : label untuk sumbu x dan y

lebih kecil  : jika &gt;0, akan ada lebih banyak ruang di sebelah kiri
untuk label.

vertikal     : Mengaktifkan atau menonaktifkan label vertikal. Ini mengubah
variabel global

verticallabels secara lokal untuk satu plot. Nilai 1 hanya set vertikal

teks, nilai 2 menggunakan label numerik vertikal pada sumbu y.

terisi       : mengisi plot kurva

fillcolor    : mengisi warna untuk bar dan kurva yang terisi

outline      : batas poligon yang terisi

logplot      : mengatur plot logaritma

            1 = logplot di y,
            2 = plot log di xy,
            3 = logplot dalam x

memiliki     : Sebuah string, yang menunjuk ke rutinitas plot sendiri. Dengan &gt;
pengguna, Anda mendapatkan interaksi pengguna yang sama seperti di plot2d. Rentang akan diatur sebelum setiap panggilan ke fungsi Anda.
peta         : ekspresi peta (0 lebih cepat), fungsi selalu dipetakan.

contourcolor : warna garis kontur

contourwidth : lebar garis kontur

clipping     : mengaktifkan clipping (default adalah true)

judul        : Ini dapat digunakan untuk menggambarkan plot. Judul akan muncul di
atas jalan cerita. Selain itu, label untuk sumbu x dan y dapat ditambahkan dengan

xl="string" atau yl="string". Label lain dapat ditambahkan dengan

fungsi label() atau labelbox(). Judulnya bisa unicode

string atau gambar rumus Lateks.

jaringan     : Menentukan jumlah garis grid untuk plot grid yang kompleks.

Harus merupakan pembagi dari ukuran matriks dikurangi 1 (jumlah subinterval). cgrid dapat berupa vektor [cx,cy].

Ringkasan  

Fungsi dapat merencanakan  
* ekspresi, koleksi panggilan atau fungsi dari satu variabel,
* kurva parametrik,
* data x terhadap data y,
* fungsi implisit,
* petak batang,
* jaringan kompleks,
* poligon.

Jika fungsi atau ekspresi untuk xv diberikan, plot2d() akan menghitung nilai dalam rentang yang diberikan menggunakan fungsi atau ekspresi. Itu ekspresi harus berupa ekspresi dalam variabel x. Rentang harus didefinisikan dalam parameter a dan b kecuali rentang default
[-2,2] harus digunakan. Rentang y akan dihitung secara otomatis, kecuali c dan d ditentukan, atau radius r, yang menghasilkan kisaran [-r,r] untuk x dan y. Untuk plot fungsi, plot2d akan menggunakan evaluasi adaptif fungsi secara default. Untuk mempercepat plot untuk fungsi yang rumit, matikan ini dengan &lt;adaptif, dan opsional mengurangi jumlah interval n. Selain itu, plot2d() akan secara default menggunakan pemetaan. Yaitu, itu akan menghitung elemen plot untuk elemen. Jika ekspresi atau fungsi Anda dapat menangani a vector x, Anda dapat menonaktifkannya dengan &lt;maps untuk evaluasi yang lebih cepat.

Perhatikan bahwa plot adaptif selalu dihitung elemen untuk elemen.  
Jika fungsi atau ekspresi untuk xv dan untuk yv ditentukan, plot2d() akan menghitung kurva dengan nilai xv sebagai koordinat x dan nilai yv sebagai koordinat y. Dalam hal ini, rentang harus didefinisikan untuk parameter menggunakan xmin, xmax. Ekspresi yang terkandung dalam string harus selalu ekspresi dalam variabel parameter x.

## Soal
1. Buatlah plot 2 dimensi dari fungsi

dengan a=4 dan interval dari x=-1 sampai x=1. Lalu, buatlah plot
tersebut dalam grid 3 dan ketebalan 3!

\>a:=4; expr &=exp(a\*(x^2)/a);
\>plot2d(expr,-1,1,grid=3,thickness=3):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-147.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-147.png)

2. Buatlah plot 2 dimensi dari fungsi 

dengan nilai parameternya adalah 5, interval x nya dari 1 sampai 2

\>a=5; expr &=(x^2-a\*x);
\>plot2d(expr,1,2):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-148.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-148.png)
3. Selidi dimanakah fungsi f(x) berikut naik dan turun

\>expr &= ((1/3)\*x^3-x^2-3\*x+4);
\>plot2d(expr,-4,5):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-149.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot2D-149.png)

Nama : Alya Putri Medilasari

NIM  : 23030630018

Kelas: Matematika B 2023

## Menggambar Plot 3D dengan EMT 

Ini adalah pengenalan plot 3D di Euler. Kami membutuhkan plot 3D untuk memvisualisasikan fungsi dari dua variabel.

Euler menggambar fungsi seperti itu menggunakan algoritma pengurutan untuk menyembunyikan bagian di latar belakang. Secara umum, Euler menggunakan proyeksi pusat. Defaultnya adalah dari kuadran x-y positif ke arah asal x = y = z = 0, tetapi sudut = 0 ? melihat dari arah sumbu y. Sudut pandang dan ketinggian dapat diubah.

Euler bisa merencanakan
* permukaan dengan bayangan dan garis level atau rentang level,
* awan poin,
* kurva parametrik,
* permukaan implisit.

Plot 3D dari suatu fungsi menggunakan plot3d. Cara termudah adalah dengan memplot ekspresi dalam x dan y. Parameter r mengatur kisaran plot sekitar (0,0).

\>aspect(1.5); plot3d("x^2+sin(y)",-5,5,0,6\*pi):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-001.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-001.png)
# Fungsi Dua Variabel

Untuk grafik suatu fungsi, gunakan
* ekspresi sederhana dalam x dan y,
* nama fungsi dari dua variabel l
* atau matriks data.

Defaultnya adalah kisi kawat yang diisi dengan warna berbeda di kedua sisi. Perhatikan bahwa jumlah default interval kisi adalah 10, tetapi plot menggunakan jumlah default persegi panjang 40x40 untuk membuat
permukaan. Ini bisa diubah.

* n = 40, n = [40,40]: jumlah garis grid di setiap arah
* grid= 10, grid = [10,10]: jumlah garis kisi di setiap arah.

Kami menggunakan default n = 40 dan grid = 10.

\>plot3d("x^2+y^2"):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-002.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-002.png)

Interaksi pengguna dimungkinkan dengan&gt; user parameter. Pengguna dapat menekan tombol berikut.

* left,right,up,down: putar sudut pandang
* +, -: memperbesar atau memperkecil
* a: menghasilkan anaglyph (lihat di bawah)
* l: beralih memutar sumber cahaya (lihat di bawah)
* space: reset ke default
* return: interaksi akhir

\>plot3d("exp(-x^2+y^2)",\>user, ...  

\>     title="Turn with the vector keys (press return to finish)"):
![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-003.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-003.png)

Rentang plot untuk fungsi dapat ditentukan dengan
* a, b: rentang-x
* c, d: rentang y
* r: persegi simetris di sekitar (0,0).
* n: jumlah subinterval untuk plot.

Ada beberapa parameter untuk menskalakan fungsi atau mengubah tampilan grafik.

fscale: menskalakan ke nilai fungsi (defaultnya adalah &lt;fscale).

scale: angka atau vektor 1x2 untuk skala ke arah x dan y.

frame: jenis bingkai (default 1)

\>plot3d("exp(-(x^2+y^2)/5)",r=10,n=80,fscale=4,scale=1.2,frame=3,\>user):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-004.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-004.png)

Tampilan dapat diubah dengan berbagai cara.
* distance: jarak pandang ke plot.
* zoom: nilai zoom.
* angle: sudut ke sumbu y negatif dalam radian.
* height: ketinggian tampilan dalam radian.

Nilai default bisa diperiksa atau diubah dengan fungsi view (). Ini mengembalikan parameter dalam urutan di atas.

\>view

    [5,  2.6,  2,  0.4]

Jarak yang lebih dekat membutuhkan lebih sedikit zoom. Efeknya lebih seperti lensa sudut lebar.

Dalam contoh berikut, sudut = 0 dan tinggi = 0 dilihat dari sumbu y negatif. Label sumbu untuk y disembunyikan dalam kasus ini.

\>plot3d("x^2+y",distance=3,zoom=1,angle=pi/2,height=0):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-005.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-005.png)

Plot selalu terlihat ke tengah plot kubus. Anda dapat memindahkan
pusat dengan parameter tengah.

\>plot3d("x^4+y^2",a=0,b=1,c=-1,d=1,angle=-20°,height=20°, ...  
\>     center=[0.4,0,0],zoom=5):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-006.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-006.png)
Plot diskalakan agar sesuai dengan kubus satuan untuk dilihat. Jadi tidak perlu mengubah jarak atau zoom tergantung ukuran plot. Namun, label mengacu pada ukuran sebenarnya.

Jika Anda mematikannya dengan scale = false, Anda harus berhati-hati, bahwa plot masih pas dengan jendela plotting, dengan mengubah jarak pandang atau zoom, dan memindahkan pusat.

\>plot3d("5\*exp(-x^2-y^2)",r=2,<fscale,<scale,distance=13,height=50°, ...  

\>     center=[0,0,-2],frame=3):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-007.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-007.png)
Plot kutub juga tersedia. The parameter polar= true menggambarkan plot kutub. Fungsi tersebut harus tetap merupakan fungsi dari x dan y. Parameter "fscale" menskalakan fungsi dengan skala sendiri. Jika tidak, fungsi diskalakan agar sesuai dengan kubus.

\>plot3d("1/(x^2+y^2+1)",r=5,\>polar, ...  
\>   fscale=2,\>hue,n=100,zoom=4,\>contour,color=blue):
![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-008.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-008.png)

\>function f(r) := exp(-r/2)\*cos(r); ...  
\>   plot3d("f(x^2+y^2)",\>polar,scale=[1,1,0.4],r=pi,frame=3,zoom=4):
![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-009.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-009.png)

Parameter memutar memutar fungsi dalam x di sekitar sumbu x.
* rotate = 1: Menggunakan sumbu x
* rotate = 2: Menggunakan sumbu z
  
\>plot3d("x^2+1",a=-1,b=1,rotate=true,grid=5):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-010.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-010.png)

\>plot3d("x^2+1",a=-1,b=1,rotate=2,grid=5):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-011.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-011.png)

\>plot3d("sqrt(25-x^2)",a=0,b=5,rotate=1):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-012.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-012.png)

\>plot3d("x\*sin(x)",a=0,b=6pi,rotate=2):
![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-013.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-013.png)
Ini adalah plot dengan tiga fungsi

\>plot3d("x","x^2+y^2","y",r=2,zoom=3.5,frame=3):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-014.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-014.png)

# Plot Kontur

Untuk plot, Euler menambahkan garis kisi. Alih-alih, dimungkinkan untuk menggunakan garis level dan corak satu warna atau corak warna spektral. Euler dapat menggambar ketinggian fungsi pada plot dengan shading. Di semua plot 3D, Euler dapat menghasilkan anaglyph merah / cyan.

-&gt; hue: Mengaktifkan bayangan terang, bukan kabel.
-&gt; contour: Membuat plot garis kontur otomatis pada plot.
- level = ... (atau level): Vektor nilai untuk garis kontur.

Standarnya adalah level = "auto", yang menghitung beberapa baris level secara otomatis. Seperti yang Anda lihat di plot, level sebenarnya adalah rentang level.

Gaya default dapat diubah. Untuk plot kontur berikut, kami menggunakan kisi yang lebih halus untuk 100x100 titik, menskalakan fungsi dan plot, dan menggunakan sudut pandang yang berbeda.

\>plot3d("exp(-x^2-y^2)",r=2,n=100,level="thin", ...  
\>    \>contour,\>spectral,fscale=1,scale=1.1,angle=45°,height=20°):
![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-015.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-015.png)

\>plot3d("exp(x\*y)",angle=100°,\>contour,color=green):
![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-016.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-016.png)

Bayangan default menggunakan warna abu-abu. Tetapi berbagai spektrum warna juga tersedia.

-&gt; spectral: Menggunakan skema spektral default
- color = ...: Menggunakan warna khusus atau skema spektral
  
Untuk plot berikut, kami menggunakan skema spektral default dan menambah jumlah poin untuk mendapatkan tampilan yang sangat mulus.

\>plot3d("x^2+y^2",\>spectral,\>contour,n=100):
![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-017.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-017.png)
Alih-alih garis level otomatis, kami juga dapat mengatur nilai garis level. Ini akan menghasilkan garis level tipis, bukan rentang level.

\>plot3d("x^2-y^2",0,5,0,5,level=-1:0.1:1,color=redgreen):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-018.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-018.png)
Dalam plot berikut, kami menggunakan dua pita level yang sangat luas dari -0,1 hingga 1, dan dari 0,9 hingga 1. Ini dimasukkan sebagai
matriks dengan batas level sebagai kolom.

Selain itu, kami melapisi kisi dengan 10 interval di setiap arah.

\>plot3d("x^2+y^3",level=[-0.1,0.9;0,1], ...  
\>     \>spectral,angle=30°,grid=10,contourcolor=gray):
![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-019.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-019.png)

Dalam contoh berikut, kami memplot set, di mana

Kami menggunakan satu garis tipis untuk garis level.

\>plot3d("x^y-y^x",level=0,a=0,b=6,c=0,d=6,contourcolor=red,n=100):
![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-020.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-020.png)

Dimungkinkan untuk menunjukkan bidang kontur di bawah plot. Warna dan jarak ke plot dapat ditentukan.

\>plot3d("x^2+y^4",\>cp,cpcolor=green,cpdelta=0.2):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-021.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-021.png)

Berikut beberapa gaya lainnya. Kami selalu mematikan bingkai, dan
menggunakan berbagai skema warna untuk plot dan kisi.

\>figure(2,2); ...  
\>   expr="y^3-x^2"; ...  
\>   figure(1);  ...  
\>     plot3d(expr,<frame,\>cp,cpcolor=spectral); ...  
\>   figure(2);  ...  
\>     plot3d(expr,<frame,\>spectral,grid=10,cp=2); ...  
\>   figure(3);  ...  
\>     plot3d(expr,<frame,\>contour,color=gray,nc=5,cp=3,cpcolor=greenred); ...  
\>   figure(4);  ...  
\>     plot3d(expr,<frame,\>hue,grid=10,\>transparent,\>cp,cpcolor=gray); ...  
\>   figure(0):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-022.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-022.png)

Ada beberapa skema spektral lain, diberi nomor dari 1 hingga 9. Tetapi
Anda juga dapat menggunakan color=value, di mana nilai

* spectral: untuk rentang dari biru hingga merah
* white: untuk rentang yang lebih redup
* yellowblue,purplegreen,blueyellow,greenred
* blueyellow, greenpurple,yellowblue,redgreen

\>figure(3,3); ...  
\>   for i=1:9;  ...  
\>     figure(i); plot3d("x^2+y^2",spectral=i,\>contour,\>cp,<frame,zoom=4);  ...  
\>   end; ...  
\>   figure(0):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-023.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-023.png)

Sumber cahaya dapat diubah dengan l dan tombol kursor selama interaksi
pengguna. Itu juga dapat diatur dengan parameter.

- light : arah cahaya
- amb: cahaya ambient antara 0 dan 1

Perhatikan bahwa program tidak membuat perbedaan antara sisi-sisi plot. Tidak ada bayangan. Untuk ini, Anda membutuhkan Povray.

\>plot3d("-x^2-y^2", ...  
\>     hue=true,light=[0,1,1],amb=0,user=true, ...  
\>     title="Press l and cursor keys (return to exit)"):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-024.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-024.png)
Parameter warna mengubah warna permukaan. Warna garis level juga dapat diubah.

\>plot3d("-x^2-y^2",color=rgb(0.2,0.2,0),hue=true,frame=false, ...  
\>     zoom=3,contourcolor=red,level=-2:0.1:1,dl=0.01):
![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-025.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-025.png)

Warna 0 memberikan efek pelangi khusus.

\>plot3d("x^2/(x^2+y^2+1)",color=0,hue=true,grid=10):
![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-026.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-026.png)

Permukaannya juga bisa transparan.

\>plot3d("x^2+y^2",\>transparent,grid=10,wirecolor=red):
![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-027.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-027.png)

# Plot Implisit

Ada juga plot implisit dalam tiga dimensi. Euler menghasilkan pemotongan melalui objek. Fitur plot3d termasuk plot implisit. Plot ini menunjukkan himpunan nol fungsi dalam tiga variabel.

Solusi dari
$$f(x,y,z) = 0$$dapat divisualisasikan dalam potongan sejajar dengan bidang x-y-,
x-z-, dan y-z.

* implisit = 1: potong sejajar bidang y-z
* implisit = 2: potong sejajar dengan bidang x-z
* implisit = 4: potong sejajar bidang x-y

Tambahkan nilai-nilai ini, jika Anda suka. Dalam contoh yang kami plot
$$M = \{ (x,y,z) : x^2+y^3+zy=1 \}$$\>plot3d("x^2+y^3+z\*y-1",r=5,implicit=3):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-030.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-030.png)
\>c=1; d=1;

\>plot3d("((x^2+y^2-c^2)^2+(z^2-1)^2)\*((y^2+z^2-c^2)^2+(x^2-1)^2)\*((z^2+x^2-c^2)^2+(y^2-1)^2)-d",r=2,<frame,\>implicit,\>user):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-031.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-031.png)
\>plot3d("x^2+y^2+4\*x\*z+z^3",\>implicit,r=2,zoom=2.5):
![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-032.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-032.png)

# Plotting 3D Data

Sama seperti plot2d, plot3d menerima data. Untuk objek 3D, Anda perlu
memberikan matriks nilai x, y dan z, atau tiga fungsi atau ekspresi fx
(x, y), fy (x, y), fz (x, y).
$$\gamma(t,s) = (x(t,s),y(t,s),z(t,s))$$Karena x, y, z adalah matriks, kita asumsikan bahwa (t, s) berjalan melalui kotak persegi. Hasilnya, Anda dapat memplot gambar persegi
panjang di luar angkasa.

Anda dapat menggunakan bahasa matriks Euler untuk menghasilkankoordinat secara efektif.

Dalam contoh berikut, kami menggunakan vektor nilai t dan vektor kolom nilai s untuk membuat parameter permukaan bola. Dalam gambar kita bisa menandai daerah, dalam kasus kita daerah kutub.

\>t=linspace(0,2pi,180); s=linspace(-pi/2,pi/2,90)'; ...  
\>   x=cos(s)\*cos(t); y=cos(s)\*sin(t); z=sin(s); ...  
\>   plot3d(x,y,z,\>hue, ...  
\>   color=blue,<frame,grid=[10,20], ...  
\>   values=s,contourcolor=red,level=[90°-24°;90°-22°], ...  
\>   scale=1.4,height=50°):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-034.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-034.png)

Berikut adalah contoh grafik dari suatu fungsi.

\>t=-1:0.1:1; s=(-1:0.1:1)'; plot3d(t,s,t\*s,grid=10):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-035.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-035.png)
Namun, kita bisa membuat semua jenis permukaan. Ini adalah permukaan yang sama sebagai suatu fungsi

\>plot3d(t\*s,t,s,angle=180°,grid=10):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-036.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-036.png)

Dengan lebih banyak usaha, kami dapat menghasilkan banyak permukaan.

Dalam contoh berikut, kami membuat tampilan berbayang dari bola yang terdistorsi. Koordinat biasa untuk bola adalah dengan
Kami menyimpangkan ini dengan sebuah faktor

\>t=linspace(0,2pi,320); s=linspace(-pi/2,pi/2,160)'; ...  
\>   d=1+0.2\*(cos(4\*t)+cos(8\*s)); ...  
\>   plot3d(cos(t)\*cos(s)\*d,sin(t)\*cos(s)\*d,sin(s)\*d,hue=1, ...  
\>     light=[1,0,1],frame=0,zoom=5):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-037.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-037.png)

Tentu saja, point cloud juga dimungkinkan. Untuk memplot data titik
dalam ruang, kita membutuhkan tiga vektor sebagai koordinat titik.

Gayanya sama seperti di plot2d dengan points = true;

\>n=500;  ...  
\>     plot3d(normal(1,n),normal(1,n),normal(1,n),points=true,style="."):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-038.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-038.png)
Juga dimungkinkan untuk memplot kurva dalam 3D. Dalam kasus ini, lebih mudah untuk menghitung sebelumnya titik-titik kurva. Untuk kurva di bidang kita menggunakan urutan koordinat dan parameter wire = true.

\>t=linspace(0,8pi,500); ...  
\>   plot3d(sin(t),cos(t),t/10,\>wire,zoom=3):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-039.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-039.png)
\>t=linspace(0,4pi,1000); plot3d(cos(t),sin(t),t/2pi,\>wire, ...  
\>   linewidth=3,wirecolor=blue):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-040.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-040.png)
\>X=cumsum(normal(3,100)); ...  
\>    plot3d(X[1],X[2],X[3],\>anaglyph,\>wire):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-041.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-041.png)
EMT juga dapat memplot dalam mode anaglyph. Untuk melihat plot seperti
itu, Anda membutuhkan red/cyan glasses.

\> plot3d("x^2+y^3",\>anaglyph,\>contour,angle=30°):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-042.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-042.png)
Seringkali, skema warna spektral digunakan untuk plot. Ini menekankan
ketinggian fungsinya.

\>plot3d("x^2\*y^3-y",\>spectral,\>contour,zoom=3.2):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-043.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-043.png)

Euler juga dapat memplot permukaan berparameter, jika parameternya adalah nilai x, y, dan z dari gambar kisi persegi panjang di dalam
ruang.

Untuk demo berikut, kami menyiapkan parameter u- dan v-, dan menghasilkan koordinat ruang dari ini.

\>u=linspace(-1,1,10); v=linspace(0,2\*pi,50)'; ...  
\>   X=(3+u\*cos(v/2))\*cos(v); Y=(3+u\*cos(v/2))\*sin(v); Z=u\*sin(v/2); ...  
\>   plot3d(X,Y,Z,\>anaglyph,<frame,\>wire,scale=2.3):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-044.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-044.png)

Berikut adalah contoh yang lebih rumit, yang megah dengan red/cyan glasses.

\>u:=linspace(-pi,pi,160); v:=linspace(-pi,pi,400)';  ...  
\>   x:=(4\*(1+.25\*sin(3\*v))+cos(u))\*cos(2\*v); ...  
\>   y:=(4\*(1+.25\*sin(3\*v))+cos(u))\*sin(2\*v); ...  
\>    z=sin(u)+2\*cos(3\*v); ...  
\>   plot3d(x,y,z,frame=0,scale=1.5,hue=1,light=[1,0,-1],zoom=2.8,\>anaglyph):
![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-045.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-045.png)

# Plot Statistik

Plot batang juga dimungkinkan. Untuk ini, kami harus menyediakan

* x: vektor baris dengan n + 1 elemen
* y: vektor kolom dengan n + 1 elemen
* z: nxn matriks nilai.

z bisa lebih besar, tetapi hanya nilai nxn yang akan digunakan.

Dalam contoh, pertama-tama kita menghitung nilainya. Kemudian kita menyesuaikan x dan y, sehingga vektor berpusat pada nilai yang
digunakan.

\>x=-1:0.1:1; y=x'; z=x^2+y^2; ...  
\>   xa=(x|1.1)-0.05; ya=(y\_1.1)-0.05; ...  
\>   plot3d(xa,ya,z,bar=true):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-046.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-046.png)

Dimungkinkan untuk membagi plot permukaan menjadi dua bagian atau lebih.
 
\>x=-1:0.1:1; y=x'; z=x+y; d=zeros(size(x)); ...  
\>   plot3d(x,y,z,disconnect=2:2:20):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-047.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-047.png)

Jika memuat atau membuat matriks data M dari file dan perlu memplotnya dalam 3D, Anda dapat menskalakan matriks ke [-1,1] dengan skala (M), atau menskalakan matriks dengan&gt; zscale. Ini dapat dikombinasikan
dengan faktor penskalaan individu yang diterapkan sebagai tambahan.

\>i=1:20; j=i'; ...  
\>   plot3d(i\*j^2+100\*normal(20,20),\>zscale,scale=[1,1,1.5],angle=-40°,zoom=1.8):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-048.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-048.png)

\>Z=intrandom(5,100,6); v=zeros(5,6); ...  
\>   loop 1 to 5; v[#]=getmultiplicities(1:6,Z[#]); end; ...  
\>   columnsplot3d(v',scols=1:5,ccols=[1:5]):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-049.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-049.png)

# Permukaan Benda Putar

\>plot2d("(x^2+y^2-1)^3-x^2\*y^3",r=1.3, ...  
\>   style="#",color=red,<outline, ...  
\>   level=[-2;0],n=100):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-050.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-050.png)

\>ekspresi &= (x^2+y^2-1)^3-x^2\*y^3; $ekspresi
$$\left(y^2+x^2-1\right)^3-x^2\,y^3$$Kami ingin memutar kurva jantung di sekitar sumbu y. Inilah ungkapan yang mendefinisikan hati:

Selanjutnya kita atur

\>function fr(r,a) &= ekspresi with [x=r\*cos(a),y=r\*sin(a)] | trigreduce; $fr(r,a)
$$\left(r^2-1\right)^3+\frac{\left(\sin \left(5\,a\right)-\sin \left(  3\,a\right)-2\,\sin a\right)\,r^5}{16}$$Hal ini memungkinkan untuk menentukan fungsi numerik, yang menyelesaikan r, jika a diberikan. Dengan fungsi itu kita dapat
memplot jantung yang berubah sebagai permukaan parametrik.

\>function map f(a) := bisect("fr",0,2;a); ...  
\>   t=linspace(-pi/2,pi/2,100); r=f(t);  ...  
\>   s=linspace(pi,2pi,100)'; ...  
\>   plot3d(r\*cos(t)\*sin(s),r\*cos(t)\*cos(s),r\*sin(t), ...  
\>   \>hue,<frame,color=red,zoom=4,amb=0,max=0.7,grid=12,height=50°):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-053.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-053.png)
Berikut ini adalah plot 3D dari gambar di atas yang diputar di sekitar
sumbu z. Kami mendefinisikan fungsi, yang mendeskripsikan objek.

\>function f(x,y,z) ...

    r=x^2+y^2;
    return (r+z^2-1)^3-r*z^3;
     endfunction

\>plot3d("f(x,y,z)", ...  
\>   xmin=0,xmax=1.2,ymin=-1.2,ymax=1.2,zmin=-1.2,zmax=1.4, ...  
\>   implicit=1,angle=-30°,zoom=2.5,n=[10,60,60],\>anaglyph):
![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-054.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-054.png)

# Special 3D Plots

Fungsi plot3d bagus untuk dimiliki, tetapi tidak memenuhi semua kebutuhan. Selain rutinitas yang lebih mendasar, Anda bisa mendapatkan plot berbingkai dari objek apa pun yang Anda suka.

Meskipun Euler bukan program 3D, Euler dapat menggabungkan beberapa objek dasar. Kami mencoba untuk memvisualisasikan paraboloid dan garis singgung-nya.

\>function myplot ...

      y=0:0.01:1; x=(0.1:0.01:1)';
      plot3d(x,y,0.2*(x-0.1)/2,<scale,<frame,>hue, ..
        hues=0.5,>contour,color=orange);
      h=holding(1);
      plot3d(x,y,(x^2+y^2)/2,<scale,<frame,>contour,>hue);
      holding(h);
    endfunction

Sekarang framedplot () menyediakan bingkai, dan menyetel tampilan.
\>framedplot("myplot",[0.1,1,0,1,0,1],angle=-45°, ...  
\>     center=[0,0,-0.7],zoom=6):
![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-055.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-055.png)

Dengan cara yang sama, Anda dapat memplot bidang kontur secara manual.
Perhatikan bahwa plot3d () menyetel jendela ke fullwindow () secara
default, tetapi plotcontourplane () mengasumsikannya.

\>x=-1:0.02:1.1; y=x'; z=x^2-y^4;

\>function myplot (x,y,z) ...  
\>  
<pre class="udf">      zoom(2);
      wi=fullwindow();
      plotcontourplane(x,y,z,level="auto",<scale);
      plot3d(x,y,z,>hue,<scale,>add,color=white,level="thin");
      window(wi);
      reset();
    endfunction
</pre>
\>myplot(x,y,z):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-056.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-056.png)

# Animasi

Salah satu fungsi yang memanfaatkan teknik ini adalah memutar. Itu dapat mengubah sudut pandang dan menggambar ulang plot 3D. Fungsi tersebut memanggil addpage () untuk setiap plot baru. Akhirnya itu menjiwai plot.

Harap pelajari sumber rotasi untuk melihat lebih detail.

\>function testplot () := plot3d("x^2+y^3"); ...  
\>   rotate("testplot"); testplot():

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-057.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-057.png)

# Menggambar Povray

Dengan bantuan file Euler povray.e, Euler dapat menghasilkan file Povray. Hasilnya sangat bagus untuk dilihat.

Anda perlu menginstal Povray (32bit atau 64bit)dari

  <a href="http://www.povray.org/,">http://www.povray.org/,</a>

dan meletakkan sub-direktori "bin" Povray ke dalam jalur lingkungan, atau menyetel variabel "defaultpovray" dengan jalur lengkap yang
mengarah ke "pvengine.exe".

Antarmuka Povray dari Euler menghasilkan file Povray di direktori home pengguna, dan memanggil Povray untuk mengurai file-file ini. Nama file default adalah current.pov, dan direktori default adalah eulerhome (), biasanya c: \ Users \ Username \ Euler. Povray menghasilkan file PNG, yang dapat dimuat oleh Euler ke dalam notebook. Untuk membersihkan
file-file ini, gunakan povclear ().

Fungsi pov3d memiliki semangat yang sama dengan plot3d. Ini dapat menghasilkan grafik fungsi f (x, y), atau permukaan dengan koordinat X, Y, Z dalam matriks, termasuk garis level opsional. Fungsi ini memulai raytracer secara otomatis, dan memuat pemandangan ke dalam notebook Euler.

Selain pov3d (), ada banyak fungsi yang menghasilkan objek Povray. Fungsi-fungsi ini mengembalikan string, berisi kode Povray untuk
objek. Untuk menggunakan fungsi ini, mulai file Povray dengan povstart (). Kemudian gunakan writeln (...) untuk menulis objek ke file adegan. Terakhir, akhiri file dengan povend (). Secara default, raytracer akan mulai, dan PNG akan dimasukkan ke dalam notebook Euler.

Fungsi objek memiliki parameter yang disebut "look", yang membutuhkan string dengan kode Povray untuk tekstur dan penyelesaian objek. Fungsi\ povlook () dapat digunakan untuk menghasilkan string ini. Ini memiliki parameter untuk warna, transparansi, Phong Shading dll. 

Perhatikan bahwa alam semesta Povray memiliki sistem koordinat lain. Antarmuka ini menerjemahkan semua koordinat ke sistem Povray. Jadi Anda dapat terus berpikir dalam sistem koordinat Euler dengan z menunjuk ke atas secara vertikal, sumbu a nd x, y, z di tangan kanan.

Anda perlu memuat file povray.

\>load povray;

Pastikan, direktori bin Povray ada di jalurnya. Jika tidak, edit variabel berikut sehingga berisi path ke povray yang dapat dieksekusi.
 
\>defaultpovray="C:\\Program Files\\POV-Ray\\v3.7\\bin\\pvengine.exe"

    C:\Program Files\POV-Ray\v3.7\bin\pvengine.exe

Untuk pertamakali, kami memplot fungsi sederhana. Perintah berikut menghasilkan file povray di direktori pengguna Anda, dan menjalankan Povray untuk menelusuri file ini.
 
Jika Anda memulai perintah berikut, GUI Povray akan terbuka,
menjalankan file, dan menutup secara otomatis. Karena alasan keamanan,
Anda akan ditanya, apakah Anda ingin mengizinkan file exe dijalankan.
Anda dapat menekan batal untuk menghentikan pertanyaan lebih lanjut.
Anda mungkin harus menekan OK di jendela Povray untuk mengetahui
dialog start-up Povray. 

\>plot3d("x^2+y^2",zoom=2):
 
![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-058.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-058.png)

\>pov3d("x^2+y^2",zoom=3);
 
![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-059.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-059.png)
 
Kita bisa membuat fungsinya transparan dan menambahkan hasil akhir lainnya. Kita juga bisa menambahkan garis level ke plot fungsi.

\>pov3d("x^2+y^3",axiscolor=red,angle=-45°,\>anaglyph, ...  
\>     look=povlook(cyan,0.2),level=-1:0.5:1,zoom=3.8);

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-060.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-060.png)

Terkadang perlu untuk mencegah penskalaan fungsi, dan menskalakan fungsi dengan tangan.

Kami memplot himpunan titik di bidang kompleks, di mana hasil kali jarak ke 1 dan -1 sama dengan 1.

\>pov3d("((x-1)^2+y^2)\*((x+1)^2+y^2)/40",r=1.5, ...  
\>     angle=-120°,level=1/40,dlevel=0.005,light=[-1,1,1],height=45°,n=50, ...  
\>     <fscale,zoom=3.8);

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-061.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-061.png)

# Merencanakan dengan Koordinat

Alih-alih fungsi, kita bisa memplot dengan koordinat. Seperti pada plot3d, kita membutuhkan tiga matriks untuk mendefinisikan objeknya.

Dalam contoh ini, kita memutar fungsi di sekitar sumbu z.

\>function f(x) := x^3-x+1; ...  
\>   x=-1:0.01:1; t=linspace(0,2pi,8)'; ...  
\>   Z=x; X=cos(t)\*f(x); Y=sin(t)\*f(x); ...  
\>   pov3d(X,Y,Z,angle=40°,height=20°,axis=0,zoom=4,light=[10,-5,5]);

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-062.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-062.png)

Dalam contoh berikut, kami memplot gelombang teredam. Kami menghasilkan gelombang dengan bahasa matriks Euler.

Kami juga menunjukkan, bagaimana objek tambahan dapat ditambahkan ke adegan pov3d. Untuk pembuatan objek, lihat contoh berikut. Perhatikan bahwa plot3d menskalakan plot, sehingga sesuai dengan kubus satuan

\>r=linspace(0,1,80); phi=linspace(0,2pi,80)'; ...  
\>   x=r\*cos(phi); y=r\*sin(phi); z=exp(-5\*r)\*cos(8\*pi\*r)/3;  ...  
\>   pov3d(x,y,z,zoom=5,axis=0,add=povsphere([0,0,0.5],0.1,povlook(green)), ...  
\>     w=500,h=300);

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-063.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-063.png)

Dengan metode naungan lanjutan Povray, sangat sedikit titik yang dapat menghasilkan permukaan yang sangat halus. Hanya di perbatasan dan dalam bayangan, triknya mungkin menjadi jelas.

Untuk ini, kita perlu menambahkan vektor normal di setiap titik matriks.

\>Z &= x^2\*y^3
    
                                     2  3
                                    x  y
    
Persamaan permukaannya adalah [x, y, Z]. Kami menghitung dua turunan menjadi x dan y dari ini dan mengambil produk silang sebagai normal.

\>dx &= diff([x,y,Z],x); dy &= diff([x,y,Z],y);

Kami mendefinisikan normal sebagai produk silang dari turunan ini, dan mendefinisikan fungsi koordinat.\

\>N &= crossproduct(dx,dy); NX &= N[1]; NY &= N[2]; NZ &= N[3]; N,
    
                                   3       2  2
                           [- 2 x y , - 3 x  y , 1]
    
We use only 25 points.

\>x=-1:0.5:1; y=x';

\>pov3d(x,y,Z(x,y),angle=10°, ...  
\>     xv=NX(x,y),yv=NY(x,y),zv=NZ(x,y),<shadow);

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-064.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-064.png)

Berikut ini adalah simpul Trefoil yang dilakukan oleh A. Busser di Povray. Ada versi perbaikannya dalam contoh.

  <a href="Examples\Trefoil Knot.html">Trefoil Knot</a>  

Untuk tampilan yang bagus dengan tidak terlalu banyak titik, kami menambahkan vektor normal di sini. Kami menggunakan Maxima untuk menghitung normal bagi kami. Pertama, tiga fungsi koordinat sebagai
ekspresi simbolik.

\>X &= ((4+sin(3\*y))+cos(x))\*cos(2\*y); ...  
\>   Y &= ((4+sin(3\*y))+cos(x))\*sin(2\*y); ...  
\>   Z &= sin(x)+2\*cos(3\*y);

Kemudian dua vektor turunannya menjadi x dan y.

\>dx &= diff([X,Y,Z],x); dy &= diff([X,Y,Z],y);

Sekarang normal, yang merupakan produk persilangan dari dua turunannya.

\>dn &= crossproduct(dx,dy);

Kami sekarang mengevaluasi semua ini secara numerik.

\>x:=linspace(-%pi,%pi,40); y:=linspace(-%pi,%pi,100)';

Vektor normal adalah evaluasi dari ekspresi simbolik dn [i] untuk i =1,2,3. Sintaks untuk ini adalah &amp; "expresi" (parameter). Ini adalahn alternatif metode pada contoh sebelumnya, di mana kita mendefinisikan
ekspresi simbolik NX, NY, NZ terlebih dahulu.

\>pov3d(X(x,y),Y(x,y),Z(x,y),axis=0,zoom=5,w=450,h=350, ...  
\>     <shadow,look=povlook(gray), ...  
\>     xv=&"dn[1]"(x,y), yv=&"dn[2]"(x,y), zv=&"dn[3]"(x,y));

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-065.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-065.png)

Kami juga dapat membuat grid dalam 3D.

\>povstart(zoom=4); ...  
\>   x=-1:0.5:1; r=1-(x+1)^2/6; ...  
\>   t=(0°:30°:360°)'; y=r\*cos(t); z=r\*sin(t); ...  
\>   writeln(povgrid(x,y,z,d=0.02,dballs=0.05)); ...  
\>   povend();

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-066.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-066.png)
Dengan povgrid (), kurva dimungkinkan.

\>povstart(center=[0,0,1],zoom=3.6); ...  
\>   t=linspace(0,2,1000); r=exp(-t); ...  
\>   x=cos(2\*pi\*10\*t)\*r; y=sin(2\*pi\*10\*t)\*r; z=t; ...  
\>   writeln(povgrid(x,y,z,povlook(red))); ...  
\>   writeAxis(0,2,axis=3); ...  
\>   povend();

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-067.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-067.png)

# Objek Povray

Di atas, kami menggunakan pov3d untuk memplot permukaan. Antarmuka povray di Euler juga dapat menghasilkan objek Povray. Objek-objek ini disimpan sebagai string di Euler, dan perlu ditulis ke file Povray.

Kami memulai output dengan povstart ().

\>povstart(zoom=4);

Pertama kita tentukan tiga silinder, dan simpan dalam string di Euler.

Fungsi povx () dll. Hanya mengembalikan vektor [1,0,0], yang bisa digunakan sebagai gantinya.

\>c1=povcylinder(-povx,povx,1,povlook(red)); ...  
\>   c2=povcylinder(-povy,povy,1,povlook(green)); ...  
\>   c3=povcylinder(-povz,povz,1,povlook(blue)); ...  
\>  
String berisi kode Povray, yang tidak perlu kita pahami pada saat itu.

\>c1

    cylinder { &lt;-1,0,0&gt;, &lt;1,0,0&gt;, 1
     texture { pigment { color rgb &lt;0.564706,0.0627451,0.0627451&gt; }  } 
     finish { ambient 0.2 } 
     }

Seperti yang Anda lihat, kami menambahkan tekstur ke objek dalam tiga warna berbeda.

Itu dilakukan oleh povlook (), yang mengembalikan string dengan kode Povray yang relevan. Kita dapat menggunakan warna Euler default, atau menentukan warna kita sendiri. Kami juga dapat menambahkan transparansi, atau mengubah cahaya sekitar.

\>povlook(rgb(0.1,0.2,0.3),0.1,0.5)

     texture { pigment { color rgbf &lt;0.101961,0.2,0.301961,0.1&gt; }  } 
     finish { ambient 0.5 } 
    
Sekarang kita mendefinisikan objek interseksi, dan menulis hasilnya ke
file.

\>writeln(povintersection([c1,c2,c3]));

Perpotongan tiga silinder sulit untuk divisualisasikan, jika Anda belum pernah melihatnya sebelumnya.

\>povend;
![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-068.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-068.png)

Fungsi berikut menghasilkan fraktal secara rekursif.

Fungsi pertama menunjukkan, bagaimana Euler menangani objek Povray sederhana. Fungsi povbox () mengembalikan string, berisi koordinat kotak, tekstur, dan hasil akhir.

\>function onebox(x,y,z,d) := povbox([x,y,z],[x+d,y+d,z+d],povlook());

\>function fractal (x,y,z,h,n) ...  
\>  
<pre class="udf">     if n==1 then writeln(onebox(x,y,z,h));
     else
       h=h/3;
       fractal(x,y,z,h,n-1);
       fractal(x+2*h,y,z,h,n-1);
       fractal(x,y+2*h,z,h,n-1);
       fractal(x,y,z+2*h,h,n-1);
       fractal(x+2*h,y+2*h,z,h,n-1);
       fractal(x+2*h,y,z+2*h,h,n-1);
       fractal(x,y+2*h,z+2*h,h,n-1);
       fractal(x+2*h,y+2*h,z+2*h,h,n-1);
       fractal(x+h,y+h,z+h,h,n-1);
     endif;
    endfunction
</pre>
\>povstart(fade=10,<shadow);

\>fractal(-1,-1,-1,2,4);

\>povend();

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-069.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-069.png)

Perbedaan memungkinkan pemotongan satu objek dari yang lain. Seperti persimpangan, ada bagian dari objek CSG Povray.

\>povstart(light=[5,-5,5],fade=10);

Untuk demonstrasi ini, kami mendefinisikan sebuah objek di Povray, daripada menggunakan string di Euler. Definisi segera ditulis ke file.

Koordinat kotak -1 berarti [-1, -1, -1].

\>povdefine("mycube",povbox(-1,1));

Kita bisa menggunakan objek ini di povobject (), yang mengembalikan string seperti biasa.

\>c1=povobject("mycube",povlook(red));

Kami menghasilkan kubus kedua, dan memutar serta menskalakannya sedikit.

\>c2=povobject("mycube",povlook(yellow),translate=[1,1,1], ...  
\>     rotate=xrotate(10°)+yrotate(10°), scale=1.2);

Kemudian kita ambil perbedaan kedua objek tersebut.

\>writeln(povdifference(c1,c2));

Sekarang tambahkan tiga sumbu.

\>writeAxis(-1.2,1.2,axis=1); ...  
\>   writeAxis(-1.2,1.2,axis=2); ...  
\>   writeAxis(-1.2,1.2,axis=4); ...  
\>   povend();

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-070.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-070.png)

# Fungsi Implisit

Povray dapat memplot himpunan di mana f (x, y, z) = 0, seperti parameter implisit di plot3d. Namun, hasilnya terlihat jauh lebih
baik.

Sintaks untuk fungsinya sedikit berbeda. Anda tidak dapat menggunakan keluaran ekspresi Maxima atau Euler.

\>povstart(angle=70°,height=50°,zoom=4);

Buat permukaan implisit. Perhatikan sintaks yang berbeda dalam ekspresi tersebut.

\>writeln(povsurface("pow(x,2)\*y-pow(y,3)-pow(z,2)",povlook(green))); ...  
\>   writeAxes(); ...  
\>   povend();

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-071.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-071.png)

# Objek Jaring

Dalam contoh ini, kami menunjukkan cara membuat objek mesh, dan menggambarnya dengan informasi tambahan.

Kami ingin memaksimalkan xy di bawah kondisi x + y = 1 dan mendemonstrasikan sentuhan tangensial dari garis level.

\>povstart(angle=-10°,center=[0.5,0.5,0.5],zoom=7);

Kami tidak dapat menyimpan objek dalam string seperti sebelumnya, karena terlalu besar. Jadi kami mendefinisikan objek dalam file Povray menggunakan #declare. Fungsi povtriangle () melakukan ini secara otomatis. Ia dapat menerima vektor normal seperti pov3d ().

Yang berikut ini mendefinisikan objek mesh, dan langsung menulisnya ke dalam file.

\>x=0:0.02:1; y=x'; z=x\*y; vx=-y; vy=-x; vz=1;

\>mesh=povtriangles(x,y,z,"",vx,vy,vz);

Sekarang kami mendefinisikan dua disk, yang akan berpotongan dengan permukaan.

\>cl=povdisc([0.5,0.5,0],[1,1,0],2); ...  
\>   ll=povdisc([0,0,1/4],[0,0,1],2);

Tulis permukaan dikurangi dua cakram.

\>writeln(povdifference(mesh,povunion([cl,ll]),povlook(green)));

Tuliskan dua persimpangan tersebut.

\>writeln(povintersection([mesh,cl],povlook(red))); ...  
\>   writeln(povintersection([mesh,ll],povlook(gray)));

Tulis titik maksimal.

\>writeln(povpoint([1/2,1/2,1/4],povlook(gray),size=2\*defaultpointsize));

Tambahkan sumbu dan selesai.

\>writeAxes(0,1,0,1,0,1,d=0.015); ...  
\>   povend();

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-072.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-072.png)
# Anaglyph di Povray
Untuk menghasilkan anaglyph untuk kacamata merah / cyan, Povray harus dijalankan dua kali dari posisi kamera yang berbeda. Ini menghasilkan dua file Povray dan dua file PNG, yang dimuat dengan fungsi
loadanaglyph ().

Tentu saja, Anda memerlukan kaca mata merah / cyan untuk melihat contoh berikut dengan benar.

Fungsi pov3d () memiliki tombol sederhana untuk menghasilkan anaglyph.

\>pov3d("-exp(-x^2-y^2)/2",r=2,height=45°,\>anaglyph, ...  
\>     center=[0,0,0.5],zoom=3.5);

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-073.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-073.png "images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-073.png")
Jika Anda membuat adegan dengan objek, Anda perlu memasukkan pembuatan adegan ke dalam fungsi, dan menjalankannya dua kali dengan nilai yang berbeda untuk parameter anaglyph.

\>function myscene ...

      s=povsphere(povc,1);
      cl=povcylinder(-povz,povz,0.5);
      clx=povobject(cl,rotate=xrotate(90°));
      cly=povobject(cl,rotate=yrotate(90°));
      c=povbox([-1,-1,0],1);
      un=povunion([cl,clx,cly,c]);
      obj=povdifference(s,un,povlook(red));
      writeln(obj);
      writeAxes();
    endfunction
</pre>
Fungsi povanaglyph () melakukan semua ini. Parameternya seperti di
povstart () dan povend () digabungkan.

\>povanaglyph("myscene",zoom=4.5);

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-074.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-074.png)
# Mendefinisikan Objek Sendiri

Antarmuka povray Euler berisi banyak objek. Tetapi Anda tidak dibatasi untuk ini. Anda dapat membuat objek sendiri, yang menggabungkan objek lain, atau merupakan objek yang sama sekali baru.

Kami mendemonstrasikan torus. Perintah Povray untuk ini adalah "torus". Jadi kami mengembalikan string dengan perintah ini dan
parameternya. Perhatikan bahwa torus selalu berpusat pada asalnya.
 
\>function povdonat (r1,r2,look="") ...

      return "torus {"+r1+","+r2+look+"}";
    endfunction
</pre>
Here is our first torus.

\>t1=povdonat(0.8,0.2)

    torus {0.8,0.2}

Mari kita gunakan objek ini untuk membuat torus kedua, diterjemahkan dan diputar.

\>t2=povobject(t1,rotate=xrotate(90°),translate=[0.8,0,0])
 
    object { torus {0.8,0.2}
     rotate 90 *x 
     translate &lt;0.8,0,0&gt;
     }

Sekarang kami menempatkan objek ini ke dalam sebuah adegan. Untuk tampilan, kami menggunakan Phong Shading.

\>povstart(center=[0.4,0,0],angle=0°,zoom=3.8,aspect=1.5); ...  
\>   writeln(povobject(t1,povlook(green,phong=1))); ...  
\>   writeln(povobject(t2,povlook(green,phong=1))); ...  
\>   &gt; povend ();

memanggil program Povray. Namun, jika terjadi kesalahan, itu tidak menampilkan kesalahan. Karena itu Anda harus menggunakan

 &gt; povend (&lt;exit);  

jika ada yang tidak berhasil. Ini akan membuat jendela Povray terbuka.

\>povend (h=320,w=480);

    Command was not allowed!
    exec:
        return _exec(program,param,dir,print,hidden,wait);
    povray:
        exec(program,params,defaulthome);
    Try "trace errors" to inspect local variables after errors.
    povend:
        povray(file,w,h,aspect,exit); 

Berikut adalah contoh yang lebih lengkap. Kami menyelesaikannya dan menunjukkan poin yang layak dan optimal dalam plot 3D.

\>A=[10,8,4;5,6,8;6,3,2;9,5,6];

\>b=[10,10,10,10]';

\>c=[1,1,1];

Pertama, mari kita periksa, apakah contoh ini memiliki solusi.

\>x=simplex(A,b,c,\>max,\>check)'

    [0,  1,  0.5]
Yes, it has.

Next we define two objects. The first is the plane

\>function oneplane (a,b,look="") ...

      return povplane(a,b,look)
    endfunction
</pre>
Kemudian kami mendefinisikan perpotongan dari semua setengah spasi dan
sebuah kubus.

\>function adm (A, b, r, look="") ...

      ol=[];
      loop 1 to rows(A); ol=ol|oneplane(A[#],b[#]); end;
      ol=ol|povbox([0,0,0],[r,r,r]);
      return povintersection(ol,look);
    endfunction
</pre>
We can now plot the scene.

\>povstart(angle=120°,center=[0.5,0.5,0.5],zoom=3.5); ...  
\>   writeln(adm(A,b,2,povlook(green,0.4))); ...  
\>   writeAxes(0,1.3,0,1.6,0,1.5); ...  
\>  The following is a circle around the optimum.

--Terjemahan

Berikut ini adalah lingkaran di sekitar optimal.

\>writeln(povintersection([povsphere(x,0.5),povplane(c,c.x')], ...  
\>     povlook(red,0.9)));

Dan ada kesalahan di arah optimal.

\>writeln(povarrow(x,c\*0.5,povlook(red)));

Kami menambahkan teks ke layar. Teks hanyalah objek 3D. Kita perlu menempatkan dan memutarnya sesuai dengan pandangan kita.

\>writeln(povtext("Linear Problem",[0,0.2,1.3],size=0.05,rotate=125°)); ...  
\>   povend();

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-075.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-075.png)
# Latihan Soal

1. Buatkan grafik$$f(x,y)=2^x+3y$$\>function f(x,y):= 2^x+3\*y 

\>plot3d("f"):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-077.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-077.png)

2. Buatkan grafik

$$f(x)=x^3-3x+4$

dengan a=-2, b=2, dan grid=18

\>plot3d("x^3-3\*x+4",a=-2,b=2,rotate=true,grid=18):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-079.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-079.png)

3. Buatlah grafik plot kontur$$f(x)=e^{3xy}$$\>plot3d("exp(3\*x\*y)",angle=150°,\>contour,color=yellow):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-081.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-081.png)
4. Buat grafik plot implisit

$$x^2+y^2+5xz+3z^3$$\>plot3d("x^2+y^2+5\*x\*z+3\*z^3",\>implicit,r=2,zoom=2.2):

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-083.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-083.png)

5. Buatlah plot 3D dari fungsi
$$f(x,y)=x^3+y^2$$

dengan zoom 3 dan angle 55 derajat menggunakan povray

\>pov3d("x^3+y^2",zoom=3,angle=55°);

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-085.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-085.png)

6. Buatlah gabungan 2 silinder dengan fungsi povx() berwarna merah dan
povz() berwarna kuning dan zoom 4

\>povstart(zoom=4)

\>c1 = povcylinder(-povx,povx,1,povlook(red));

\>c2 = povcylinder(-povz,povz,1,povlook(yellow));

\>writeln(povintersection([c1,c2]));

\>povend();

![images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-086.png](images/Alya%20Putri%20Medilasari_23030630018_EMTPlot3D-086.png)



