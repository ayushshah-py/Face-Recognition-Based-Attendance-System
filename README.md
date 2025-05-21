# 🎓 Face Recognition-Based Attendance System

Welcome to the **Face Recognition-Based Attendance System**, an innovative and automated solution for managing attendance using cutting-edge face recognition technology. Built with **Python** and the powerful **Django web framework**, this project replaces the outdated manual methods with a modern, fast, and secure system that recognizes faces in real-time to mark attendance efficiently and accurately.

## 📘 Table of Contents

- [About the Project](#about-the-project)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Project Architecture](#project-architecture)
- [How It Works](#how-it-works)
- [Installation and Setup](#installation-and-setup)
- [Usage Instructions](#usage-instructions)
- [Screenshots](#screenshots)
- [Future Enhancements](#future-enhancements)
- [Known Issues](#known-issues)
- [Contributing](#contributing)
- [Author](#author)
- [License](#license)

---

## 📖 About the Project

This project aims to **eliminate traditional paper-based and manual attendance systems** by automating the entire process using facial recognition. It leverages advanced computer vision and machine learning algorithms to identify and authenticate students or employees from a live video stream.

Whether you're managing attendance in a **classroom**, **corporate setting**, **lab**, or **event**, this system provides a scalable and user-friendly solution. The admin can register new individuals, capture their face data, and monitor attendance records all through a secure web-based interface.

---

## ✨ Features

- ✅ **Real-time Face Detection** using OpenCV and Dlib
- ✅ **Face Recognition Matching** using deep learning-based face encodings
- ✅ **Auto Attendance Marking** once a known face is detected
- ✅ **Web Dashboard for Admins**
  - Add/update/delete student data
  - Upload face images
  - View attendance records
- ✅ **Date-Wise and Student-Wise Reports**
- ✅ **Student Registration via Webcam or File Upload**
- ✅ **Secure Login System for Administrators**
- ✅ **Data Persistence with Django ORM**
- ✅ **Mobile and Desktop Responsive UI**
- ✅ **Scalable Database Architecture**

---

## 🧰 Technology Stack

| Category          | Tech Used                                |
|-------------------|-------------------------------------------|
| **Frontend**       | HTML5, CSS3, JavaScript, Bootstrap       |
| **Backend**        | Python, Django Web Framework              |
| **Face Recognition**| `face_recognition`, `OpenCV`, Dlib      |
| **Database**       | SQLite (can be switched to PostgreSQL/MySQL) |
| **Authentication** | Django's built-in User model             |
| **Tools**          | NumPy, Pillow, Virtualenv                |

---

## 🏗️ Project Architecture

```

face\_attendance/
├── attendance/                  # Django app for attendance system
│   ├── templates/               # HTML templates
│   ├── static/                  # Static files (CSS, JS, images)
│   ├── migrations/              # Database migration files
│   ├── **init**.py
│   ├── admin.py                 # Admin site configuration
│   ├── apps.py
│   ├── models.py                # Database models
│   ├── views.py                 # Core logic for face detection & attendance
│   ├── urls.py
│   └── forms.py
│
├── face\_attendance/            # Project settings and config
│   ├── **init**.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
│
├── media/                      # Face images storage
├── db.sqlite3                  # SQLite Database
├── manage.py                   # Django CLI entry
├── requirements.txt
└── README.md

````

---

## ⚙️ How It Works

1. **Student Registration**  
   The admin registers a new student, inputs their details, and uploads or captures a clear face image. The system then encodes the face and stores it in the database.

2. **Face Encoding**  
   Using the `face_recognition` library, the uploaded face image is converted into a unique numerical encoding vector for identification.

3. **Live Detection**  
   When attendance is being marked, the webcam feed is continuously scanned. Detected faces are compared to known encodings using Euclidean distance.

4. **Attendance Marking**  
   If a match is found, the attendance is marked in the database with date, time, and student details. Duplicate entries for the same session are avoided.

5. **Reports & Dashboard**  
   Admin can log in, view historical attendance logs, and filter reports by student or date.

---

## 🖥️ Installation and Setup

### Step 1: Clone the Repository

```bash
git clone https://github.com/yourusername/face-attendance.git
cd face-attendance
````

### Step 2: Create Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
```

### Step 3: Install Required Packages

```bash
pip install -r requirements.txt
```

### Step 4: Apply Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

### Step 5: Create Superuser

```bash
python manage.py createsuperuser
```

### Step 6: Run the Server

```bash
python manage.py runserver
```

Now open your browser and go to: [http://127.0.0.1:8000](http://127.0.0.1:8000)

---

## 🎮 Usage Instructions

* Go to `/admin` and log in using superuser credentials.
* Add new students via the dashboard.
* Navigate to the camera capture interface to start a live session.
* Detected and recognized faces will be marked as present automatically.
* Go to the "Attendance Logs" page to download/view the attendance report.

---

## 🖼️ Screenshots (Optional)

*Add screenshots showing:*

* Admin login
* Student registration
* Face detection in action
* Attendance report page

---

## 📌 Known Issues

* Faces must be well-lit and clearly visible for accurate detection
* Multiple faces in one frame may confuse the recognizer
* Not optimized for low-end hardware
* Webcam may lag with poor processing speed

---

## 🚧 Future Enhancements

* PDF/CSV export of attendance records
* Email notifications to absentees
* Multiple camera/device support
* Facial spoof detection (mask detection)
* API for mobile integration
* Face training automation pipeline
* Integration with RFID or biometric systems

---

## 🤝 Contributing

Contributions are welcome!

To contribute:

1. Fork this repo
2. Create a new branch: `git checkout -b feature-name`
3. Commit your changes: `git commit -m 'Add feature'`
4. Push to the branch: `git push origin feature-name`
5. Create a Pull Request

## 👨‍💻 Author

**Ayush Shah**
📧 Email: \[[your.email@example.com](mailto:ayushs1904@gmail.com)]
💼 LinkedIn: \[linkedin.com/in/yourprofile] *(Optional)*
## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.
## 🙏 Acknowledgements

* [`face_recognition`](https://github.com/ageitgey/face_recognition)
* Django community and documentation
* Bootstrap for responsive UI
