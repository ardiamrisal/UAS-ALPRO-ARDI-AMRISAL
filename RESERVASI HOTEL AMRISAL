class Hotel:
    def __init__(self):
        self.kamar = {
            'Single': {'harga': 300000, 'tersedia': 5},
            'Double': {'harga': 500000, 'tersedia': 3},
            'Suite': {'harga': 1000000, 'tersedia': 2}
        }

    def tampilkan_kamar(self):
        print("\nDaftar Kamar:")
        for tipe, info in self.kamar.items():
            print(f"- {tipe}: Rp{info['harga']} (Tersedia: {info['tersedia']} kamar)")

    def reservasi(self, tipe_kamar, jumlah):
        if tipe_kamar in self.kamar:
            if self.kamar[tipe_kamar]['tersedia'] >= jumlah:
                total_harga = self.kamar[tipe_kamar]['harga'] * jumlah
                self.kamar[tipe_kamar]['tersedia'] -= jumlah
                print(f"\nReservasi berhasil! Anda memesan {jumlah} kamar {tipe_kamar}.")
                print(f"Total harga: Rp{total_harga}")
            else:
                print(f"\nMaaf, kamar {tipe_kamar} hanya tersedia {self.kamar[tipe_kamar]['tersedia']} kamar.")
        else:
            print("\nTipe kamar tidak ditemukan.")

    def jalankan(self):
        print("Selamat datang di Sistem Reservasi Hotel\n")
        while True:
            print("Menu:")
            print("1. Tampilkan Daftar Kamar")
            print("2. Reservasi Kamar")
            print("3. Keluar")
            pilihan = input("Pilih menu (1/2/3): ")

            if pilihan == '1':
                self.tampilkan_kamar()
            elif pilihan == '2':
                tipe_kamar = input("Masukkan tipe kamar (Single/Double/Suite): ")
                try:
                    jumlah = int(input("Masukkan jumlah kamar: "))
                    self.reservasi(tipe_kamar, jumlah)
                except ValueError:
                    print("\nJumlah kamar harus berupa angka.")
            elif pilihan == '3':
                print("\nTerima kasih telah menggunakan sistem reservasi hotel.")
                break
            else:
                print("\nPilihan tidak valid, silakan coba lagi.")

if __name__ == "__main__":
    hotel = Hotel()
    hotel.jalankan()
