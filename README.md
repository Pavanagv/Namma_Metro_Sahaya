# 🚇 Namma Metro Sahaya

**Namma Metro Sahaya** is an Android app designed to help first-time metro users — especially people from rural areas — navigate the Namma Metro Bengaluru network with ease. The app provides route planning, fare calculation, exit guidance, a visual step-by-step travel guide, and an AI-powered assistant named *Sahaya* that can respond in both English and Kannada.

---

## ✨ Features

- **🗺️ Route Finder** — Find the best route between any two metro stations on the Purple and Green lines, with interchange detection at Majestic (KSR Bengaluru City).
- **💰 Fare & Time Calculator** — Instantly calculate the fare (₹10–₹50) and estimated travel time between any two stations.
- **🚪 Exit Finder** — Locate the right gate/exit at any metro station so you walk out in the right direction.
- **📋 Visual Guide** — Step-by-step illustrated travel guide for first-time users, with Kannada descriptions at each step.
- **🤖 AI Assistant (Sahaya)** — A Gemini-powered chatbot that answers metro-related questions in English or Kannada.
- **🔐 User Authentication** — Firebase-based login and registration with user profile management.
- **🌙 Dark Mode Support** — Light and dark themes supported out of the box.

---

## 🖼️ Screens

| Screen | Description |
|---|---|
| Splash | App launch screen |
| Login / Register | Firebase authentication |
| Home | Search stations + quick-access feature cards |
| Route Finder | Enter source & destination to get route details |
| Fare & Time | Calculate fare and travel duration |
| Exit Finder | Find the right gate at your station |
| Visual Guide | Step-by-step metro journey walkthrough |
| AI Assistant | Chat with Sahaya (Gemini-powered) |
| Profile | View and manage user account info |
| Settings | App preferences |
| About | App and developer info |

---

## 🛠️ Tech Stack

| Category | Technology |
|---|---|
| Language | Kotlin |
| Platform | Android (minSdk 26, targetSdk 34) |
| Build System | Gradle (Kotlin DSL) |
| UI | XML Layouts, ViewBinding, Material Design 3 |
| Authentication | Firebase Auth |
| Analytics | Firebase Analytics |
| AI Chatbot | Google Gemini API |
| Async | Kotlin Coroutines |
| Architecture | Activity-based with ViewModel + LiveData |
| Data | In-app static metro graph (MetroData, MetroGraph) |

---

## 🚀 Getting Started

### Prerequisites

- Android Studio Hedgehog or later
- Android SDK 26+
- A Firebase project with Authentication enabled
- A Google Gemini API key

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/Pavanagv/Namma_Metro_Sahaya.git
   cd Namma_Metro_Sahaya
   ```

2. **Add Firebase configuration**
   - Download `google-services.json` from your Firebase Console
   - Place it inside the `app/` directory

3. **Add your Gemini API key**
   - Open `HomeActivity.kt`
   - Replace the placeholder:
     ```kotlin
     private val GEMINI_API_KEY = "YOUR_GEMINI_API_KEY_HERE"
     ```

4. **Build and run**
   - Open the project in Android Studio
   - Sync Gradle and run on an emulator or physical device

---

## 🗺️ Metro Network Covered

| Line | Route |
|---|---|
| 🟣 Purple Line | Challaghatta ↔ Whitefield (Kadugodi) |
| 🟢 Green Line | Nagasandra ↔ Silk Institute |
| 🔁 Interchange | KSR Bengaluru City — Majestic |

Fare ranges from **₹10 to ₹50** depending on the distance.

---

## 📁 Project Structure

```
NammaMetroSahaya/
├── app/
│   └── src/main/java/com/nammametro/sahaya/
│       ├── adapter/          # RecyclerView adapters (Search, Exit, Step)
│       ├── api/              # Gemini API service
│       ├── data/             # Metro stations, graph, route logic
│       ├── HomeActivity.kt
│       ├── RouteFinderActivity.kt
│       ├── FareActivity.kt
│       ├── ExitFinderActivity.kt
│       ├── VisualGuideActivity.kt
│       ├── AIAssistantActivity.kt
│       ├── LoginActivity.kt
│       ├── RegisterActivity.kt
│       ├── ProfileActivity.kt
│       ├── SettingsActivity.kt
│       └── AboutActivity.kt
├── build.gradle.kts
├── gradle/
│   └── libs.versions.toml
└── settings.gradle.kts
```

---

## 🔒 Permissions

```xml
<uses-permission android:name="android.permission.INTERNET" />
```

Internet access is required for Firebase authentication and the Gemini AI assistant.

---

## 🤝 Contributing

Pull requests are welcome! If you'd like to contribute:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add your feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 👨‍💻 Author

**Pavanagv** — [github.com/Pavanagv](https://github.com/Pavanagv)

---

> *Sahaya (ಸಹಾಯ) means "help" in Kannada — because every first-time commuter deserves a guide.*
