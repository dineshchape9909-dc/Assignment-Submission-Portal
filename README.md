# Assignment Submission Portal

A local desktop application built using Python and Tkinter designed for managing student assignment uploads and facilitating real-time teacher grading. This application operates entirely locally, utilizing a JSON-based file system to preserve submission tracking metrics and file references securely.

## 🚀 Features

### For Students
- **Information Profiling**: Inputs for Student Name, Roll Number, and Subject.
- **Robust File Uploader**: Interactive document browser supporting `.pdf`, `.doc`, `.docx`, `.txt`, `.ppt`, and `.pptx` files.
- **Unique Submission Receipts**: Generates short, cryptographically randomized 8-character Submission IDs using UUID generation for reference tracking.
- **Result Verification Dashboard**: Look up comprehensive evaluation notes and numerical grading using a student's unique Roll Number.

### For Teachers
- **Protected Session Access**: Authenticated dashboard using a secure supervisor passcode.
- **Submission Registry**: Full data visualization via a multi-column sorting-ready UI table (`Treeview`).
- **Dynamic File Ingestion**: Instant programmatic launch triggers that let you view and open files directly in native system apps (Acrobat, MS Word, etc.).
- **Evaluation Sandbox**: Fast assignment of custom scores (0–100 numerical standard) and personalized long-form feedback strings.

---

## 🛠️ Architecture & Technologies

- **Language**: Python 3.x
- **GUI Ecosystem**: Tkinter + Built-in `ttk` (Themed Widgets) for modernized window styling.
- **Database Engine**: Flat-file JSON structure (`assignments.json`) providing structural schemas without requiring high-maintenance SQL/NoSQL platforms.
- **File Management**: `shutil` API handling secure local copy operations and `pathlib` enforcing explicit OS-agnostic folder pathways.

---

## 📂 Project Structure

```text
assignment-portal/
│
├── main.py               # Main application source code
├── assignments.json      # Structured persistent database records (Auto-generated)
└── uploads/              # Local storage repository for submitted documents (Auto-generated)
```

---

## ⚙️ Setup and Installation

### Prerequisites
Make sure your machine runs an active distribution of Python 3.7 or higher.

### Running the App
1. **Clone the repository:**
   ```bash
   git clone https://github.com
   cd assignment-submission-portal
   ```

2. **Execute the script:**
   No external pipeline components (`pip`) are required. Simply boot the built-in Tkinter application framework using your shell terminal:
   ```bash
   python main.py
   ```

---

## 🔒 Security Configuration

> [!WARNING]
> This application is configured with a default password for classroom demonstration purposes.

To change the default teacher dashboard password, open `main.py` and modify the global variable value at line 20:

```python
# -------------------- CONFIGURATION --------------------
TEACHER_PASSWORD = "your-custom-secure-password"
```

## 📜 License
Distributed under the MIT License. Feel free to fork and customize for classroom setups or academic project evaluations!
