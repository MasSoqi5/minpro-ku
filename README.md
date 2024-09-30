![flowchart minpro](https://github.com/user-attachments/assets/91018ebe-204a-437e-998f-7f80a856b0cf)
# Terminal
![Screenshot 2024-09-30 223738](https://github.com/user-attachments/assets/ce2af43d-dc52-4b43-bc8c-f954c86f8a91)
# Penjelasan
#Langkah 1 LOGIN
- muncul pertanyaan nama dan nim
- JIka nama dan nim benar dilanjutkan ke perhitungan
- Jika salah ada pertanyaan mau dilanjutkan atau tidak==> jika n keluar aplikasi
- ==> jika y muncul pertanyaan nama dan nim.
#Langkah 2 PERHITUNGAN
- muncul pertanyaan jumlah dan harga barang
- JIka perkaian jumlah dan harga barang > 250000 dilakuikan diskon, jika tidak, harga tetap
- Akan muncul pertanyaan "Ingin menghitung ulang? jika y akan muncul pertanyaan harga dan barang, jika tidak selesai

# minproku
masuk = 'y'
while masuk == 'y':
    namabenar = "Syauqi Etna"
    nimbenar = "2409116030"
    
    nama = input("Masukkan Namamu: ")
    nim = input("Masukkan NIM: ")
    
    # Perbaikan dengan menggunakan 'or' untuk pengecekan
    if nama != namabenar or nim != nimbenar:
        print("Nama atau NIM salah, coba lagi.")
        masuk = input("Apakah Anda ingin mencoba lagi? (y/n): ").lower()
        if masuk =='n' :
            quit()
    else:
        print(f"Selamat datang, {nama}!")
        masuk = 'n'  # Menghentikan loop jika login berhasil

# Menanyakan apakah ingin menghitung ulang
ulang = 'y'  # Inisialisasi variabel ulang
while ulang == 'y':
    # Mengambil input
    harga_brg = float(input("Harga barang: "))  # Mengonversi input ke float
    jum_brg = int(input("Jumlah Barang: "))      # Mengonversi input ke int

    # Menghitung total harga
    tot_brg = harga_brg * jum_brg

    # Mengecek kondisi untuk diskon
    if tot_brg > 250000:
            diskon = tot_brg * 0.25  # Menghitung diskon 25%
            tot_brg -= diskon         # Mengurangi total dengan diskon

    # Menampilkan output
    print("Total harga :", tot_brg)

    # Menanyakan apakah ingin menghitung ulang
    ulang = input("Ingin menghitung ulang? (y/t): ").lower()


