## Tutorial 8 - Subscriber

#### Commit 1 Reflection
#### 1. What is AMQP?
AMQP, singkatan dari Advanced Message Queuing Protocol, adalah open standard application layer protocol yang berfokus pada message-oriented middleware. AMQP bekerja sebagai protokol jaringan yang memfasilitasi pertukaran data pada sistem yang terpisah. Komunikasi yang terjadi antara aplikasi client (penerima data) dan aplikasi sumber (pengirim data) ini akan melibatkan penggunaan messaging middleware.

#### 2. What it means? guest:guest@localhost:5672, what is the first guest, and what is the second guest, and what is localhost:5672 is for?
String guest:guest@localhost:5672 merupakan string koneksi untuk server AMQP. Dalam kasus ini, guest pertama merupakan username dan guest kedua merupakan password yang diperlukan untuk melakukan autentikasi ke server. Kemudian, localhost merupakan hostname dari server karena server tersebut berjalan pada mesin yang sama dengan client. Terakhir, 5672 adalah nomor port default yang digunakan untuk komunikasi dengan AMQP.

#### Commit 2 Screen Capture and Reflection
Simulation Slow Subscriber Screen Capture
![Simulation Slow Subscriber Screen Capture](/images/simulation_slow_subscriber.png)

Berdasarkan lampiran di atas, dapat dilihat bahwa jumlah message terbanyak yang ada di message queue saya adalah 30. Hal ini bisa terjadi karena program subscriber memerlukan waktu yang lebih lama untuk me-handle message namun program publisher terus-menerus mengirimkan message setelah di-run berulang kali. Alhasil, terjadi "penumpukan" message di message queue.