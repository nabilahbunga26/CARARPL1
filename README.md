

# 🟢 0. PERSIAPAN (INSTALL GIT)

Kalau Git belum ada:

1. Download di: [https://git-scm.com/download/win](https://git-scm.com/download/win)
2. Install → klik **Next terus** sampai selesai
3. Buka **Windows PowerShell**, cek:

```powershell
git --version
```

👉 Kalau muncul versi → Git sudah siap

---

# 🟢 1. KONFIGURASI GIT (IDENTITAS KAMU)

Ini supaya Git tahu siapa yang bikin commit.

Ketik:

```powershell
git config --global user.name "Nabilah Bunga Sulistia"
git config --global user.email "emailkamu@gmail.com"
```

Cek:

```powershell
git config --list
```

👉 Pastikan nama & email kamu muncul

---

# 🟢 2. FORK REPOSITORY (WAJIB BANGET)

Ini langkah yang paling sering salah.

### Cara:

1. Buka:
   👉 [https://github.com/Lab-RPL-ITS/module-pelatihan-vcs](https://github.com/Lab-RPL-ITS/module-pelatihan-vcs)

2. Klik tombol **Fork** (kanan atas)

3. Pilih akun kamu: `nabilahbunga26`

👉 Hasil:
Sekarang kamu punya repo sendiri:

```
https://github.com/nabilahbunga26/module-pelatihan-vcs
```

📌 Ini penting:

* Repo lab = tidak boleh langsung diedit
* Repo fork = tempat kamu ngerjain tugas

---

# 🟢 3. CLONE KE LAPTOP

Sekarang ambil repo ke laptop kamu.

Di PowerShell:

```powershell
git clone https://github.com/nabilahbunga26/module-pelatihan-vcs.git
```

Masuk ke folder:

```powershell
cd module-pelatihan-vcs
```

👉 Sekarang kamu sudah punya project di laptop

---

# 🟢 4. CEK REMOTE (BIAR NGGAK SALAH REPO)

Ketik:

```powershell
git remote -v
```

👉 Harus muncul:

```
origin https://github.com/nabilahbunga26/module-pelatihan-vcs
```

Kalau bukan ini → berarti salah clone ❌

---

# 🟢 5. BUAT BRANCH (WAJIB)

Jangan kerja di `main`.

Format:

```
penugasan/nama_kamu
```

Ketik:

```powershell
git checkout -b penugasan/nabilah
```

Cek:

```powershell
git branch
```

👉 Harus ada tanda `*` di:

```
* penugasan/nabilah
```

---

# 🟢 6. BUAT FOLDER TUGAS

Sesuai aturan:

```
tugas/pelatihan-vcs-2026/nama_kamu
```

Ketik:

```powershell
New-Item -ItemType Directory -Force -Path .\tugas\pelatihan-vcs-2026\nabilah
```

👉 Ini bikin folder khusus punyamu

---

# 🟢 7. SALIN LANDING PAGE

⚠️ Jangan edit folder `landing-page`

Ketik:

```powershell
Copy-Item -Path .\landing-page\* -Destination .\tugas\pelatihan-vcs-2026\nabilah -Recurse
```

👉 Artinya:

* semua file HTML/CSS disalin ke folder kamu

---

# 🟢 8. BUAT FILE README.md

Masuk ke folder kamu dan buat file:

Isi WAJIB:

```
Nama: Nabilah Bunga Sulistia
Pelatihan: VCS RPL 2026
```

Cara cepat:

```powershell
@"
Nama: Nabilah Bunga Sulistia
Pelatihan: VCS RPL 2026
"@ | Out-File -FilePath .\tugas\pelatihan-vcs-2026\nabilah\README.md -Encoding utf8
```

---

# 🟢 9. CEK PERUBAHAN

Sebelum simpan:

```powershell
git status
```

👉 Harus muncul:

* folder baru
* file baru

---

# 🟢 10. MASUKKAN KE GIT (ADD)

```powershell
git add .
```

👉 Artinya: semua file siap disimpan

---

# 🟢 11. COMMIT

```powershell
git commit -m "menambahkan tugas pelatihan vcs"
```

👉 Artinya:
kamu menyimpan perubahan ke repo lokal

---

# 🟢 12. PUSH KE GITHUB

```powershell
git push -u origin penugasan/nabilah
```

👉 Artinya:
kirim hasil kerja ke GitHub kamu

---

# 🟢 13. BUAT PULL REQUEST (PENGUMPULAN)

Ini langkah terakhir & WAJIB ❗

1. Buka GitHub repo kamu

2. Akan muncul tombol:
   👉 **Compare & pull request**

3. Klik

4. Pastikan:

* from: `penugasan/nabilah`
* to: `main` repo lab

5. Klik:
   👉 **Create Pull Request**

---


Tinggal bilang:
**“aku error di step …”** 👍
