<h1 align="center">Multimodal-Biometric-Voting-System-_BE-Project</h1>

http://127.0.0.1:8000/docs

## Biometric Voting System - Project Documentation

### Project Overview

This is a secure biometric voting system that uses Android fingerprint authentication for voter registration, authentication, and vote casting. The system consists of a React Native mobile application and a Python FastAPI backend server.

### Technologies Used

#### Mobile Application

* React Native – Cross-platform mobile framework
* Expo SDK 50.0.0 – Development and build tooling
* expo-local-authentication – Android fingerprint sensor integration
* AsyncStorage – Local data caching on mobile device
* JavaScript / React – Programming language and UI framework

#### Backend Server

* Python 3.8+
* FastAPI
* Uvicorn
* Pydantic
* JSON Storage (votes.json, voters.json)

#### Build Tools (Android)

* Gradle 8.3
* Java 17 (Eclipse Adoptium)
* Android SDK 34
* Android NDK 25.1.8937393
* ADB (Android Debug Bridge)

### System Architecture

The system consists of three main components:

1. **Mobile App (Frontend)**

   * User interface for voters
   * Fingerprint authentication
   * API communication
   * Local storage using AsyncStorage

2. **Backend API (Server)**

   * Voter registration validation
   * Authentication management
   * Vote recording
   * Results generation

3. **Android Device**

   * Fingerprint sensor
   * Secure biometric storage
   * Network connectivity

### Key Features

* Fingerprint-based voter authentication
* Secure voter registration
* Anonymous vote casting
* Duplicate vote prevention
* FastAPI backend integration
* React Native mobile application
* JSON-based data storage

### Security Features

* Fingerprint data never leaves the Android device
* Android BiometricPrompt API integration
* Separate voter and vote records
* Duplicate voting prevention
* Request validation using Pydantic

### Project Structure

```text
Biometric_voting_system/
│
├── mobile/
├── admin/
├── api.py
├── requirements.txt
├── votes.json
├── voters.json
└── README.md
```

### Installation

#### Backend

```bash
pip install -r requirements.txt
python -m uvicorn api:app --host 0.0.0.0 --port 8000 --reload
```

#### Mobile Application

```bash
cd mobile
npm install
npx expo run:android --device
```

### API Endpoints

| Method | Endpoint      | Description        |
| ------ | ------------- | ------------------ |
| GET    | /             | Health Check       |
| POST   | /register     | Register Voter     |
| POST   | /authenticate | Authenticate Voter |
| POST   | /vote         | Cast Vote          |
| GET    | /results      | View Results       |

### Future Enhancements

* Face Recognition Authentication
* OTP Verification
* HTTPS Security
* Database Integration (MySQL/PostgreSQL)
* Admin Dashboard
* Real-Time Election Monitoring
* End-to-End Vote Encryption

### Project Status

**Status:** Functional Prototype
**Platform:** Android + FastAPI Backend
**Authentication:** Fingerprint-Based Biometric Verification
**Academic Project:** BE Final Year Project
