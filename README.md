# 🚀 Portofolio Flask — Deploy ke Vercel (GRATIS)

## 📁 Struktur Folder Lengkap

```
portfolio/
├── app.py                  ← Flask app + semua data (nama, proyek, skill, dll)
├── vercel.json             ← Konfigurasi Vercel deployment
├── requirements.txt        ← Python dependencies
├── README.md               ← Panduan ini
│
├── templates/
│   └── index.html          ← Template HTML (Jinja2)
│
└── static/
    ├── css/
    │   └── style.css       ← Semua styling
    ├── js/
    │   └── main.js         ← Animasi, load proyek, nav aktif
    └── images/
        ├── profile.jpg     ← ⭐ TARUH FOTO KAMU DI SINI
        └── cv.pdf          ← (opsional) CV untuk didownload
```

---

## 📸 Cara Menambahkan Foto

1. Rename foto kamu menjadi `profile.jpg` (atau format lain)
2. Taruh di folder `static/images/`
3. Jika nama file berbeda (misal `foto.jpg`), ubah di `app.py`:
   ```python
   "photo": "foto.jpg",   # ← ganti nama di sini
   ```

---

## ✏️ Cara Kustomisasi Data

Semua data ada di **`app.py`**, bagian `PROFILE`, `PROJECTS`, dan `SKILLS`:

```python
PROFILE = {
    "name": "Nama Kamu",          # ← Ganti nama
    "role": "...",                # ← Ganti jabatan
    "email": "kamu@email.com",    # ← Ganti email
    "photo": "profile.jpg",       # ← Nama file foto
    ...
}

PROJECTS = [
    {
        "title": "Nama Proyek",   # ← Ganti judul
        "desc": "Deskripsi...",   # ← Ganti deskripsi
        "tech": ["Python", ...],  # ← Stack teknologi
        "link": "https://...",    # ← URL GitHub
        "live": "https://...",    # ← URL live demo
    },
    ...
]
```

---

## 🛠️ Jalankan Lokal

```bash
pip install -r requirements.txt
python app.py
# Buka: http://localhost:5000
```

---

## ☁️ Deploy ke Vercel (GRATIS)

### 1. Upload ke GitHub
```bash
git init
git add .
git commit -m "portfolio init"
git branch -M main
git remote add origin https://github.com/USERNAME/portfolio.git
git push -u origin main
```

### 2. Deploy ke Vercel
1. Buka **vercel.com** → Login dengan GitHub
2. Klik **"Add New → Project"**
3. Pilih repo portfolio kamu
4. Klik **Deploy** (Vercel auto-detect Python!)
5. ✅ URL gratis: `https://portfolio-kamu.vercel.app`

### 3. Update Otomatis
Setiap `git push`, Vercel langsung redeploy otomatis.

---

## 🎨 Kustomisasi Warna

Edit variabel di `static/css/style.css`:
```css
:root {
  --bg:     #0a0a08;   /* Warna latar */
  --text:   #e8e4d9;   /* Warna teks */
  --accent: #c8b560;   /* Warna emas (aksen utama) */
}
```