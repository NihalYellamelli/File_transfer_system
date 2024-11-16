# Secure File Sharing System

This is a **Secure File Sharing System** built with **FastAPI**, designed to handle file management for two types of users:

- Ops Users: Can upload specific types of files to the system.
- Client Users: Can sign up, log in, and securely download files shared by Ops users.

The system ensures that files are securely stored and can only be accessed by the appropriate users through encrypted URLs. The project makes use of **JWT (JSON Web Tokens)** for authentication and **role-based access control** to ensure the security of operations.

Key Features:

1. Ops User Capabilities:
- Login: Ops Users can log in using their credentials.
- File Upload: Ops Users can upload files of specific types (e.g., `.pptx`, `.docx`, `.xlsx`). The upload process ensures that only authorized users can upload certain file types.

2. Client User Capabilities:
- Sign Up: Clients can register with the system by providing their username, email, and password.
- Login: Client Users can log in after registration.
- Download Files: After logging in, Client Users can download files that have been shared with them. The system ensures that only authorized users can download the files by generating an **encrypted URL**.
- List Files: Client Users can see a list of files uploaded by Ops Users.

3. Security Features
- JWT Authentication: The system uses JWT tokens for secure authentication. All requests to access protected endpoints require the user to present a valid JWT token.
- Role-based Access Control: The system enforces role-based access control (RBAC). Ops Users can upload files, but only Client Users who have been given access can download them.
- Encrypted URLs: When a file is downloaded, the system generates a **secure URL** that can only be accessed by the Client User who has permission to download it.

4. Technology Stack
- **Backend Framework**: FastAPI
- **Database**: SQLite (can be easily swapped with other databases like PostgreSQL)
- **Authentication**: JWT (JSON Web Tokens)
- **ORM**: SQLAlchemy
- **Password Hashing**: bcrypt
- **Environment Variables**: python-dotenv

Installation: using pip install command

Prerequisites
Make sure you have **Python 3.8+** installed. You'll also need `pip` to install the dependencies.

