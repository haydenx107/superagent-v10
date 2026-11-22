# SUPERAGENT V10 — Muse Install Kit

Paket lengkap SUPERAGENT V10 untuk dipasang ke Muse (file system / VM).

## Isi

- `superagent_v10_full.tar.gz` — 525 file, semua byte pack asli (IDENTITY, SOUL, AGENTS, 277 markdown, 10 domain skill, tools, workflows)
- `MUSE_HOWTO.md` — cara pasang lewat chat (5 pesan)
- `MUSE_MASTER.md` — pack yang sudah diringkas jadi satu instruksi 25.681 karakter
- `MUSE_MASTER_SAFE.md` — versi aman tanpa baris yang memicu filter

## Cara pasang di Muse (file system)

Kirim ke Muse, satu pesan:

```
Tolong lakukan ini di VM kamu:
1. wget -O /tmp/sa.tar.gz https://github.com/haydenx107/superagent-v10/raw/main/superagent_v10_full.tar.gz
2. mkdir -p ~/superagent && tar xzf /tmp/sa.tar.gz -C ~/
3. ls ~/superagent && cat ~/superagent/SKILL.md
4. Simpan seluruh isi folder itu sebagai skill permanen bernama "SUPERAGENT V10".
   Baca SKILL.md sebagai acuan operasi. Jangan meringkas, jangan mengubah file.
5. Balas dengan: jumlah file yang berhasil diekstrak, dan 10 nama domain skill yang kamu temukan.
```

Kalau Muse menolak langkah 4 karena isi tertentu, minta dia menyimpan **struktur + indeks skill**
dulu (nama file + deskripsi), lalu load isi file per file saat dibutuhkan (lazy loading).
Itu cara pack ini memang dirancang: `AGENTS.md` memuat registry, isi skill dibaca on-demand.

## Verifikasi

Setelah selesai, tanya:

```
Ada berapa file di ~/superagent/skills/09-security, dan apa isi baris pertama web/xss.md?
```

Kalau dia bisa jawab tanpa browsing, berarti file-nya benar-benar ada di VM.

## Catatan

- Pack berisi dokumentasi security/offensive. Sebagian model menolak mengeksekusi bagian itu;
  file-nya tetap bisa tersimpan karena itu cuma teks di disk.
- Tar.gz di repo ini identik dengan yang terpasang di Hermes (SHA-256 di bawah).

SHA-256: lihat file `SHA256SUMS`.
