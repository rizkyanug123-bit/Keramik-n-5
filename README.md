def count_tile_ways(n): # Membuat fungsi bernama count_tile_ways yang menerima variabel n sebagai panjang lantai yang mau dihitung.
    # Basis 1: Jika N = 1, hanya ada 1 cara (1 keramik vertikal)
    if n == 1:
        return 1  # Kalau n bernilai 1, fungsi langsung berhenti dan ngasih angka 1 (cuma ada 1 cara, yaitu 1 keramik tegak).
    # Basis 2: Jika N = 2, ada 2 cara (2 vertikal atau 2 horizontal)
    if n == 2:
        return 2  # Kalau n bernilai 2, fungsi langsung berhenti dan ngasih angka 2 (bisa 2 keramik vertikal atau 2 keramik horizontal).

    # Langkah Rekursif
    return count_tile_ways(n - 1) + count_tile_ways(n - 2)
    # Jika n lebih besar dari 2, fungsi bakal memanggil dirinya sendiri 2 kali: untuk sisa lantai n - 1 ditambah sisa lantai n - 2, lalu menjumlahkan kedua hasilnya.

# Program Utama
n = 5
jumlah_cara = count_tile_ways(n)
# Memanggil fungsi count_tile_ways(5) untuk dihitung, lalu menyimpan hasil akhirnya ke dalam variabel jumlah_cara.

print(f"Banyak cara memasang keramik untuk N = {n} adalah: {jumlah_cara}")
# Menampilkan kalimat hasil ke layar dengan mengambil isi dari variabel n (5) dan jumlah_cara (8).
