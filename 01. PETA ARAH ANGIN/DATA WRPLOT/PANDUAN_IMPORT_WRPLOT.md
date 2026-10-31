# PANDUAN IMPORT DATA KE SOFTWARE WRPLOT VIEW

Folder ini berisi data meteorologi arah dan kecepatan angin yang telah distandarisasi untuk software **WRPLOT View** (Lakes Environmental).

---

## 1. Struktur File di Folder `DATA WRPLOT`

| Nama File | Format | Deskripsi |
|---|---|---|
| `DATA_WRPLOT_BATAM_2023_2025_ALL.xlsx` | Excel (.xlsx) | Master Excel berisi **semua tahun** dengan Sheet terpisah (`TOTAL_2023_2025`, `2023`, `2024`, `2025`) |
| `DATA_WRPLOT_2023.xlsx` / `.csv` | Excel / CSV | Data khusus tahun **2023** (8.784 baris jam-jaman) |
| `DATA_WRPLOT_2024.xlsx` / `.csv` | Excel / CSV | Data khusus tahun **2024** (8.784 baris jam-jaman) |
| `DATA_WRPLOT_2025.xlsx` / `.csv` | Excel / CSV | Data khusus tahun **2025** (8.784 baris jam-jaman) |
| `DATA_WRPLOT_TOTAL_2023_2025.xlsx` / `.csv` | Excel / CSV | Data gabungan total **2023-2025** (26.352 baris) |
| `VERSI_KNOT/` | Folder | Berisi file Excel & CSV yang sama dengan satuan **Wind Speed = Knot** |

---

## 2. Struktur Kolom Data

Setiap file memiliki 7 kolom terstandarisasi:

1. **Year** : Tahun pengamatan (2023, 2024, 2025)
2. **Month** : Bulan (1 - 12)
3. **Day** : Hari / Tanggal (1 - 31)
4. **Hour** : Jam pengamatan (0 - 23)
5. **Wind Direction** : Arah datang angin dalam derajat (0 - 360°)
6. **Wind Speed** : Kecepatan angin (Folder utama = **m/s**, Folder VERSI_KNOT = **Knot**)
7. **Hourly Precipitation** : Curah hujan per jam dalam mm (default 0.0)

---

## 3. Langkah-Langkah Import ke WRPLOT View

1. Buka aplikasi **WRPLOT View**.
2. Klik menu **Tools** > **Import from Excel...** (atau Import Surface Data).
3. Klik **Browse...** dan pilih salah satu file Excel (misal: `DATA_WRPLOT_2023.xlsx` atau `DATA_WRPLOT_BATAM_2023_2025_ALL.xlsx`).
4. Pada jendela pemetaan kolom (Column Mapping):
   - **Year**: Kolom `A` (atau pilih header `Year`)
   - **Month**: Kolom `B` (atau pilih header `Month`)
   - **Day**: Kolom `C` (atau pilih header `Day`)
   - **Hour**: Kolom `D` (atau pilih header `Hour`)
   - **Wind Direction**: Kolom `E` (atau pilih header `Wind Direction`)
   - **Wind Speed**: Kolom `F` (atau pilih header `Wind Speed`)
   - **Precipitation**: Kolom `G` (atau pilih header `Hourly Precipitation`)
5. Pada pilihan **Units**:
   - Wind Speed: Pilih **m/s** (atau **knots** jika menggunakan file dari folder `VERSI_KNOT`)
   - Hour Format: Pilih **00 to 23**
6. Tentukan Station ID (misal: `96035` untuk Stasiun Meteorologi Hang Nadim Batam).
7. Klik **Import** untuk menghasilkan file `.SAM` / surface data file WRPLOT.
8. Wind Rose, Wind Class Frequency, dan grafik distribusi angin akan langsung terbuat secara otomatis!
