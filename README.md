# Simulasi Konfigurasi IP Print Server

Laboratorium virtual interaktif untuk siswa jaringan: mensimulasikan proses
menghubungkan Print Server ke Switch, menentukan **IP Statis** yang valid pada
subnet `192.168.1.0/24`, lalu menguji koneksi lewat terminal PC-01.

Tampilan menyerupai Cisco Packet Tracer. Seluruhnya berjalan di browser tanpa
instalasi apa pun.

## Fitur

- **4 tahap misi** berurutan dengan sistem skor (maks. 100) dan timer.
- **Topologi jaringan SVG** (Router, Switch, 2 PC, Print Server) dengan kabel
  yang digambar ulang otomatis setiap ukuran layar berubah.
- **Animasi paket ICMP** yang tetap terlihat di atas modal.
- **Puzzle subnet**: siswa memilih IP / Subnet Mask / Default Gateway yang benar.
- **Validasi IP lengkap**: format IPv4, konflik IP, network/broadcast address,
  dan gateway di luar subnet.
- **Terminal PC-01** dengan perintah `ping`, `print test`, `ipconfig`, `cls`.
- **Efek suara** sintetis via Web Audio API, tanpa file audio eksternal.
- **Responsif** — dapat dipakai di HP, tablet, maupun desktop.

## Menjalankan secara lokal

Buka `index.html` di browser. Tidak ada build step dan tidak ada dependency
yang perlu dipasang.

## Publish ke GitHub Pages

```bash
git init
git add .
git commit -m "feat: simulasi konfigurasi IP print server"
git branch -M main
git remote add origin https://github.com/USERNAME/REPO.git
git push -u origin main
```

Kemudian di GitHub: **Settings → Pages → Source: Deploy from a branch →
Branch: main, folder: / (root) → Save**.

Situs akan tayang di `https://USERNAME.github.io/REPO/`.
File `.nojekyll` sudah disertakan agar Jekyll tidak memproses halaman.

## Struktur Berkas

```
index.html    # seluruh aplikasi (HTML + Tailwind CDN + JS vanilla)
.nojekyll     # menonaktifkan proses Jekyll pada GitHub Pages
README.md
```

## Catatan Teknis

- Tailwind dimuat dari CDN (`cdn.tailwindcss.com`). Outer offline penuh tidak
  tersedia. Untuk production, pertimbangkan kompilasi Tailwind secara lokal.
- Font Awesome dimuat dari `cdnjs.cloudflare.com`.
- State simulasi hanya disimpan di memori. Muat ulang halaman untuk mengulang.
- Skor diberikan 25 poin per tahap yang diselesaikan, total 100.

## Lisensi

Untuk keperluan pembelajaran dan pengajaran.
