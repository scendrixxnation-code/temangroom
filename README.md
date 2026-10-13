# TemanGroom

**Teman pengantin, tenang sepanjang majlis.**

Prototaip frontend Bahasa Melayu untuk mencari dan menghantar permintaan demo kepada pembantu pengantin lelaki di Malaysia. Semua profil, pengalaman, harga, review dan slot ialah contoh rekaan.

## Buka laman

Buka `index.html` dengan Chrome, Edge, Firefox atau Safari moden. Fail ini berdiri sendiri: CSS, JavaScript, fon Poppins dan ilustrasi SVG telah dibenamkan. Tiada rangka kerja, pemasangan, build, video atau aset luar diperlukan. Sambungan Internet tidak diperlukan untuk penggunaan laman.

Jika pelayar mengehadkan storan fail setempat, jalankan pelayan statik dalam folder ini, contohnya:

```sh
python3 -m http.server 8080 --bind 127.0.0.1
```

Kemudian buka `http://127.0.0.1:8080`. Hentikan pelayan dengan Ctrl+C. Tiada backend aplikasi diperlukan.

## Cuba dashboard dan dua acara berlainan tarikh

1. Tekan **Log Masuk**, pilih **Pengantin**, kemudian **Isi Akaun Contoh → Log Masuk Demo**. Dashboard halaman penuh akan dibuka.
2. Buka **Majlis Saya**. Tekan **Isi Contoh Nikah & Sanding** untuk dua acara rekaan pada tarikh 14 dan 16 hari selepas tarikh Malaysia semasa halaman dibuka, atau tambah acara sendiri.
3. Pada kad **Nikah**, tekan **Cari Assistant**. Carian menggunakan tarikh, waktu, kawasan dan bajet acara itu. Pilih profil Amir, kemudian pakej Nikah.
4. Borang tempahan memaparkan acara dan perkahwinan yang dipautkan. Nama, telefon, venue dan nota diisi daripada profil/acara. Venue dikunci kepada acara supaya rekod konsisten. Semak bil, tandakan persetujuan dan hantar permintaan demo.
5. Kembali ke **Majlis Saya**, lalu cari assistant pada kad **Sanding**. Pilih assistant dan pakej Sanding. Ia boleh assistant sama atau berbeza, tertakluk slot. Dua tempahan mempunyai bil, deposit, baki dan status berasingan.
6. Tukar ke akaun Assistant yang berkaitan. Desktop menyediakan **Tukar Akaun Demo** pada menu sisi. Pada telefon, tekan **Log keluar** pada bahagian atas dashboard, kemudian buka menu marketplace dan **Log Masuk** untuk peranan lain. Akaun Amir ialah `assistant@temangroom.demo`; akaun Faris ialah `faris@temangroom.demo`.
7. Assistant membuka **Permintaan Masuk** dan menerima permintaan. Pengantin menghantar deposit demo. Assistant menyemak deposit dan menandakan job selesai. Kawalan yang tidak sesuai dengan peranan disembunyikan dan ditolak oleh logik demo.
8. Selepas selesai, Pengantin boleh menulis satu review. Assistant melihatnya dalam **Rekod Job & Review**.
9. Cuba **Jadual Saya → Tutup Slot Sendiri** pada akaun Assistant. Slot ini mempengaruhi padanan servis contoh miliknya, termasuk penampan perjalanan 60 minit. Slot sendiri boleh dibuka semula.
10. Untuk memadam semua data prototaip, kembali ke marketplace dan gunakan **Reset Data Demo** di footer. Tempahan, acara, review tambahan, borang minat, akaun baharu, draf pakej dan slot sendiri dipadam; tujuh akaun contoh dipulihkan.

Carian tanpa login masih tersedia. **Cuba Carian Demo** mengisi carian nikah dengan tiga padanan awal. Jika memilih pakej daripada carian bebas, login Pengantin diperlukan dan pengguna diminta memilih acara sepadan atau menambah acara sebelum meneruskan tempahan.

## Login demo Pengantin dan Assistant

Gunakan butang **Log Masuk** dalam navigasi (dalam menu pada telefon). Pilih peranan, isi e-mel dan kata laluan, atau tekan **Isi Akaun Contoh**. Tunjuk/sembunyi kata laluan, daftar akaun dan panduan lupa kata laluan tersedia.

| Peranan | E-mel contoh | Kata laluan |
| --- | --- | --- |
| Pengantin | `pengantin@temangroom.demo` | `Demo123!` |
| Assistant — Amir | `assistant@temangroom.demo` | `Demo123!` |
| Assistant — Faris | `faris@temangroom.demo` | `Demo123!` |
| Assistant — Haziq | `haziq@temangroom.demo` | `Demo123!` |
| Assistant — Danish | `danish@temangroom.demo` | `Demo123!` |
| Assistant — Syafiq | `syafiq@temangroom.demo` | `Demo123!` |
| Assistant — Irfan | `irfan@temangroom.demo` | `Demo123!` |

Pendaftaran Pengantin memerlukan nama, telefon, e-mel dan persetujuan demo. Assistant turut memilih kawasan servis. Kata laluan pendaftaran ialah contoh tetap, bukan kata laluan peribadi yang dipilih pengguna. E-mel yang sama tidak boleh didaftarkan dua kali untuk peranan sama. Peranan dipilih secara jelas semasa login.

Selepas login, pengguna masuk ke dashboard halaman penuh. Navigasi marketplace turut menyediakan **Akaun Saya** atau **Ruang Assistant** untuk kembali ke dashboard. Jalur sesi di bahagian carian menunjukkan nama, peranan dan log keluar. Sesi demo dikekalkan selepas muat semula jika storan tersedia.

- Pengantin boleh mengemas kini nama/telefon, mencari servis, menghantar permintaan, melihat tempahan sendiri, menghantar deposit demo, membatalkan dan menulis satu review selepas selesai.
- Assistant contoh melihat permintaan bagi profil servis yang dipadankan kepadanya sahaja. Assistant boleh menerima/menolak, menyemak deposit demo, melengkapkan job dan melihat pakej serta slot contoh.
- Akaun Assistant baharu mempunyai draf profil sendiri (nama, telefon, kawasan, bio dan URL portfolio). Draf ini tidak diterbitkan ke marketplace dan tidak memiliki profil assistant contoh orang lain. Pakej boleh disimpan sebagai draf dan slot sendiri boleh dicatat secara peribadi. Penerbitan servis baharu ke marketplace belum tersedia.
- Perubahan profil Assistant contoh juga draf akaun; profil marketplace rekaan asal dikekalkan.
- Tempahan lama daripada versi sebelum login dipadankan kepada Pengantin Demo sahaja sebagai migrasi data contoh setempat.
- **Lupa kata laluan?** menyediakan panduan demo dan kembali ke login dengan e-mel diisi. Tiada e-mel reset dihantar atau proses reset sebenar dilakukan.

Penapisan akaun dan peranan dibuat pada frontend sahaja. Sesi boleh diubah melalui alat pelayar dan semua data berada pada storan sama. Ini bukan pemisahan data yang selamat atau autentikasi produksi. Login sebenar memerlukan backend, pengesahan e-mel, pengurusan sesi serta kawalan akses pelayan. Gunakan maklumat rekaan sahaja.

## Ruang selepas login

**Pengantin:** Dashboard, Majlis Saya, Tempahan Saya, Profil Saya dan pautan Cari Assistant. Dashboard menunjukkan acara akan datang yang belum selesai, ringkasan status dan tindakan seterusnya. Acara Nikah/Sanding menyimpan nama, tarikh, masa, kawasan, venue, bajet dan nota sendiri.

**Assistant:** Dashboard, Permintaan Masuk, Jadual Saya, Profil & Portfolio, Pakej Saya serta Rekod Job & Review. Dashboard menunjukkan permintaan baharu dan job seterusnya. Kalendar bulanan boleh ditukar, tarikh boleh dipilih dan slot sendiri boleh ditutup/dibuka semula.

Peraturan tambahan:

- Setiap akaun Pengantin mempunyai satu rekod perkahwinan dengan beberapa acara; nama perkahwinan boleh diubah.
- Acara bertindih waktunya dalam perkahwinan sama ditolak. Acara hari sama yang tidak bertindih dibenarkan. Penampan perjalanan assistant dinilai berasingan semasa carian.
- Nikah dan sanding berbeza tarikh menggunakan dua acara dan dua tempahan. Pakej gabungan hanya untuk **hari sama**.
- Satu acara hanya boleh mempunyai satu permintaan/tempahan aktif atau satu job selesai. Batalkan permintaan sebelum memilih assistant lain. Rekod ditolak, dibatalkan atau tamat pegangan tidak menghalang tempahan baharu.
- Setiap tempahan menyimpan ID perkahwinan, ID acara dan salinan tajuk/jenis acara. Tarikh, waktu, harga, deposit, baki dan status kekal pada tempahan masing-masing.
- Acara dengan permintaan aktif atau job selesai dikunci daripada ubah/padam untuk menjaga rekod. Acara kosong boleh diubah dan dipadam selepas pengesahan. Tempahan yang telah dibatalkan kekal dalam sejarah.
- Harga draf pakej dan profil draf tidak mengubah penyenaraian contoh atau bil tempahan lama. Ia belum diterbitkan. Ini dinyatakan pada borang draf.
- Slot sendiri Assistant contoh menyekat carian setempat bagi profilnya sahaja. Sekatan tidak boleh bertindih dengan job diterima/disahkan atau sekatan lain, termasuk penampan 60 minit. Slot akaun baharu kekal peribadi kerana servis belum diterbitkan.
- Permintaan yang belum diterima tidak menyekat kalendar. Pegangan tamat melepaskan slot; permintaan diterima, deposit menunggu semakan dan job disahkan dipaparkan dalam jadual.
- Tempahan versi lama tanpa pautan acara masih boleh dilihat sebagai **Tempahan terdahulu — belum dipautkan**. Ia tidak dibuang atau dicampur secara automatik dengan acara baharu.
- Pautan halaman dalaman `#app/overview`, `#app/events`, `#app/bookings`, `#app/schedule`, `#app/profile`, `#app/packages` dan `#app/history` menyokong muat semula serta butang kembali pelayar. Pilihan bergantung pada peranan.

## Peraturan demo

- Tarikh dan tahun menggunakan `Asia/Kuala_Lumpur`; mata wang RM. Tarikh lampau dan waktu mula yang sudah berlalu pada hari ini ditolak.
- Setiap acara mesti bermula dan tamat pada hari yang sama. Satu perkahwinan boleh mempunyai banyak acara pada tarikh berbeza; nikah dan sanding bukan satu sesi panjang merentas hari. Sesi merentas tengah malam tidak disokong.
- Padanan menggunakan kawasan servis, jenis majlis, tempoh pakej, bajet dan pertindihan slot. Pakej ialah 4 jam nikah, 5 jam sanding atau 8 jam gabungan.
- Penampan perjalanan ialah 60 minit sebelum/selepas slot. Slot seterusnya boleh bermula tepat 60 minit selepas slot terdahulu tamat.
- Data slot asal menyekat satu sesi setiap assistant pada tarikh demo atau sehari selepasnya. Waktu sekatan boleh dilihat dalam profil.
- Permintaan awal tidak menyekat slot. Selepas penerimaan simulasi, pegangan sementara selama 15 minit menyekat assistant yang sama. Permintaan bertindih tidak boleh diterima atau disahkan.
- Pegangan tamat diperiksa pada muatan halaman, kembali ke tab, tindakan carian/tempahan dan setiap 10 saat. Tab yang digantung pelayar akan disemak apabila kembali aktif.
- Deposit ilustrasi 30%, baki 70%. Status bayaran disimpan berasingan daripada status tempahan. Tiada pembayaran sebenar atau muat naik bukti diperlukan.
- Pakej tidak termasuk solekan, dandanan rambut atau styling profesional. Caj lebih masa contoh RM 60/jam memerlukan persetujuan dan tidak ditambah secara automatik.
- Terma pembatalan contoh dipaparkan sebelum permintaan: sebelum pengesahan tiada caj; selepas pengesahan deposit ilustrasi tidak dipulangkan, baki tidak dikenakan. Tiada jaminan pengganti.

## Data dan batasan

Tiada backend, akaun sebenar, pengesahan identiti, pembayaran, penghantaran mesej, admin langsung atau kalendar bersama. Login yang disediakan ialah simulasi akaun dalam pelayar sahaja dan bukan perlindungan data. Borang minat assistant hanya disimpan setempat dan berasingan daripada pendaftaran akaun demo; kedua-duanya tidak menerbitkan profil sebenar.

Data tempahan menggunakan kunci localStorage `temangroom-demo-v1`. Acara perkahwinan, slot sendiri dan draf pakej menggunakan `temangroom-workspace-v1`. Akaun dan sesi demo menggunakan `temangroom-accounts-v1`. Tiada kata laluan pengguna atau hash kata laluan disimpan; semua akaun menggunakan kata laluan contoh tetap `Demo123!`. Gunakan butiran rekaan kerana sesiapa yang menggunakan profil pelayar sama boleh membaca data itu. Storan boleh berbeza antara pelayar, profil, alamat pelayan dan lokasi fail. Memindahkan fail mungkin menghasilkan ruang storan baharu.

Data rosak akan diabaikan dengan notis. Jika storan tidak tersedia, halaman terus berfungsi menggunakan memori sementara dan memaparkan notis apabila menyimpan. Data itu hilang selepas muat semula. Tiada sinkronisasi atau penguncian merentas tab/peranti; gunakan satu tab untuk simulasi tempahan.

## Kebolehcapaian dan reka bentuk

Navigasi berlabel, pautan langkau, label borang, fokus jelas, mesej status, dialog dengan perangkap fokus serta Escape disediakan. Menu mudah alih menggunakan pautan navigasi yang sama dan ditutup melalui Escape, klik di luar, pilihan pautan atau perubahan ke desktop. Kandungan penerangan kekal tersedia jika JavaScript dimatikan; carian dan tempahan memerlukan JavaScript.

Cincin 3D mempunyai 37 kad, jejari dan perspektif 891px, pemisahan 360/37 darjah serta kelajuan 1.9 darjah/saat. Kad di luar 42 darjah disembunyikan. Animasi berhenti apabila hero di luar skrin atau tab tersembunyi. `prefers-reduced-motion` menghentikan gerakan cincin, animasi intro dan tatal lancar.

## Pengesahan yang dilakukan

Ujian automatik dijalankan dalam Chrome setempat dengan Playwright. Semakan visual dibuat pada hero desktop, halaman telefon dan dialog profil/tempahan. Lulus:

- Enam profil, 37 kad cincin; carian wajib, tarikh lampau, susunan masa, padanan diketahui, caj perjalanan, bajet dan tiada padanan.
- Susunan harga/rating, profil dan pecahan bil, pakej nikah serta gabungan 8 jam.
- Pengesahan borang, teks input dipaparkan secara selamat, permintaan pendua dan peralihan status tidak sah dihalang.
- Pertindihan penerimaan dan pengesahan dihalang; sempadan penampan 60 minit; penolakan, pembatalan dan tamat pegangan melepaskan slot.
- Muat semula mengekalkan tempahan/review; satu review selepas selesai; jumlah job/review dikemas kini; reset memulihkan statistik asal.
- URL borang minat, storan rosak dan storan tidak tersedia.
- Fokus dialog, Escape, pemulihan fokus, menu telefon serta reduced motion.
- Lebar 320, 375, 768, 1080 dan 1440px tanpa limpahan halaman mendatar. Dialog diuji pada 320px dan skrin pendek 720×400.
- Susun atur setara pembesaran 200% melalui viewport lebih kecil; ujian pembesaran CSS 200% turut dibuat. Ini bukan ujian pembesaran pada peranti fizikal.
- Tiada ralat JavaScript halaman dalam aliran yang diuji.

Ujian tambahan login (Chrome/Playwright) turut lulus: carian tetamu, sambungan tempahan selepas login, input kosong/salah, tunjuk kata laluan, pilihan peranan, pendaftaran kedua-dua peranan, e-mel pendua, profil draf, URL portfolio, pemaparan teks selamat, panduan lupa kata laluan, log keluar, sesi selepas reload, tempahan mengikut pemilik, halangan tindakan akaun/peranan lain, aliran dua pihak hingga review, reset akaun, data akaun rosak dan login tanpa storan. Dialog login disemak pada lima lebar skrin dan fokus papan kekunci; paparan login telefon serta ruang Assistant disemak secara visual.

Ujian dashboard tambahan (Chrome/Playwright) meliputi halaman penuh selepas login, dua acara berlainan tarikh, carian khusus acara, venue diisi automatik, dua assistant atau assistant sama pada hari berlainan, pautan perkahwinan sama dengan bil/status berasingan, muat semula, tindakan dua peranan hingga review, jadual job diterima, tutup/buka slot yang mengubah padanan, kunci acara ditempah, pengesahan acara kosong/lampau/bertindih, tambah/padam acara kosong, draf profil/pakej, pengasingan akaun, navigasi kembali, laluan persendirian tetamu, data ruang kerja rosak dan reset. Semua ruang utama kedua-dua peranan disemak pada 320, 375, 768, 1080 dan 1440px. Paparan dashboard desktop, kad acara dan kalendar telefon disemak secara visual.

Firefox, Safari, pembaca skrin dan peranti fizikal belum diuji. Tiada dakwaan kesiapan produksi atau jaminan slot sebenar dibuat.

## Kredit

Ilustrasi perkahwinan SVG dicipta khusus untuk prototaip ini. Fon Poppins dibenamkan daripada repositori Google Fonts dan diedarkan di bawah SIL Open Font License 1.1. Teks lesen penuh turut terkandung dalam komen awal `index.html`.
