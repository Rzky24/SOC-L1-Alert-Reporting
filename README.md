# SOC-L1-Alert-Reporting

Selama atau setelah triase peringatan, analis L1 mungkin tidak yakin tentang cara mengklasifikasikan peringatan tersebut, sehingga memerlukan dukungan senior atau informasi dari pemilik sistem. Selain itu, L1 mungkin berurusan dengan serangan siber dan pelanggaran nyata yang membutuhkan perhatian segera dan tindakan perbaikan. Ruangan ini membahas kasus-kasus ini dengan memperkenalkan tiga istilah baru: pelaporan peringatan, eskalasi, dan komunikasi.

Tujuan pembelajaran
Memahami kebutuhan pelaporan dan eskalasi peringatan SOC.
Pelajari cara menulis komentar peringatan atau laporan kasus dengan benar.
Jelajahi metode eskalasi dan praktik terbaik komunikasi.
Terapkan pengetahuan tersebut untuk melakukan triase peringatan dalam lingkungan simulasi.

Dasbor SOC
Lanjutkan perjalanan Anda di dasbor SOC ! Kali ini Anda akan membutuhkannya untuk menulis laporan profesional dan berlatih dalam meningkatkan eskalasi peringatan. Buka situs web terlampir di jendela terpisah dengan mengklik tautan dasbor SOC di bawah ini dan lanjutkan ke tugas berikutnya!

Alert Funnel
Anda telah mempelajari cara mengklasifikasikan dan memprioritaskan peringatan. Namun, Anda mungkin penasaran tentang apa yang terjadi selanjutnya. Bagaimana prioritas peringatan Anda membantu mencegah ancaman dan menghentikan pelanggaran? Ini adalah topik baru yang akan dibahas di ruangan ini segera, tetapi untuk saat ini, mari kita ingat kembali alur peringatan tersebut.<img width="1175" height="539" alt="image" src="https://github.com/user-attachments/assets/444dac09-c2c8-41d9-a8aa-96f6feed7307" />


Pertama, analis L1 menerima peringatan di SIEM , EDR , atau platform manajemen tiket. Sebagian besar peringatan ditutup sebagai False Positive atau ditangani di tingkat L1, tetapi peringatan yang kompleks dan mengancam dikirim ke L2 yang menangani sebagian besar pelanggaran. Dan untuk mengirim peringatan lebih lanjut, Anda perlu mempelajari tiga istilah baru: pelaporan, eskalasi, dan komunikasi.

Pelaporan Peringatan
Sebelum menutup atau meneruskan peringatan ke L2, Anda mungkin perlu melaporkannya. Tergantung pada standar tim dan tingkat keparahan peringatan, alih-alih komentar peringatan singkat, Anda mungkin diminta untuk mendokumentasikan investigasi Anda secara detail, memastikan semua bukti yang relevan disertakan. Ini sangat penting untuk True Positive, yang memerlukan eskalasi.

Peningkatan Peringatan
Jika peringatan True Positive memerlukan tindakan tambahan atau investigasi lebih mendalam, eskalasikan ke analis L2 untuk peninjauan lebih lanjut sesuai prosedur yang disepakati. Di sinilah laporan peringatan Anda akan berguna karena L2 akan menggunakannya untuk mendapatkan konteks awal dan mengurangi biaya analisis dari awal.

Komunikasi
Anda mungkin juga perlu berkomunikasi dengan departemen lain selama atau setelah analisis. Misalnya, tanyakan kepada tim TI apakah mereka telah mengkonfirmasi pemberian hak akses administratif kepada beberapa pengguna atau hubungi bagian SDM untuk mendapatkan informasi lebih lanjut tentang karyawan yang baru direkrut.

Bagaimana proses meneruskan peringatan mencurigakan ke analis L2 untuk ditinjau? Alert Escalation
Bagaimana proses mendeskripsikan detail dan temuan peringatan secara formal? Alert Reporting

Panduan Pelaporan
Sebelum kita melanjutkan, penting untuk mengklarifikasi mengapa seseorang menginginkan analis L1 untuk menulis laporan selain menandainya sebagai Positif Benar atau Positif Salah, dan mengapa topik ini tidak boleh diremehkan. Meminta analis L1 untuk menulis laporan peringatan memiliki beberapa tujuan utama:

Tujuan Laporan Peringatan	Penjelasan
Berikan konteks untuk eskalasi.	
Laporan yang ditulis dengan baik menghemat banyak waktu bagi analis L2.
Selain itu, hal ini membantu mereka memahami dengan cepat apa yang terjadi.
Simpan temuan untuk arsip.	
Log SIEM mentah disimpan selama 3-12 bulan, tetapi peringatan disimpan tanpa batas waktu.
Oleh karena itu, lebih baik menyimpan semua konteks di dalam peringatan, untuk berjaga-jaga.
Meningkatkan keterampilan investigasi	
Jika Anda tidak bisa menjelaskannya dengan sederhana, berarti Anda belum cukup memahaminya.
Menulis laporan adalah cara yang bagus untuk meningkatkan kemampuan bahasa ibu (L1) dengan meringkas peringatan.
Format Laporan
Contoh laporan terstruktur yang baik mengikuti pendekatan 5W.

Bayangkan diri Anda sebagai analis L2, anggota tim DFIR , atau profesional TI yang perlu memahami peringatan tersebut. Apa yang ingin Anda lihat dalam laporan? Kami menyarankan Anda mengikuti  pendekatan Lima W dan menyertakan setidaknya item-item berikut dalam laporan:

Siapa : Pengguna mana yang masuk, menjalankan perintah, atau mengunduh file
Apa : Tindakan atau urutan kejadian persis apa yang dilakukan?
Kapan : Kapan tepatnya aktivitas mencurigakan tersebut dimulai dan berakhir?
Di mana : Perangkat, IP, atau situs web mana yang terlibat dalam peringatan tersebut
Mengapa : W yang paling penting, alasan di balik keputusan akhir Anda.

Berdasarkan dasbor SOC , email pengguna mana yang membocorkan dokumen sensitif tersebut? m.boslan@tryhackme.thm
Berdasarkan peringatan terbaru, siapakah "pengirim" email mencurigakan yang kemungkinan besar merupakan email phishing tersebut? support@microsoft.com
Buka peringatan phishing, baca detailnya, dan coba pahami aktivitas tersebut.
Dengan menggunakan templat Lima W, bendera apa yang Anda terima setelah menulis laporan yang baik? THM{nice_attempt_faking_microsoft_support}

Panduan Eskalasi
Setelah Anda membuat keputusan dan menulis laporan peringatan, Anda harus memilih apakah akan meningkatkan peringatan tersebut ke L2. Sekali lagi, jawabannya mungkin berbeda dari tim ke tim, tetapi rekomendasi berikut umumnya cocok untuk sebagian besar tim SOC . Anda harus meningkatkan peringatan jika:

Peringatan ini merupakan indikator serangan siber besar yang memerlukan investigasi lebih mendalam atau DFIR ( Dependency and Functional Information Response).
Tindakan perbaikan seperti penghapusan malware, isolasi host, atau pengaturan ulang kata sandi diperlukan.
Komunikasi dengan pelanggan, mitra, manajemen, atau lembaga penegak hukum diperlukan.
Anda belum sepenuhnya memahami peringatan tersebut dan membutuhkan bantuan dari analis yang lebih senior.
Langkah-langkah Eskalasi
Untuk meningkatkan penanganan peringatan, dalam kebanyakan kasus, yang perlu Anda lakukan hanyalah menetapkan ulang peringatan tersebut kepada L2 yang sedang bertugas dan menghubungi mereka melalui obrolan perusahaan atau secara langsung. Namun, di beberapa tim, Anda mungkin diharuskan untuk membuat permintaan peningkatan penanganan peringatan secara tertulis dengan puluhan kolom yang wajib diisi.https://tryhackme-images.s3.amazonaws.com/user-uploads/678ecc92c80aa206339f0f23/room-content/678ecc92c80aa206339f0f23-1743520297119.svg

Apa pun kesepakatannya, L2 pada akhirnya akan menerima tiket dari Anda, membaca laporan Anda, dan menghubungi Anda jika ada pertanyaan. Setelah semuanya jelas, analis L2 biasanya akan meneliti detail peringatan lebih lanjut, memvalidasi apakah peringatan tersebut memang True Positive, berkomunikasi dengan departemen lain jika diperlukan, dan, untuk insiden besar, memulai proses Tanggap Insiden formal.

Meminta Dukungan L2
Pada umumnya tidak masalah bagi L1 untuk meminta bantuan senior jika ada sesuatu yang tidak jelas. Terutama di bulan-bulan pertama Anda, selalu lebih baik untuk mendiskusikan peringatan dan mengklarifikasi prosedur SOC daripada menutup peringatan yang tidak Anda pahami sendiri secara membabi buta. Prosedur untuk meminta bantuan mungkin berbeda, tetapi alurnya umumnya seperti ini:https://tryhackme-images.s3.amazonaws.com/user-uploads/678ecc92c80aa206339f0f23/room-content/678ecc92c80aa206339f0f23-1743520519371.svg

Eskalasi Dasbor SOC
Tulis laporan peringatan dan berikan penilaian Anda; pindahkan peringatan ke status Sedang Diproses.
Tetapkan tugas peringatan ini kepada L2 yang sedang bertugas. L2 akan menerima pemberitahuan dan mulai bertugas berdasarkan laporan Anda.

Siapakah L2 Anda saat ini di dasbor SOC yang dapat Anda beri tugas (eskalasi) untuk menangani peringatan tersebut? E.Fleming

Komunikasi SOC
Topik eskalasi dan pelaporan seharusnya terdengar mudah dan logis bagi Anda. Namun, seperti biasa, lebih mudah diucapkan daripada dilakukan, dan Anda harus siap menghadapi skenario yang tidak terduga dan mengetahui apa yang harus dilakukan dalam kasus-kasus kritis. Dalam skenario terbaik, tim SOC memiliki prosedur Komunikasi Krisis sendiri - panduan dan proses untuk membantu Anda dan rekan tim Anda menyelesaikan masalah. Jika tidak, Anda disarankan untuk membaca kasus-kasus di bawah ini dan bersiap untuk menanganinya secara efektif.

Kasus Komunikasi
Anda perlu meningkatkan penanganan peringatan mendesak dan kritis, tetapi L2 tidak tersedia dan tidak merespons selama 30 menit.
Pastikan Anda mengetahui di mana menemukan kontak darurat. Pertama, coba hubungi L2, lalu L3, dan terakhir manajer Anda.

Peringatan tentang peretasan akun Slack/Teams mengharuskan Anda untuk memvalidasi login dengan pengguna yang terpengaruh.
Jangan menghubungi pengguna melalui obrolan yang diretas - gunakan metode kontak alternatif seperti panggilan telepon.

Anda menerima sejumlah besar peringatan dalam waktu singkat, beberapa di antaranya sangat penting.
Prioritaskan peringatan sesuai dengan alur kerja, tetapi beri tahu L2 Anda yang sedang bertugas tentang situasi tersebut.

Setelah beberapa hari, Anda menyadari bahwa Anda salah mengklasifikasikan peringatan tersebut dan kemungkinan besar melewatkan tindakan berbahaya.
Segera hubungi L2 Anda dan jelaskan kekhawatiran Anda. Pelaku ancaman dapat berdiam diri selama berminggu-minggu sebelum menimbulkan dampak.

Anda tidak dapat menyelesaikan triase peringatan karena log SIEM tidak diuraikan dengan benar atau tidak dapat dicari.
Jangan abaikan peringatan ini - selidiki apa yang bisa Anda selidiki dan laporkan masalah ini kepada L2 yang bertugas atau teknisi SOC Anda .

Kesimpulan
Kerja bagus telah mempelajari tiga keterampilan SOC penting : pelaporan peringatan, eskalasi, dan komunikasi. Keterampilan ini sangat penting bagi setiap analis L1: Pelaporan peringatan membantu melestarikan dan memberikan konteks aktivitas untuk L2, eskalasi memastikan ancaman ditangani tepat waktu, dan komunikasi membuat koordinasi antara SOC dan departemen lain menjadi jelas dan efektif.
