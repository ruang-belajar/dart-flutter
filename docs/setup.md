# Persiapan Belajar

Berikut adalah setup dan persiapan yang perlu dilakukan untuk memulai belajar Flutter

## Download & Install Android Studio
- Install _Android SDK_
- Untuk panduan, check [Youtube: Dart & Flutter Installation (Erico Darmawan Handoyo)](https://youtu.be/asNdz10WR6w?si=ePXjDAwlqsD8POSw)

## Download & Install Visual Studio Code
- Install extension: _Flutter_ dan _Dart_
- Download & Install [Desktop development with C++](https://visualstudio.microsoft.com/downloads/#build-tools-for-visual-studio-2022)
- Untuk panduan, check [YouTube: Fix Flutter Doctor Visual Studio Not Installed - Please Install the Desktop Development With C++](https://www.youtube.com/watch?v=9Tux8qPK-mk)
  
## Download & Setup Flutter
- [Install Flutter](https://docs.flutter.dev/get-started/install)
- gunakan perintah `flutter doctor` untuk memeriksa kelengkapan instalasi
- Dalam kondisi jika kita hanya mau melakukan development aplikasi Windows saja, tanpa Android, kita bisa menonaktifkan pemeriksaan `flutter doctor` terhadap _Android SDK_ lewat perintah `flutter config --no-enable-android`

## Setup HP sebagai perangkat test aplikasi
- Masuk ke _Developer Mode_ di HP.
- Sambungkan HP ke PC menggunakan kabel USB.
- Set aktif mode _USB Debugging_ dan _Install via USB_. Pada saat Anda mengaktifkan opsi ini, pop-up pada layar HP akan muncul meminta ijin. Centang _Always Allow_ kemudian klik _OK_.
- Gunakan perintah `flutter devices` pada terminal untuk mengecek apakah perangkat sudah tersambung.
- Jika Anda melakukannya dengan benar, maka Anda akan menemukan nama model HP yang tersambung di pojok kanan bawah _VS Code_.
- Untuk bantuan, Anda bisa check [Youtube: Running App Flutter di Handphone Langsung via kabel USB](https://www.youtube.com/watch?v=f3p6fF79k0M)

## Setup _Flutter Version Management_
1. Install _fvm_
    ```
    dart pub global activate fvm
    ```
   Test `fvm`. Pada _CLI_/_Command Prompt_, jalankan `fvm --version`.\
   Jika instalasi berhasil, maka akan muncul informasi versi `fvm`.\
   Jika belum pesan _command not recognized_, tambahkan folder instalasi `fvm` ke _Windows Path_.
2. Install Flutter SDK
   1. Gunakan perintah `fvm releases` untuk melihat versi SDK yang tersedia.
   2. Install SDK di CLI menggunakan perintah `fvm install [version]`. Contoh: `fvm install 2.10.5`
   3. Aktifkan SDK di CLI menggunakan perintah `fvm use [version]`, lakukan di folder project
3. Setup VS Code
   1. Temukan _folder SDK Flutter_ lewat perintah `fvm list`
   2. Edit `setting.json` (`ctrl+shift+p`: _Preferences: Open User Settings (JSON)_)
   3. tambahkan _folder SDK Flutter_
      ```
      "dart.flutterSdkPaths": ["C:\\Users\\$USER\\fvm\\versions"]
      ```
   4. `ctrl+shift+p`: _Flutter: Change SDK_\
      Sampai titik ini, Anda seharusnya melihat versi SDK yang baru Anda install.\
      Jika tidak, rubah `$USER` pada langkah sebelumnya menjadi nama user windows.
4. Untuk bantuan cek [video tutorial](https://www.youtube.com/watch?v=7NS-RyJH9GM)

**Perintah _fvm_:**

| perintah | keterangan |
| --- | --- |
| `fvm list` | menampilkan versi SDK yang terinstall. SDK yang diinstall manual (tidak menggunakan _fvm_ tidak akan muncul di list) |
| `fvm install [version]` | install SDK `[version]` |
| `fvm use [version]` | mengaktifkan SDK `[version]` |
| `fvm releases` | menampilkan daftar _[version]_ yang tersedia |

