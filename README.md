
# ANPR-Based Stolen Vehicle Detection System

## 📌 Project Overview
This project implements an **Automatic Number Plate Recognition (ANPR) system** for detecting stolen vehicles using **YOLOv8** for license plate detection and **EasyOCR** for text recognition. The system is integrated with **FastAPI** and **MySQL** to store vehicle data and send alerts to authorities when a stolen vehicle is detected.

---
## 🔥 Features
- **License Plate Detection**: Uses YOLOv8 for real-time number plate detection.
- **OCR for Text Extraction**: EasyOCR extracts characters from detected plates.
- **Stolen Vehicle Detection**: Cross-checks recognized plates against a MySQL database.
- **FastAPI Integration**: Provides a REST API for vehicle data management.
- **Real-Time Alerts**: Sends alerts to authorities when a stolen vehicle is detected.

---
## 🏗️ Tech Stack
- **Deep Learning**: YOLOv8 (License Plate Detection), EasyOCR (OCR for Text Extraction)
- **Backend**: FastAPI
- **Database**: MySQL
- **Libraries**: OpenCV, Ultralytics YOLO, Tesseract OCR

---
## ⚙️ Setup & Installation
### 1️⃣ Clone the Repository
```sh
git clone https://github.com/your-username/anpr-stolen-vehicle.git
cd anpr-stolen-vehicle
```

### 2️⃣ Create a Virtual Environment
```sh
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3️⃣ Install Dependencies
```sh
pip install -r requirements.txt
```

### 4️⃣ Download Pretrained YOLOv8 Model
```sh
mkdir models
wget -O models/yolov8n-license-plate.pt https://github.com/ultralytics/assets/releases/download/v8.0/yolov8n-license-plate.pt
```

### 5️⃣ Configure MySQL Database
- Create a MySQL database:
```sql
CREATE DATABASE anpr_db;
```
- Update `config.py` with database credentials.

### 6️⃣ Run the FastAPI Server
```sh
uvicorn main:app --reload
```

---
## 🚀 API Endpoints
| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/upload` | Uploads an image for ANPR processing |
| `GET`  | `/vehicles` | Retrieves stored vehicle records |
| `POST` | `/add-vehicle` | Adds a new vehicle to the database |
| `DELETE` | `/remove-vehicle/{plate}` | Removes a vehicle by plate number |

---
## 🎯 Future Work
- **🚀 UPI-Based Toll Collection**: Extend the project to enable automatic toll collection.
- **📡 Police Alert System**: Implement real-time alerts for stolen vehicles via SMS or Email.
- **📊 Dashboard**: Build a web dashboard for viewing ANPR logs and reports.

---
## 💡 Contributing
Feel free to open issues and contribute to this project via Pull Requests.

---
## 🏆 Credits
Developed by [Sivaram J](https://github.com/Sivaramjallu001)
