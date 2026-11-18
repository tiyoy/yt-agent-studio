# 🎬 YouTube Agent Studio

**AI command center untuk kreator YouTube** — aplikasi web lokal (single file HTML) untuk menyusun prompt siap kirim ke ChatGPT atau Claude, mencakup naskah, paket publikasi, editing, komentar, Shorts, SEO, chapter, dan audit channel.

> Aplikasi ini adalah **pembuat brief/prompt lokal**, bukan koneksi langsung ke Claude, ChatGPT, atau YouTube API. Hasil analisis AI diperoleh setelah prompt disalin dan dikirim ke model AI.

---

## ✨ Fitur

| Skill | Command | Fungsi |
|---|---|---|
| Script & Hook | `/yt-script` | Mengubah ide menjadi naskah video dengan hook, alur, dan CTA |
| Upload Package | `/yt-package` | Menyusun opsi judul, konsep thumbnail, deskripsi, dan angle |
| Editing Assistant | `/yt-edit` | Menganalisis transkrip/SRT untuk membuat cut list dan editing plan |
| Comment Manager | `/yt-comment` | Mengelompokkan komentar dan menyusun balasan sesuai gaya channel |
| Shorts Builder | `/yt-shorts` | Mencari momen terbaik dari video panjang untuk dijadikan Shorts |
| SEO Assistant | `/yt-seo` | Membuat judul, deskripsi, tag, dan hashtag tanpa keyword stuffing |
| Video Chapters | `/yt-chapters` | Menyusun chapter berdasarkan timestamp dan perubahan topik |
| Channel Audit | `/yt-audit` | Evaluasi channel dan prioritas perbaikan berbasis data |

- ✅ **Offline ready** — tanpa server, tanpa API key, cukup buka file HTML
- ✅ **Copy to clipboard** — tombol "Salin Prompt" di setiap output
- ✅ **Anti-halusinasi** — prompt secara eksplisit melarang AI mengarang fakta/timestamp

---

## 🚀 Cara Penggunaan

1. Buka `index.html` di browser (double-click, atau via `Start-Process index.html`).
2. Pilih skill di sidebar kiri (contoh: *Script & Hook*).
3. Isi form brief sesuai kebutuhan (topik, format, gaya, dll).
4. Klik **✦ Buat Prompt** — prompt lengkap muncul di panel output.
5. Klik **Salin Prompt**.
6. Tempel ke [ChatGPT](https://chat.openai.com) atau [Claude](https://claude.ai) untuk mendapatkan hasilnya.

### Contoh alur (Script & Hook)

1. Pilih **✍️ Script & Hook**.
2. Isi *Topik*: "Kenapa roda kemudi mobil Indonesia berada di kanan?"
3. Pilih *Format*: "Video panjang 5-10 menit", *Gaya*: "Dokumenter sinematik".
4. Klik **Buat Prompt** → **Salin Prompt**.
5. Kirim ke ChatGPT/Claude → terima naskah lengkap dengan opsi hook.

---

## 📸 Screenshot Setiap Halaman

Aplikasi terdiri dari 1 halaman dengan 8 modul yang diakses lewat sidebar:

### 1. Script & Hook Generator (`/yt-script`)
Mengubah ide menjadi naskah dengan hook kuat, alur jelas, dan CTA.

![Script & Hook Generator](docs/screenshots/script.png?v=2)

### 2. Upload Package Generator (`/yt-package`)
Menyiapkan 10 opsi judul, 3 konsep thumbnail, dan angle publikasi.

![Upload Package Generator](docs/screenshots/package.png?v=2)

### 3. Editing Assistant (`/yt-edit`)
Analisis transkrip/SRT untuk menemukan jeda, filler, dan potensi pemotongan.

![Editing Assistant](docs/screenshots/edit.png?v=2)

### 4. Comment Manager (`/yt-comment`)
Klasifikasi komentar penonton dan susun balasan sesuai karakter channel.

![Comment Manager](docs/screenshots/comment.png?v=2)

### 5. Shorts Builder (`/yt-shorts`)
Menemukan bagian terkuat dari video panjang untuk diubah menjadi konsep Shorts.

![Shorts Builder](docs/screenshots/shorts.png?v=2)

### 6. YouTube SEO Assistant (`/yt-seo`)
Metadata yang relevan dan natural: keyword, tag, hashtag, deskripsi.

![YouTube SEO Assistant](docs/screenshots/seo.png?v=2)

### 7. Video Chapters Generator (`/yt-chapters`)
Chapter informatif berdasarkan timestamp dan perubahan topik.

![Video Chapters Generator](docs/screenshots/chapters.png?v=2)

### 8. Channel Audit (`/yt-audit`)
Evaluasi channel, prioritas perbaikan, eksperimen 30 hari, dan metrik.

![Channel Audit](docs/screenshots/audit.png?v=2)

---

## 📁 Struktur Proyek

```
yt-agent-studio/
├── index.html          # Seluruh aplikasi (HTML + CSS + JS dalam satu file)
└── docs/
    └── screenshots/    # Screenshot setiap modul
        ├── script.png
        ├── package.png
        ├── edit.png
        ├── comment.png
        ├── shorts.png
        ├── seo.png
        ├── chapters.png
        └── audit.png
```

---

## 🔧 Teknologi

- **HTML5 + CSS3 + Vanilla JavaScript** — tanpa framework, tanpa dependensi
- Tema gelap responsif (breakpoint 800px untuk tampilan mobile)
- Clipboard API untuk tombol salin

## ⚠️ Catatan Keamanan

Jangan masukkan API key, password, atau data sensitif ke halaman ini. Aplikasi hanya menyusun teks prompt di browser dan tidak mengirim data ke mana pun.
