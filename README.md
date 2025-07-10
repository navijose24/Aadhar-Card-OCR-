
## 📄 Aadhar OCR Extraction using Tesseract

This project extracts key information such as **Name**, **Date of Birth**, **Aadhar Number**, and **Gender** from an uploaded Aadhar card image using the `pytesseract` OCR engine in Google Colab.

### 🚀 Features

* 📤 Upload any Aadhar card image
* 🧠 Uses Tesseract OCR (pre-trained, no custom model needed)
* 🔍 Extracts:

  * 👤 Name
  * 🎂 Date of Birth
  * 🆔 Aadhar Number
  * 🚻 Gender
* 💡 Works directly inside Google Colab — no installation needed on your system

---

### 📦 Requirements

Google Colab already includes all required packages, but for local use:

```bash
pip install pytesseract pillow
sudo apt install tesseract-ocr
```

---

### 🛠️ How It Works

1. Upload an image of the Aadhar card in Colab.
2. Image is read using Pillow and passed to Tesseract.
3. Extracted text is parsed using regex to locate:

   * Name (from capitalized line near DOB)
   * Date of Birth (`dd/mm/yyyy`)
   * Aadhar Number (`XXXX XXXX XXXX`)
   * Gender (`Male` or `Female`)
4. Final output is printed clearly.

---

### 🔁 Example Output

```text
✅ Extracted Info:
👤 Name      : John Doe
🎂 DOB       : 15/03/1985
🆔 Aadhar No : 1234 5678 9012
🚻 Gender    : Male
```

---

### 🧠 Tech Stack

* Python 🐍
* Google Colab 📓
* Tesseract OCR 🔎
* Regex 🧵
* Pillow (PIL) 🖼️

---

### 📁 Folder Structure (if exported)

```
├── Aadhar_OCR.ipynb
├── README.md
└── sample_images/
    └── aadhar_sample.jpg
```

---

### ✅ To-Do / Improvements

* [ ] Image preprocessing (binarization, resizing)
* [ ] Hindi/Multilingual OCR support
* [ ] Streamlit frontend for local use
* [ ] Save output to CSV or PDF

---

💬 Built with ❤️ for learning & open-source sharing

---
