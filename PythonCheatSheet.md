# Python `py` Launcher Cheat Sheet (Windows)
Mengelola Multi Versi Python dengan Python Launcher

---

## 1. Cek Python Launcher

Cek apakah `py` tersedia:
```bash
py
```

Cek versi launcher:
```bash
py --version
```

---

## 2. List Semua Versi Python Terpasang

Daftar versi:
```bash
py -0
```

Daftar versi lengkap dengan path:
```bash
py -0p
```

Contoh output:
```
Installed Pythons found by py Launcher for Windows
 -3.12-64 C:\Python312\python.exe
 -3.11-64 C:\Python311\python.exe
 -3.9-64  C:\Python39\python.exe
```

---

## 3. Menjalankan Python Versi Tertentu

Versi mayor:
```bash
py -3
py -2
```

Versi spesifik:
```bash
py -3.12
py -3.11
py -3.9
```

Versi + arsitektur:
```bash
py -3.11-64
py -3.11-32
```

---

## 4. Menjalankan File Python

```bash
py -3.12 script.py
```

```bash
py -3.9 main.py
```

---

## 5. Masuk REPL Python Versi Tertentu

```bash
py -3.11
```

Keluar:
```python
exit()
```

---

## 6. Menjalankan Module (`pip`, `venv`, dll)

pip versi tertentu:
```bash
py -3.12 -m pip install requests
```

upgrade pip:
```bash
py -3.12 -m pip install --upgrade pip
```

---

## 7. Virtual Environment (venv)

Buat venv:
```bash
py -3.12 -m venv .venv
```

Aktivasi venv:
```bash
.venv\Scripts\activate
```

Deactivate:
```bash
deactivate
```

---

## 8. Cek Python Aktif (Dalam venv)

```bash
python --version
```

```bash
where python
```

---

## 9. Shebang untuk Multi Versi

Gunakan di baris pertama file `.py`:
```python
#! python3.11
```

Atau:
```python
#! python3
```

---

## 10. Menentukan Python Default (py.ini)

Lokasi file:
```
%LOCALAPPDATA%\py.ini
```

Contoh isi:
```
[defaults]
python=3.11
```

---

## 11. Troubleshooting

Cek apakah `python` ≠ `py`:
```bash
python --version
py --version
```

Pastikan pip sesuai versi:
```bash
py -3.11 -m pip --version
```

---

## 12. Best Practices

- Gunakan `py` untuk SEMUA eksekusi Python
- Jangan mengandalkan PATH
- Satu project = satu venv
- Selalu install package via `py -X -m pip`

---

## 13. Ringkasan Cepat

```bash
py -0p                 # list semua python
py -3.12               # jalankan python 3.12
py -3.12 script.py     # jalankan file
py -3.12 -m pip install x
py -3.12 -m venv .venv
```
