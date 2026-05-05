# 📄 PDF to Word Converter

> **A professional, simple, and powerful tool to convert PDF files to Word (DOCX) documents while preserving text, layout, and extracting images**

This command-line tool is built using **PyMuPDF** and **python-docx** libraries. It provides accurate PDF-to-Word conversion with features like page range selection and automatic image extraction.

---

## ✨ Features

- 🔄 Convert PDF to Word (DOCX format) while preserving text order
- 🖼️ Extract and embed **images** into the Word document
- 📑 Select **specific page ranges** (convert only parts of the PDF)
- ⚡ High speed and optimized processing
- 📊 Display conversion statistics (pages processed, images extracted, etc.)
- 🛠️ Simple and interactive command-line interface
- ✅ Handles errors gracefully (file not found, missing libraries, etc.)

---

## 📸 Preview

```
=================================
📚 PDF TO WORD CONVERTER
=================================

📁 Enter PDF filename (with .pdf extension): document.pdf

🔄 Converting 'document.pdf' to 'document.docx'...
📖 Total pages: 10

Do you want specific pages only? (y/n): y
Enter start page (0 for first): 2
Enter end page (press Enter for last): 5

Extract images from PDF? (y/n): y

📄 Processing page 3/10...
📄 Processing page 4/10...
...

==================================================
✅ CONVERSION COMPLETE!
==================================================
📁 Input file: document.pdf
📄 Output file: document.docx
📊 Statistics:
   - Pages processed: 3
   - Images extracted: 5
   - Pages without text: 0
   - File size: 245.32 KB
==================================================
```

---

## 📋 Requirements

Make sure you have **Python 3.6 or higher** installed on your system.

Required Python packages:
- `PyMuPDF` (fitz) – for reading and extracting PDF content
- `python-docx` – for creating Word documents

---

## 🚀 Installation

### 1. Clone the repository

```bash
git clone https://github.com/imsinazn/pdf-to-word-converter.git
cd pdf-to-word-converter
```

### 2. Install required libraries

```bash
pip install PyMuPDF python-docx
```

Or if you have a `requirements.txt` file:

```bash
pip install -r requirements.txt
```

### 3. Run the script

```bash
python pdf_to_word_converter.py
```

---

## 🖥️ Usage

### Basic Usage

Simply run the script and follow the interactive prompts:

```bash
python pdf_to_word_converter.py
```

You will be asked to:
1. Enter the PDF file name (e.g., `myfile.pdf`)
2. Choose whether to convert specific pages or all pages
3. Choose whether to extract images from the PDF

### Programmatic Usage

You can also use the `convert_pdf_to_word()` function directly in your own Python code:

```python
from pdf_to_word_converter import convert_pdf_to_word

# Convert entire PDF with images
convert_pdf_to_word('input.pdf', 'output.docx')

# Convert specific pages (page 2 to 5, 0-indexed)
convert_pdf_to_word('input.pdf', 'output.docx', start=2, end=6, keep_images=True)
```

---

## 📁 Project Structure

```
pdf-to-word-converter/
│
├── pdf_to_word_converter.py   # Main script
├── README.md                   # Documentation
├── requirements.txt            # Dependencies (optional)
└── example.pdf                 # Sample PDF for testing
```

---

## 🛠️ How It Works

1. **Open PDF** – Uses PyMuPDF to open and read the PDF file.
2. **Extract Text** – Retrieves text from each page and adds it as paragraphs in Word.
3. **Extract Images** – For each page, extracts embedded images and inserts them into the Word document.
4. **Save Document** – Saves the final `.docx` file.
5. **Display Statistics** – Shows number of pages processed, images extracted, and file size.

---

## 🐛 Troubleshooting

| Issue | Solution |
|-------|----------|
| `ModuleNotFoundError` | Run `pip install PyMuPDF python-docx` |
| `File not found` | Make sure the PDF file exists in the same directory or provide the full path |
| No images extracted | Some PDFs store images in a non-standard way; try another PDF to verify |
| Poor text formatting | PDF structure varies – this tool preserves text order but not complex layouts |

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

## 👨‍💻 Author

**Sina**  
GitHub: [@imsinazn](https://github.com/imsinazn)

---

## ⭐ Support

If you find this project useful, please give it a ⭐ on GitHub and share it with others!

For issues or feature requests, feel free to [open an issue](https://github.com/imsinazn/pdf-to-word-converter/issues) on GitHub.

---

## 🙏 Acknowledgements

- [PyMuPDF](https://pymupdf.readthedocs.io/) – PDF processing library
- [python-docx](https://python-docx.readthedocs.io/) – Word document creation
```
