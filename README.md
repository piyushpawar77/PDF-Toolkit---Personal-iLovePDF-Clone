# 📄 PDF Toolkit - Personal iLovePDF Clone

**A comprehensive PDF manipulation tool built with Python and Gradio, offering all essential PDF operations through a clean web interface. Perfect for personal use with no authentication or storage required.**

## 🌟 Features

### 🔧 Complete PDF Operations
- **🔗 Merge PDFs** - Combine multiple PDF files into one document
- **✂️ Split PDFs** - Extract individual pages or groups of pages (outputs as ZIP)
- **🗑️ Remove Pages** - Delete specific pages using flexible range syntax
- **🗜️ Compress PDFs** - Reduce file size through content stream compression
- **🔄 Rotate Pages** - Rotate specific pages or all pages (90°, 180°, 270°)
- **📝 Extract Text** - Pull out all text content from PDF documents
- **💧 Add Watermark** - Add customizable text watermarks with opacity control
- **🔀 Rearrange Pages** - Reorder pages in any sequence you want

### 🎯 Key Benefits
- **No Authentication Required** - Pure local processing
- **User-Friendly Interface** - Clean Gradio web UI with tabbed layout
- **Flexible Input Parsing** - Smart handling of page ranges and operations
- **Error Handling** - Comprehensive error messages and status feedback
- **Google Colab Ready** - Optimized for cloud environments
- **Cross-Platform** - Works on any system with Python

## 🚀 Quick Start

### Option 1: Google Colab (Recommended)
1. Open [Google Colab](https://colab.research.google.com/)
2. Copy and paste the entire code into a new cell
3. Run the cell - packages will install automatically
4. Click the generated public link to access your PDF toolkit

### Option 2: Local Installation
```bash
# Clone the repository
git clone https://github.com/yourusername/pdf-toolkit.git
cd pdf-toolkit

# Install dependencies
pip install gradio PyPDF2 reportlab

# Run the application
python pdf_toolkit.py
```

Access the interface at `http://127.0.0.1:7860`

## 📦 Dependencies

- **gradio** - Web interface framework
- **PyPDF2** - PDF manipulation library
- **reportlab** - PDF generation and watermarking

## 💡 Usage Examples

### Page Range Syntax
- **Remove pages**: `1,3,5-7` (removes pages 1, 3, and pages 5 through 7)
- **Rotate pages**: `all` (all pages) or `1,3-5` (specific pages)
- **Rearrange**: `3,1,4,2` (reorder: page 3 first, then 1, then 4, then 2)

### Split Options
- Set **Pages per split** to `1` for individual pages
- Set to higher numbers for groups (e.g., `3` creates 3-page chunks)

### Watermark Settings
- **Text**: Any custom text (e.g., "CONFIDENTIAL", "DRAFT")
- **Opacity**: `0.1` (very light) to `1.0` (fully opaque)
- **Positioning**: Automatically centered and rotated 45 degrees

## 🔧 Technical Details

### Architecture
- **Backend**: Python with PyPDF2 for PDF operations
- **Frontend**: Gradio for the web interface
- **File Handling**: Temporary files with automatic cleanup
- **Error Management**: Comprehensive try-catch with user-friendly messages

### Supported Operations
- All operations use 1-based page numbering
- Range syntax supports commas and hyphens
- File downloads are handled automatically
- Memory-efficient processing for large PDFs

## 🛠️ Development

### Project Structure
```
pdf-toolkit/
├── pdf_toolkit.py          # Main application file
├── README.md              # This file
└── requirements.txt       # Dependencies list
```

### Contributing
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Extending Functionality
The `PDFToolkit` class is designed for easy extension. Each operation is a separate method that:
- Takes file inputs and parameters
- Returns `(output_path, status_message)` tuple
- Handles errors gracefully
- Uses temporary files for processing

## ⚠️ Limitations

- **Memory**: Large PDFs (>100MB) may cause issues in constrained environments
- **Session**: Colab sessions expire after inactivity
- **Temporary Files**: Files are not permanently stored
- **Complex PDFs**: Some advanced PDF features may not be fully preserved

## 🔒 Privacy & Security

- **No Cloud Storage** - All processing happens locally or in your Colab session
- **No Authentication** - No user accounts or data collection
- **Temporary Processing** - Files are automatically cleaned up after operations
- **Open Source** - Complete transparency in code and operations

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## UI Sample

![Screenshot_14-9-2025_81234_colab research google com](https://github.com/user-attachments/assets/90589f29-2178-4256-9322-f14c827580ff)


## 🐛 Issues & Support

If you encounter any issues or have suggestions:

1. Check the [Issues](https://github.com/piyushpawar77/pdf-toolkit/issues) page
2. Create a new issue with:
   - Clear description of the problem
   - Steps to reproduce
   - Expected vs actual behavior
   - Your environment details

## 🌟 Star History

If you find this project helpful, please consider giving it a star! ⭐

---

**Made with ❤️ for the PDF manipulation community**
