
# GIS Digitasi Lahan - EPSG:4326 WGS84

Prototype MVP uji bertahap untuk digitasi bidang tanah sawah/ladang/kebun/pekarangan/kolam.

**Fitur:**
- Satu layar GIS dominan peta (100vh, no scroll)
- EPSG:4326 - WGS84, koordinat LAT/LON live di bawah peta
- Geolokasi selalu aktif (watchPosition high accuracy) + blue dot + accuracy circle
- Geotag otomatis per titik (lat,lon,acc,timestamp)
- Penggunaan lahan: Sawah, Ladang, Kebun, Pekarangan, Kolam, Lainnya (warna transparansi 30%)
- Metode: Manual Tap & GPS Track (filter jarak 1-10m)
- Upload peta offline: GeoJSON, MBTiles, GeoTIFF, PDF (georeference 2 titik)
- Perhitungan luas geodesic WGS84 & keliling haversine
- Simpan localStorage, auto increment P001->P002, ekspor GeoJSON

## Struktur File
- `index.html` - Versi V4 terbaru (1-layar + uploader)
- `v3_single_screen.html` - V3 stabil tanpa uploader
- `docs/` - nanti untuk GitHub Pages docs

## Deploy ke GitHub Pages (3 menit)

1. Buat repo baru di GitHub: `gis-digitasi-epsg4326`
2. Upload file:
   ```bash
   git init
   git add .
   git commit -m "MVP GIS EPSG:4326 V4"
   git branch -M main
   git remote add origin https://github.com/USERNAME/gis-digitasi-epsg4326.git
   git push -u origin main
   ```
3. Di GitHub repo > Settings > Pages > Source: Deploy from branch `main` / root
4. Link akan jadi: `https://USERNAME.github.io/gis-digitasi-epsg4326/`

Buka link itu di HP -> langsung bisa digitasi, GPS aktif.

## GitHub untuk Kolaborasi

- `Issues` untuk bug: "Peta blank di Xiaomi"
- `Branches`: `dev/upload-mbtiles` untuk fitur MBTiles extractor
- `Releases`: tag V1.0 setelah uji lapangan lolos

## Roadmap V5
- [ ] Extractor MBTiles via sql.js wasm (offline full)
- [ ] Parser GeoTIFF via geotiff.js (bounds otomatis)
- [ ] Foto patok + tanda tangan pemilik
- [ ] Ekspor SHP ZIP + CSV
- [ ] PWA installable (manifest.json + service worker) untuk 100% offline

## Lisensi
MIT - bebas pakai untuk PTSL / GTRA / pemetaan partisipatif.

Koordinat sistem: EPSG:4326 - WGS84 (LatLon)
Dibuat: Bandung, 2026
