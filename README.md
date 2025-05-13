
### 📝 Description

This project is a simple but powerful **cybersecurity tool** that monitors changes in files by generating and comparing **SHA-256 hash values**. It helps verify whether files have been **modified**, **deleted**, or **tampered with**, which is essential for maintaining **file integrity** in sensitive systems.

---

### 🎯 Objectives

* Detect unauthorized file modifications.
* Alert when files are deleted or newly added.
* Build foundational understanding of cryptographic hash functions.
* Demonstrate practical Python scripting skills in cybersecurity.

---

### 🧰 Technologies Used

| Tool         | Purpose                        |
| ------------ | ------------------------------ |
| Python       | Core language                  |
| hashlib      | Generate SHA-256 hashes        |
| os           | Traverse file directories      |
| json         | Store and compare hash data    |
| Google Colab | Cloud-based Python development |

---

### 🚀 How It Works

1. **Initial Scan**:

   * Upload a folder (as a ZIP file).
   * The tool calculates SHA-256 hashes of all files.
   * Hashes are saved in a `hashes.json` file.

2. **File Change Detection**:

   * Upload a new/modified version of the folder.
   * The tool re-scans and compares new hashes with the old.
   * Reports all:

     * 🔁 Modified files
     * ❌ Deleted files
     * ➕ New files

---

### 📂 File Structure

```
/IntegriScan/
├── README.md
├── IntegriScan.ipynb   ← Python code (Colab Notebook)
├── hashes.json                    ← Saved file hashes
├── /test_folder/                  ← Sample files 
```

---

### ⚙️ How to Run (Google Colab)

1. Open the Colab notebook.
2. Upload a `.zip` file of the folder to scan.
3. Run all cells:

   * It extracts and scans the files.
   * Stores hashes in `hashes.json`.
4. Modify one or more files and upload the folder again (as a new ZIP).
5. Run the comparison block to see detected changes.

---

### 📌 Features

* SHA-256 hashing for security.
* JSON storage for portability and future scans.
* Change detection in real time.
* Designed to run fully inside Google Colab.


---

### 🔒 Why SHA-256?

SHA-256 is a **cryptographic hash function** that generates a unique, fixed-size string for any file. It's widely trusted for its:

* Collision resistance
* Irreversibility
* Speed and efficiency

---

### 🧪 Test Example

You can test the tool by:

* Creating a few text files.
* Running the scan once.
* Editing a file (e.g., adding a line).
* Running the scan again and comparing results.

Expected output:

```
🔍 File Change Report:
📝 Modified Files:
 - file2.txt
❌ Deleted Files:
 - None
➕ New Files:
 - None
```


