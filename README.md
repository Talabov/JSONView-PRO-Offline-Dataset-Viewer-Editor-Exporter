# 🧩 JSONView PRO — Offline Dataset Viewer, Editor & Exporter

**JSONView PRO** is a self-hosted **data management suite** built with **FastAPI + Jinja2 + Pandas + ReportLab**.  
It runs entirely **offline**, giving you full control over your data — no cloud, no telemetry, no sync.  
View, edit, and export any local `.json` or `.csv` file through a clean, modern web interface.

---

## ✅ Key Features

- 📂 **Dataset browser** — automatically detects and loads local JSON/CSV files  
- ✏️ **Built-in JSON/CSV editor** — view, edit, and re-save datasets directly in the browser  
- 💾 **Save / Save As...** — overwrite or duplicate datasets into the `/data` directory  
- 📄 **Export Engine** — generate elegant **PDF** or **HTML** reports instantly  
- 🧠 **Smart JSON parser** — auto-flattens nested data structures for readability  
- 🎨 **Dark & light themes** with glass-blur topbar  
- 🔒 **100% offline operation** — no external APIs or network dependencies  
- 🪟 **One-click launch scripts** for Windows, macOS, and Linux  
- 🐳 **Docker-ready** for easy deployment  

---

## 📂 Project Structure

```
C:.
│   .dockerignore
│   docker-compose.yml
│   Dockerfile
│   LICENSE
│   main.py
│   README.md
│   requirements.txt
│   run.py
│   start_linux.sh
│   start_macos.sh
│   start_windows.bat
│
├───api
│       chart_export.py
│       convert.py
│       dataset.py
│       export.py
│       info.py
│       meta.py
│       mock.py
│       schema.py
│       __init__.py
│
├───core
│       auth.py
│       charts.py
│       config.py
│       converter.py
│       exporter.py
│       loader.py
│       mocker.py
│       watcher.py
│       __init__.py
│
├───data
│       employees-10-level_5MB.json
│       example.csv
│
├───screens
│       1 start server.png
│       2 dashboard .png
│       3 csv json.png
│       4 edit .png
│       5 upload .png
│       6 export .png
│       7 html export.png
│       8 dark theme.png
│
├───static
│       app.js
│       style.css
│       uploader.js
│
└───templates
        base.html
        export.html
        index.html
        login.html
        register.html
        upload.html
```

---

## 🌐 Main Routes

| URL | Description |
|-----|--------------|
| `/` | Dashboard showing available datasets |
| `/upload` | Upload new JSON/CSV files |
| `/export` | Export datasets to PDF or HTML |
| `/api/list` | Get all dataset names |
| `/api/{dataset}` | Fetch dataset data (JSON) |
| `/api/save_dataset` | Overwrite existing dataset |
| `/api/save_dataset_as` | Save dataset as a new file |
| `/login` / `/register` | Simple user auth pages |

---

## ⚙️ Requirements

Install all dependencies:
```bash
pip install -r requirements.txt
```

### Core dependencies
- fastapi  
- uvicorn  
- pandas  
- jinja2  
- reportlab  
- python-multipart  
- watchdog  

---

## 🚀 Run Locally

### 🪟 Windows
```bat
start_windows.bat
```

### 🍎 macOS
```bash
chmod +x start_macos.sh
./start_macos.sh
```

### 🐧 Linux
```bash
chmod +x start_linux.sh
./start_linux.sh
```

Once started, open:  
👉 [http://127.0.0.1:8000](http://127.0.0.1:8000)

---

## 🐳 Run with Docker

### Build and start:
```bash
docker compose up --build
```

or manually:
```bash
docker build -t jsonview-pro .
docker run -p 8000:8000 jsonview-pro
```

Open in your browser:  
[http://127.0.0.1:8000](http://127.0.0.1:8000)

---

## 🧠 JSON/CSV Editor

| Feature | Description |
|----------|-------------|
| **Edit** | Opens dataset in full-width text editor |
| **Save** | Overwrites the original dataset |
| **Save As...** | Creates a new dataset in `/data` |
| **Cancel** | Closes editor without saving |
| **Format detection** | Works for both JSON and CSV automatically |

---

## 📄 Export Engine

- Generates **dark modern PDF reports** (two cards per page)  
- Auto-formats nested JSON structures (Contact, Location, Skills, Projects)  
- Built-in headers, timestamps, and dataset info  
- Supports **HTML export** for lightweight sharing  

---

## 💻 UI Features

- Glass-blur navigation bar with transparency (55%)  
- Responsive dashboard layout  
- Dark/light mode toggle with persistence  
- Clean typography and balanced spacing  

---

## 🧾 Example Screens

| Screenshot | Description |
|-------------|-------------|
| `1 start server.png` | Starting the server |
| `2 dashboard .png` | Dataset dashboard |
| `3 csv json.png` | Viewing CSV/JSON data |
| `4 edit .png` | JSON editor view |
| `5 upload .png` | Upload interface |
| `6 export .png` | Export panel |
| `7 html export.png` | HTML report example |
| `8 dark theme.png` | Dark mode preview |

---

## 💼 Ready-to-Use Package

Includes:
- All API + frontend modules  
- `/data` workspace for datasets  
- One-click startup scripts  
- Full PDF/HTML export engine  

Perfect for developers, analysts, and teams who need a **local-first data viewer**.

---

## 📬 Support

**Email:** talabov.ali72@gmail.com  
**Telegram:** [@talabovali](https://t.me/talabovali)

---

💡 **JSONView PRO** — Local, private, and powerful.  
_Your data stays where it belongs — on your machine._
