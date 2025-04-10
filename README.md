# FileIntegrityChecker
# 🔐 File Integrity Checker using Hash Functions

A Python-based utility to verify the **integrity of files** using cryptographic hash functions like **SHA-256**, **SHA-1**, or **MD5**.

This tool can:
- 🔍 Generate secure hashes for files in a folder
- 📄 Save them in a `manifest.json`
- ✅ Verify if any files have been modified, tampered with, or corrupted later

---

## 📁 Project Structure

```
FileIntegrityChecker/
├── file_integrity_checker.py   # Main Python script
├── test_files/                 # Folder with sample text files
│   ├── file1.txt
│   └── file2.txt
└── manifest.json               # Generated file hash manifest (after running)
```

---

## 🚀 Features

- ✅ Detect file corruption or tampering
- 🔐 Uses SHA-256 by default (can switch to md5, sha1, etc.)
- 📁 Supports recursive folder scanning
- 📦 Easy to use and deploy

---

## 🛠️ How to Use

### 🔹 1. Clone the Repo

```bash
git clone https://github.com/yourusername/FileIntegrityChecker.git
cd FileIntegrityChecker
```

### 🔹 2. Generate Hash Manifest

```bash
python file_integrity_checker.py --generate test_files
```

> This will create `manifest.json` storing the hash of every file.

### 🔹 3. Verify File Integrity

After you modify a file, run:

```bash
python file_integrity_checker.py --verify manifest.json
```

📍 Output will show:
- ✅ OK — if the file matches the original hash
- ❌ CORRUPTED or MISSING — if changed or deleted

---

## 🔧 Optional: Change Hash Algorithm

```bash
python file_integrity_checker.py --generate test_files --hash sha1
```

Available algorithms:
- `md5`
- `sha1`
- `sha256`
- `sha512`

---

## 📸 Sample Output

```bash
$ python file_integrity_checker.py --verify manifest.json

test_files/file1.txt: ✅ OK
test_files/file2.txt: ❌ CORRUPTED or MISSING
```

---

## 🧪 Test Files

You can modify `file2.txt` in the `test_files` folder to simulate tampering and see how the tool catches it!

---

## 📚 License

MIT License — free to use, modify, and distribute.

---


