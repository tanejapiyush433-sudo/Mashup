Mashup Generator Web Application

A Python-based web service that generates a mashup from YouTube videos of a selected singer.
The system downloads videos, converts them to audio, trims them, merges into one file, and sends the final mashup to the user's email in ZIP format.

---
 Features

* Enter singer name, number of videos, duration, and email
* Downloads videos from YouTube automatically
* Converts videos to MP3 audio
* Cuts first N seconds from each audio
* Merges all audio into a single mashup
* Sends final mashup ZIP file via email
* Web interface built using Flask

---

Technologies Used

* Python
* Flask (Web framework)
* pytube (YouTube video download)
* pydub (Audio processing)
* FFmpeg (Audio backend)
* smtplib (Email sending)

---

 Project Structure


MashupProject
│── app.py
│── templates
│    └── index.html
│── downloads/
│── audio/
│── cut/
│── output/


---

## ⚙️ Installation & Setup

### 1️⃣ Install Python libraries

Open terminal inside project folder:

```
pip install flask pytube pydub moviepy audioop-lts
```

### 2️⃣ Install FFmpeg (Required)

Download FFmpeg and extract.

Add **bin folder path** to system environment variable PATH.

Check installation:


ffmpeg -version


---

## ▶️ Run the Project

Open terminal in project folder and run:


python app.py


Open browser and go to:


http://127.0.0.1:5000


Fill form and generate mashup.

---

## 📧 Email Configuration

Open `app.py` and update:

EMAIL_SENDER = "yourgmail@gmail.com"
EMAIL_PASSWORD = "your_app_password"


Use Gmail App Password (enable 2-step verification first).

---

 How It Works

1. User enters singer name, number of videos, duration, email
2. Videos downloaded using pytube
3. Converted to MP3 using pydub
4. First N seconds trimmed
5. All audio merged into mashup
6. ZIP file created
7. Sent to user's email automatically




