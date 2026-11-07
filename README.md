# caption-umkm-ai

CLI kecil yang menyusun prompt siap-tempel untuk meminta AI menulis caption atau deskripsi produk UMKM Indonesia. Prompt memasukkan nama, fakta, dan harga yang diberikan penjual, lalu mengingatkan model agar tidak mengarang manfaat, stok, sertifikasi, diskon, testimoni, atau klaim lain.

## Contoh

```sh
caption-umkm \
  --nama "Keripik Pisang" \
  --fakta "Berat bersih 100 g" \
  --fakta "Dibuat di Bandung" \
  --harga "Rp18.000" \
  --kanal whatsapp \
  --gaya hangat
```

Salin prompt yang tercetak ke chatbot AI pilihan Anda. Kanal yang tersedia: `whatsapp`, `instagram`, `marketplace`. Gaya: `hangat`, `ringkas`, `profesional`.

Tanpa instalasi perintah:

```sh
python -m caption_umkm --nama "Kopi Susu" --fakta "Botol 250 ml" --kanal instagram
```

Instalasi (Python 3.9+):

```sh
python -m pip install .
```

## Privasi dan batasan

Tool ini berjalan lokal tanpa API, telemetri, atau dependensi runtime. Detail produk tidak dikirim ke mana pun oleh program. Namun, argumen perintah bisa tersimpan di shell history; hindari memasukkan informasi sensitif yang tidak perlu. Model AI tetap dapat membuat kesalahan walau diberi instruksi grounding, jadi tinjau hasil sebelum dipublikasikan. Alat ini membuat prompt, bukan menghasilkan caption atau memverifikasi klaim secara otomatis.

## Tes

```sh
python -m unittest discover -s tests -v
```

## Lisensi

MIT. Lihat [LICENSE](LICENSE).
