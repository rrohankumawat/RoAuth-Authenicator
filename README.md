# 🔐 ASP.NET Core (.NET 8) - RoAuth Authenticator with TOTP (2FA)

Live Url: https://www.tinyurl.com/roauth

Note: Codebased Repository is Private.

This is a modular and secure authentication system built with **ASP.NET Core (.NET 8)**. It features standard authentication (login, registration, forgot/reset password) along with **Two-Factor Authentication (2FA)** using **TOTP (Time-based One-Time Passwords)** and a scannable QR code.

---

## 🚀 Features

- ✅ User Registration
- ✅ Login with Username & Password
- ✅ Forgot Password & Reset Password
- ✅ Two-Factor Authentication (2FA) using TOTP
- ✅ QR Code Generation for Authenticator Apps
- ✅ QR Code Displayed on Dashboard Post Login
- ✅ Support for Any TOTP-Based App
- 🔧 Modular Architecture with Clean Code Separation
- ⚙️ Under Active Development

---

## 📱 Works with Any TOTP Authenticator App

The app generates a QR code that can be scanned using **any TOTP-compatible authenticator app**, such as:

- Google Authenticator  
- Microsoft Authenticator  
- Authy  
- 2FAS  
- FreeOTP  
- and more...

> ✅ **Note:** The QR code shown on the dashboard after successful login can be scanned using any app that supports TOTP (RFC 6238).

---

## 🛠️ Technologies Used

- ASP.NET Core 8.0 (MVC)
- Entity Framework Core
- ASP.NET Core Identity
- SQL Server
- Docker Containerisation 
- QRCoder (QR Code Generator)
- Custom TOTP Implementation
- Modular Solution Architecture

---

## 📂 Solution Structure

Your project follows a clean and modular folder structure:

AuthenticatorAppNew.sln → Visual Studio Solution
│
├── AuthenticatorAppNew/ → Main ASP.NET Core MVC project (UI, Controllers, Views)

│
├── Domain/ → Core domain models and business logic

│
├── DTO/ → Data Transfer Objects used between layers

│
├── Repository/ → Data access layer (EF Core/Dapper Repositories)

│
├── Services/ → Application services (Authentication, TOTP logic, etc.)

│
└── Shared/ → Common helpers, utilities, constants, and enums



This structure enables scalability, testability, and separation of concerns using principles of **Clean Architecture** and **SOLID** design.

---

## 🔐 How TOTP Works

1. When a user registers or logs in successfully, a unique secret key is generated.
2. A QR code is generated from this key using `QRCoder`.
3. The user scans the QR code with any TOTP Authenticator App.
4. The app generates a 6-digit TOTP code every 30 seconds.
5. The user submits this code for verification during login.
6. The backend validates the code using the stored secret and the current timestamp.

---


**Clone the repository:**
   ```bash
   git clone https://github.com/rrohankumawat/AuthenticatorWithQr.git


📄 License
This project is licensed under the MIT License.
See the LICENSE file for details.

👨‍💻 Author
Rohan Kumawat
.NET Developer | https://linkedin.com/in/rohankumawat 
📧 rohankumawat.pinkcity@gmail.com
📍 Jaipur, Rajasthan



---

Let me know if you’d like to add GitHub badges (like build status, tech stack, stars), or want help converting this into a downloadable or GitHub-ready format.
