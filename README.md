# 📱 "My Fairy Tale" — A Mobile Application for Parents to Record Fairy Tales

Welcome! This is my pet project — an Android application for parents and children that allows users to record and listen to fairy tales, both audio and text-based, while an integrated AI analyzes the content and determines whether it is safe for children.

The original idea for this project was part of my dissertation, although most of the functionality is unrelated to the dissertation itself and was implemented out of personal interest.

A recorded fairy tale is sent to the server, where its safety is checked. If the story is considered safe, it is stored in the database.
[Backend Repository](https://github.com/Kugukov/DissertationBackend)
  
## 🧠 Main Idea

The project combines:
- Recording and playback of fairy tales
- Synchronization with a server
- AI-based analysis of text and audio for potentially harmful content (profanity, violence, etc.)
- Role separation: parent (password protected) and child (no password)
- An individual fairy tale database for each device  
  


## 🛠 Technologies

#### Android
* Kotlin / Jetpack Compose (Compose, ViewModel, Navigation)
* Coil
* Retrofit
* Hilt
#### Server
* Python
* Flask
* speech_recognition
* SQLite 
   

## 📲 Screenshots (Demo)

<img src="screenshots/HomeScreen.jpg" height="400"/>
<img src="screenshots/TalesLists.jpg" height="400"/>
<img src="screenshots/CreateEditScreens.jpg" height="400"/>
<img src="screenshots/Alerts.jpg" height="400"/>


## 🔧 Main Features

* 🎙 Record fairy tales in `.wav` format
* 📤 Upload audio recordings to the server for analysis
* 🧠 AI detects potentially harmful content and warns the user
* 🗂 Separate fairy tale lists for parents and children
* 🔒 Access restrictions: only the parent account is password-protected
* 🔄 Update and delete recordings  


## Current Limitations
- The application currently does not work without the server
- The server is implemented only as a local deployment
- The database uses SQLite on the server side, which is not suitable for high-performance production use
- There is no password recovery functionality   
  
<!-- 
## 📁 Project structure
```
📦 app/
 ┣ 📂 ui/
 ┃ ┣ 📜 CreateAudioTaleScreen.kt
 ┃ ┣ 📜 TaleListScreen.kt
 ┃ ┗ ...
 ┣ 📂 viewmodel/
 ┣ 📂 model/
 ┣ 📂 network/
 ┣ 📜 MainActivity.kt
```

---
-->

## 🧪 Example of AI Usage

1. A parent records a fairy tale
2. The fairy tale is sent to the server as a `.wav` file
3. The server transcribes and analyzes the audio
4. If harmful words or content are detected:
   * A warning message is displayed
   * The fairy tale is deleted  
  

## 🔐 Security

* Access to parent-only features is protected by a password (SharedPreferences)
* Each device has its own fairy tale database
* Fairy tales are not publicly available  


## 🧩 Possible Improvements

* Use an AI model specifically trained to detect unsafe children's content (currently such models are not available for Russian)
* ПTranslate the entire application into English to use more suitable AI models 
* Add password recovery functionality
* Implement cloud storage for fairy tales / redesign the database architecture and use the server only for content verification and caching (e.g., Redis)
* Apply MVVM and Clean Architecture principles more consistently  


## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
