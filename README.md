# BOMVBAExcel
Bill Of Material in Microsoft Excel VBA Format

PANDUAN SINGKAT SISTEM BOM

KONSEP
FG (parent) > SUB ASSY (Level 1 yang punya anak) > PART (anak di bawahnya).
Contoh: Z364 (FG) > ZKS34 (Sub Assy, proses Bush Stacking) > ZK34 dan ZU11 (Part).
Kolom Tipe terisi otomatis: FG = parent, SUB ASSY = part yang punya anak tepat di bawahnya, PART = selainnya.
Kolom Supplier / Proses diisi bebas, mis. S/A BUSH STACKING, S/A PRESS 600T, etc.

A. MEMBUAT BOM BARU
1. Di MENU klik INPUT BOM BARU.
2. Isi data FG: Unique No (mis. Z364), Part No / Cust P/N, Nama Produk, Customer, Project. Klik PILIH GAMBAR PARENT.
3. Isi baris part mulai baris 12: Level, Unique No, Part No, Nama, Qty, Satuan, Qty/Box, Supplier / Proses, Material, Keterangan.
   Level 1 = anak langsung FG (mis. ZKS34). Level 2 = anak dari Level 1 tepat di atasnya (mis. ZK34, ZU11), dst sampai Level 4.
   Tulis berurutan: setelah satu Sub Assy (Level 1), tulis komponennya (Level 2) tepat di bawahnya.
4. Klik satu sel pada baris part, lalu PILIH GAMBAR BARIS AKTIF untuk memasang gambar.
5. Klik SIMPAN BOM. Nomor (1, 1.1, 1.2, 2 ...) dan Qty total dihitung otomatis.

B. MENCARI
1. Buka sheet CARI, ketik kata kunci (Unique No, Part No, nama, supplier/proses, material, atau customer/project), klik CARI.
2. 'Cari di' membatasi hasil: Produk (FG), Sub Assy, atau Part saja.
3. Kolom 'Induk Langsung' dan 'Produk (FG)' menunjukkan item itu dipakai di sub assy dan FG mana.
4. Klik satu baris hasil, lalu LIHAT LAPORAN BOM atau MUAT KE FORM.

C. LAPORAN
- LAPORAN: BOM bertingkat berwarna per level, SUB ASSY ditandai oranye, plus gambar. Tombol 1/2/3 di kiri untuk collapse/expand.
- DAFTAR_BELI: rekap PART ujung dengan Qty sudah dikalikan sampai FG, lengkap dengan Supplier / Proses dan Qty/Box.
- EXPORT PDF atau EXPORT KE EXCEL untuk dikirim ke orang lain.

D. REVISI
1. Pilih BOM di MENU, klik MUAT BOM, ubah data, ganti nomor Revisi, lalu SIMPAN BOM (menjadi revisi baru).
2. Jika Revisi tidak diganti, BOM lama akan ditimpa (ada konfirmasi).

CATATAN PENTING
- Gambar disalin otomatis ke folder 'gambar_bom' di samping file ini. Jangan pisahkan folder itu dari file Excel.
- Nama file gambar mengikuti Unique No (atau Part No bila Unique No kosong). Gambar baru untuk kode yang sama akan menggantikan yang lama.
- Jangan edit sheet DB_BOM secara manual, kecuali Anda paham strukturnya.
- Aktifkan Macro saat membuka file (Enable Content).


<img width="1563" height="613" alt="image" src="https://github.com/user-attachments/assets/8eb1602b-37c6-4c0f-afb9-fb1a4db8d104" />
<img width="1552" height="608" alt="image" src="https://github.com/user-attachments/assets/fa9147f1-4d0f-422d-aa9f-a9fc4ffdc6c9" />


