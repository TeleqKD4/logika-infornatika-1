CODINGAN
```
def hitung_biaya_pengiriman(berat, jarak, layanan_express, member):
    biaya = 10000

    if berat > 5:
        biaya += 5000
    if jarak > 10:
        biaya += 8000
    if layanan_express:
        biaya += 20000
    if member:
        biaya -= biaya * 0.10  
    
    return biaya

def tampilkan_rincian_biaya(berat, jarak, layanan_express, member, biaya):
    nama_pelayan = "VIto Alviano Dwi Santoso"
    nim_pelayan = "312410070"  
    
    print("=" * 50)
    print("RINCIAN BIAYA PENGIRIMAN".center(50))
    print("=" * 50)

    print(f"{'Nama Pelayan':<25}: {nama_pelayan}")
    print(f"{'NIM Pelayan':<25}: {nim_pelayan}")
    print("-" * 50)
    
    print(f"{'Berat Paket':<25}: {berat} kg")
    print(f"{'Jarak Pengiriman':<25}: {jarak} km")
    print(f"{'Layanan Express':<25}: {'Ya' if layanan_express else 'Tidak'}")
    print(f"{'Pelanggan Member':<25}: {'Ya' if member else 'Tidak'}")
    print("-" * 50)
    
    print(f"{'Biaya Dasar':<25}: Rp 10.000")
    
    if berat > 5:
        print(f"{'Biaya Tambahan (Berat > 5kg)':<25}: Rp 5.000") 
    if jarak > 10:
        print(f"{'Biaya Tambahan (Jarak > 10km)':<25}: Rp 8.000")  
    if layanan_express:
        print(f"{'Biaya Layanan Express':<25}: Rp 20.000")
    if member:
        print(f"{'Diskon Member (10%)':<25}: Rp {int(biaya * 0.10):,}")
    
    print("=" * 50)
    print(f"{'Total Biaya Pengiriman':<25}: Rp {int(biaya):,}")
    print("=" * 50)

berat = float(input("Masukkan berat paket (kg): "))
jarak = float(input("Masukkan jarak pengiriman (km): "))
layanan_express = input("Apakah memilih layanan express (ya/tidak)? ").strip().lower() == "ya"
member = input("Apakah Anda seorang member (ya/tidak)? ").strip().lower() == "ya"

biaya_pengiriman = hitung_biaya_pengiriman(berat, jarak, layanan_express, member)
tampilkan_rincian_biaya(berat, jarak, layanan_express, member, biaya_pengiriman)

```
OUT PUT 
```
==================================================
                   RINCIAN BIAYA PENGIRIMAN      
==================================================
Nama Pelayan           : VIto Alviano Dwi Santoso
NIM Pelayan            : 312410070
--------------------------------------------------
Berat Paket            : 6.0 kg
Jarak Pengiriman       : 12.0 km
Layanan Express        : Ya
Pelanggan Member       : Ya
--------------------------------------------------
Biaya Dasar            : Rp 10.000
Biaya Tambahan (Berat > 5kg)   : Rp 5.000
Biaya Tambahan (Jarak > 10km)  : Rp 8.000
Biaya Layanan Express  : Rp 20.000
Diskon Member (10%)    : Rp 4.300
==================================================
Total Biaya Pengiriman : Rp 38.700
==================================================

```
