
# 📔 DIARY - Your Teaching Assistant

## A Simple Digital Diary for Teachers

---

## 📖 About the App

**DIARY** is a lightweight, offline Android application designed specifically for teachers to manage their daily teaching activities. It helps teachers organize classes, assign homework, track due dates, and generate professional PDF documents for students.

**No internet connection required.** No complicated setup. Just open, sign up once, and start using.

---

## ✨ Features

### For Teachers

| Feature | Description |
|---------|-------------|
| **One-Time Signup** | Register with name, school, contact, email, address, and subject |
| **Manage Classes** | Add, edit, and delete unlimited classes with section and optional notes |
| **Homework Tasks** | Add, edit, view, and delete homework tasks for each class |
| **Calendar Date Picker** | Select due dates easily with built-in calendar |
| **PDF Generation** | Generate professional PDF for any homework task |
| **File Name Format** | `TaskTitle-Date.pdf` (e.g., `Algebra_Problems-2026-06-14.pdf`) |
| **PDF Content** | Includes class name, task title, description, due date, teacher name, school name, and page number |
| **View Profile** | See all your registered information |
| **Edit Profile** | Update any information anytime |
| **Delete All Data** | Reset app completely with one click |

### For School Management

| Benefit | Description |
|---------|-------------|
| **Standardization** | All teachers follow the same homework format |
| **Transparency** | Clear records of all assigned homework |
| **No Paper Waste** | Digital homework distribution |
| **Offline First** | Works anywhere, no internet dependency |
| **Privacy** | All data stays on teacher's device |

---

## 📱 Screens Overview

| Screen | Purpose |
|--------|---------|
| **Splash Screen** | App logo with progress bar, auto-navigation |
| **Signup Screen** | First-time teacher registration |
| **Dashboard** | Class list, add class button, teacher name, school name |
| **Homework Screen** | Task list, add/edit/delete tasks, PDF generation |
| **View Task Dialog** | Read-only task details |
| **Settings** | View profile, edit profile, about app, about developer, delete data |
| **About App** | Version info, features, tech stack |
| **About Developer** | Developer contact with clickable links |

---

## 🛠️ Technical Stack

| Technology | Purpose |
|------------|---------|
| **Language** | Java |
| **UI Framework** | XML with Material Design |
| **Database** | SQLite |
| **PDF Generation** | Android PdfDocument API |
| **Minimum SDK** | API 24 (Android 7.0 Nougat) |
| **Target SDK** | API 34 (Android 14) |


## 📁 Project Structure

app/src/main/java/com/example/diary/ <br>
│ <br>
├── 📁 activities (9 files) <br>
│ ├── Splash.java <br>
│ ├── Signup.java <br>
│ ├── Dashboard.java <br>
│ ├── Homework.java <br>
│ ├── Settings.java <br>
│ ├── ViewProfile.java <br>
│ ├── EditProfile.java <br>
│ ├── AboutApp.java <br>
│ └── AboutDeveloper.java <br>
│ <br>
├── 📁 adapters (2 files) <br>
│ ├── ClassAdapter.java <br>
│ └── HomeworkAdapter.java <br>
│ <br>
├── 📁 models (2 files) <br>
│ ├── Class.java <br>
│ └── Mhomework.java <br>
│ <br>
├── 📁 utils (1 file) <br>
│ └── PdfGenerator.java <br>
│ <br>
├── 📄 DatabaseHelper.java <br>
│ <br>
└── 📄 (other configuration files) <br>

## 🗄️ Database Schema

### Teacher Table

| Column | Type |
|--------|------|
| id | INTEGER PRIMARY KEY |
| name | TEXT NOT NULL |
| school_name | TEXT NOT NULL |
| contact | TEXT NOT NULL |
| email | TEXT NOT NULL |
| address | TEXT NOT NULL |
| subject_special | TEXT NOT NULL |
| registered_at | DATETIME |

### Classes Table

| Column | Type |
|--------|------|
| id | INTEGER PRIMARY KEY |
| class_name | TEXT NOT NULL |
| section | TEXT NOT NULL |
| note | TEXT |
| created_at | DATETIME |

### Homework Table

| Column | Type |
|--------|------|
| id | INTEGER PRIMARY KEY |
| class_id | INTEGER FOREIGN KEY |
| title | TEXT NOT NULL |
| description | TEXT NOT NULL |
| due_date | TEXT NOT NULL |
| created_at | DATETIME |

## 🔧 Installation

### Prerequisites

- Android Studio Flamingo or newer
- JDK 11 or newer
- Android SDK (API 21 to API 34)

### Steps

1. **Clone or download the project**

2. **Open in Android Studio**
   - File → Open → Select project folder

3. **Sync Gradle**
   - Click "Sync Now" when prompted

4. **Build the project**
   - Build → Make Project

5. **Run on device/emulator**
   - Select device → Click Run button

---

## 📦 Building APK

### Debug APK


Build → Build Bundle(s) / APK(s) → Build APK(s)


### Release APK (Signed)

1. Build → Generate Signed Bundle / APK
2. Select APK
3. Create new keystore or use existing
4. Fill keystore information
5. Select release build variant
6. Finish

The APK will be generated at: `app/build/outputs/apk/release/`

---

## 📱 Compatibility

| Android Version | API Level | Status |
|-----------------|-----------|--------|
| Android 5.0 | 21 | ✅ Supported |
| Android 6.0 | 23 | ✅ Supported |
| Android 7.0 | 24 | ✅ Supported |
| Android 8.0 | 26 | ✅ Supported |
| Android 9.0 | 28 | ✅ Supported |
| Android 10 | 29 | ✅ Supported |
| Android 11 | 30 | ✅ Supported |
| Android 12 | 31 | ✅ Supported |
| Android 13 | 33 | ✅ Supported |
| Android 14 | 34 | ✅ Supported |
| Android 15 | 35 | ✅ Supported |
| Android 16 | 36 | ✅ Supported |

---

## 🔒 Permissions

| Permission | Purpose | Required For |
|------------|---------|--------------|
| `WRITE_EXTERNAL_STORAGE` | Save PDF files | Android 9 and below |
| `READ_EXTERNAL_STORAGE` | Read saved PDFs | Android 9 and below |
| `READ_MEDIA_IMAGES` | Media access | Android 13+ |
| `READ_MEDIA_VIDEO` | Media access | Android 13+ |

> **Note:** Android 10+ uses MediaStore API and does NOT require storage permissions.

---

## 👨‍💻 Developer

| Name | Syed Muhammad Sajawal Hussain |
|------|-------------------------------|
| **Role** | Android Developer |
| **Email** | syedmuhammadsajawalhussain@gmail.com |
| **Phone** | 0328-0841432 |
| **GitHub** | [SyedMuhammadSajawalHussain](https://github.com/SyedMuhammadSajawalHussain) |
| **LinkedIn** | [syed-muhammad-sajawal-hussain](https://www.linkedin.com/in/syed-muhammad-sajawal-hussain-a656283ba) |

---

## 📝 Version History

| Version | Date | Changes |
|---------|------|---------|
| 1.0 | June 2026 | Initial release |
| 1.1 | July 2026 | Added edit task, improved PDF formatting |

---

## 📄 License

This project is proprietary and confidential.

---

## 🙏 Acknowledgments

- Android SDK Documentation
- Material Design Guidelines
- SQLite Documentation

---

## 📞 Support

For questions, feedback, or support:

- **Email:** syedmuhammadsajawalhussain@gmail.com
- **Phone:** 0328-0841432

---

## 🚀 Future Roadmap

- [ ] Dark mode support
- [ ] Backup/Restore data
- [ ] Export all homework to CSV
- [ ] Homework reminders/notifications
- [ ] Share PDF directly from app
- [ ] Multiple teacher profiles
- [ ] Cloud sync (optional)

---

**DIARY - Your Teaching Assistant.** 📔

---
