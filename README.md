# React App: Firebase Hosting & Realtime Database

A lightweight, production-ready boilerplate for Firebase projects built on Vite. This setup includes essential dependencies for modern web development, such as Firebase services and tools.

## Features
- **Vite** for fast development
- **Firebase SDK** for Hosting & Realtime NOSQL Database
- **Environment configuration** via loadEnv

## Installation

1. **Clone & Install the repository**
   ```bash
   git clone https://github.com/asilvafx/firebase-app.git
   cd firebase-app
   npm install

2. **Setup Google Firebase Account**
   ```bash
   Sign in or create a new account at, https://console.firebase.google.com/ 
   Create new project
   Add Firebase to your web app
   (Optional) Check the option "Also set up Firebase Hosting for this app", if you wish to setup a hosting for your web app.
   Copy your Firebase configuration
   Update the configuration in your .env-sample at your root directory
   Rename the .env-sample to .env

3. **Edit Realtime Database "Rules" in your Firebase Console**
   ```bash 
   {  "rules": {
    ".read": "now < 1735772400000",  // 2025-1-2
    ".write": "now < 1735772400000",  // 2025-1-2 
	  "users": {
      ".indexOn": ["uid", "email"]
   } } }

3. **Development**
   ```bash
   npm run dev

4. **(Optional, Hosting) Install Firebase CLI**
   ```bash
   npm install -g firebase-tools
   firebase login
   firebase init hosting

5. **Build**
   ```bash
   npm run build
   (Optional, Hosting) Run, firebase deploy