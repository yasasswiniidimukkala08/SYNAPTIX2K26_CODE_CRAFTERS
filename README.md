# 🚨 RescueNet – AI-Powered Emergency Response System

RescueNet is a multi-sensor intelligent emergency detection and response system built using **Expo + React Native + Firebase**.

It automatically detects accidents using motion + sound analysis and instantly alerts nearby responders with real-time location tracking.

---

## 🧠 Problem Statement

In real-world emergencies:

* Victims may be unconscious
* Hands may be immobile
* Phones may be inaccessible
* Manual SOS apps become useless

Most safety apps rely on user interaction.

RescueNet removes that dependency.

---

## ⚡ Core Features

### 1️⃣ Multi-Sensor Accident Detection

* Free-fall detection using Accelerometer
* Impact detection via motion magnitude
* Loud acoustic spike detection using audio metering
* Sensor fusion logic (Fall + Sound) to reduce false positives

### 2️⃣ Automatic SOS Trigger

If both:

* Fall detected
* Loud impact sound detected

→ High-priority emergency alert is sent automatically.

No user interaction required.

---

### 3️⃣ Voice Guidance (AI Feedback)

When emergency auto-triggers:

> “Emergency detected. Help is being notified. Please stay calm and remain still.”

This provides reassurance if the victim is conscious.

---

### 4️⃣ Manual Emergency Mode

Users can:

* Select emergency type
* Choose priority (Normal / High)
* Send SOS manually

---

### 5️⃣ Real-Time Firestore Alert System

Each SOS includes:

* Victim name
* GPS coordinates
* Emergency type
* Priority status
* Timestamp
* Radius-based responder targeting

---

### 6️⃣ Responder Dashboard

Responders can:

* View nearby alerts
* Navigate to victim
* Mark arrival
* Track live status

---

## 🏗️ Tech Stack

| Layer           | Technology                |
| --------------- | ------------------------- |
| Mobile App      | Expo + React Native       |
| Sensors         | expo-sensors              |
| Audio Detection | expo-av (metering)        |
| Voice Feedback  | expo-speech               |
| Backend         | Firebase Firestore        |
| Routing         | Expo Router               |
| UI              | React Native + Reanimated |
| Haptics         | expo-haptics              |

---

## 🧠 Detection Architecture

```
Accelerometer → Free Fall
        ↓
Impact Magnitude Check
        ↓
Audio Metering Spike Detection
        ↓
Multi-Sensor Validation Engine
        ↓
High Priority SOS Dispatch
        ↓
Voice Confirmation
```

Sensor fusion reduces false positives and improves real-world reliability.

---

## 📂 Project Structure

```
app/
  sos/
    index.tsx        → SOS logic + auto detection
    radar.tsx        → Active emergency view

hooks/
  useFallDetection.ts
  useSoundSpikeDetection.ts
  useShakeDetection.ts

context/
  AppContext.tsx

lib/
  firebase.ts
```

---

## 🚀 How To Run

```bash
npm install
npx expo start
```

Scan the QR using Expo Go.

---

## 🔒 Permissions Required

* Location (Foreground)
* Microphone (Audio metering)
* Motion Sensors

---

## 🎯 What Makes This Different

Unlike traditional SOS apps:

* No button press required
* Works even if user is unconscious
* Multi-sensor validation reduces false alarms
* Provides real-time voice reassurance
* Supports responder coordination

---

## 📌 Future Improvements

* Native Android background service
* Power-button emergency integration
* Continuous live location streaming
* AI audio classification model (TFLite)
* Emergency contact auto-call integration

---

## 👨‍💻 Built For

Hackathons, real-world safety use cases, and intelligent emergency response systems.

---

## 🏆 Vision

RescueNet aims to become a proactive emergency guardian — not just a panic button.

---
