# UTS Data Acquisition & Management

*Nama:* [Ach. rafli alfian syah] | *NIM:* 2501010048 | *Kelas:* E
*Dosen:* Dr. I Gede Totok Suryawan, S.Kom., M.T.
*Topik:* Kedatangan wisatawan mancanegara ke Bali per negara per bulan (2025) dan cuaca bulanan Bali

## Sumber data dan URL

| Cara akuisisi | Sumber | URL | Berkas mentah |
|---|---|---|---|
| Berkas dataset | Dinas Pariwisata Prov. Bali, Statistik Pariwisata 2025 (sheet tab7ok) | https://disparda.baliprov.go.id/category/data-statistik/ | data/raw/Table-1-7-Final-5.xls |
| API | Open-Meteo Archive API (cuaca harian, Ngurah Rai, 2025) | https://archive-api.open-meteo.com/v1/archive?latitude=-8.7467&longitude=115.1668&start_date=2025-01-01&end_date=2025-12-31&daily=temperature_2m_max,temperature_2m_min,precipitation_sum&timezone=Asia%2FMakassar | data/raw/openmeteo_bali_2025.json |
| Scraping | Wikipedia, List of districts in Bali | https://en.wikipedia.org/wiki/List_of_districts_in_Bali | data/raw/wikipedia_districts_bali.html |
| Bukti robots.txt | Wikipedia robots.txt | https://en.wikipedia.org/robots.txt | data/raw/robots_wikipedia.txt |

Tanggal akses: 19 November 2026. Lisensi dan hash MD5 lengkap ada di docs/provenance.csv.

## Struktur repositori

- UTS_Akuisisi_Data.ipynb: notebook berisi Soal 1 sampai 5
- data/raw/: data mentah, tidak diubah
- data/interim/: hasil pembersihan dan normalisasi
- data/processed/: hasil penggabungan berkas + API (wisman_bali_2025_cuaca.csv)
- docs/: provenance, Data Ethics Checklist, identifikasi dataset, metadata penggabungan

## Catatan

- Data wisman bersifat sementara (temporary data) menurut catatan di berkas sumber.
- Cuaca hanya mewakili satu titik (sekitar Bandara Ngurah Rai).
- Tabel hasil scraping (Soal 4) tidak ikut digabung.
- Tidak ada API key atau kredensial di notebook.
