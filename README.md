# 🎙️ EduSummarize: Automated Lecture Notes & Summarization Using Speech Techniques

**EduSummarize** is an AI-driven system that automatically processes lecture audio and generates structured summaries and bullet-point notes using speech processing and NLP. It aims to improve comprehension, reduce manual effort, and support academic productivity.

---

## 📌 Project Title

**EduSummarize: Automated Lecture Notes & Summarization Using Speech Techniques**

---

## 🎯 Objective

To develop a fully automated pipeline that:
- Converts raw lecture audio into clean transcriptions
- Extracts important segments using prosodic and semantic features
- Generates both extractive and abstractive summaries
- Produces concise, bullet-point notes for study and revision

---

## 🧰 Tech Stack

| Component           | Technology Used                                 |
|---------------------|-------------------------------------------------|
| Audio Preprocessing | Noise reduction, loudness normalization         |
| ASR                 | Whisper (speech-to-text)                        |
| Feature Extraction  | Pitch, energy, jitter, shimmer, MFCC, formants  |
| NLP & Summarization | SBERT, BART-largeCNN, PCA, MMR                  |
| Evaluation          | FKGL, Gunning Fog, SMOG, Cosine Similarity      |
| Deployment (Optional) | Flask (Web Interface)                        |
| Language            | Python                                          |

---

## 🧠 Methodology

### 1. 🎧 Audio Preprocessing
- Converted 6 lectures to 16kHz mono audio
- Applied spectral-gate noise reduction and peak normalization

### 2. 🗣️ Automatic Transcription
- Used Whisper ASR to produce 5,218 time-aligned transcript segments

### 3. 🔍 Segment-Level Feature Extraction
- Computed 34 acoustic and textual features per segment
- Features include: pitch, energy, MFCCs, speech rate, articulation rate, jitter, shimmer

### 4. 📊 Exploratory Data Analysis
- Analyzed trends across pitch, energy, and speech rate
- Visualized feature distributions for lecture variability assessment

### 5. 🧾 Extractive Summarization
- Computed importance scores (energy, pitch, HNR, formant, word count)
- Used SBERT + MMR to extract top 150 sentences preserving diversity

### 6. ✍️ Abstractive Summarization
- Applied BART-largeCNN for paraphrased, narrative-style summaries
- Controlled output using beam search and length penalties

### 7. 📝 Bullet-Point Note Generation
- Ranked segments by acoustic + semantic coherence
- Extracted top 15 key ideas per lecture and converted to notes

### 8. 📏 Evaluation Metrics
| Metric               | Purpose                                           |
|----------------------|--------------------------------------------------|
| Flesch-Kincaid Grade | Measures readability grade level                 |
| SMOG Index           | Predicts education level needed for understanding|
| Gunning Fog          | Accounts for long words and sentence complexity  |
| Semantic Similarity  | Evaluates summary vs original (via SBERT)        |

---

## 💡 Key Features

- ✅ Prosody-aware summarization (pitch, energy, MFCCs)
- ✅ Dual-mode: Extractive + Abstractive summarization
- ✅ Quantitative readability and semantic alignment checks
- ✅ Bullet-point generation with topic diversity control
- ✅ Scalable to multi-lecture datasets

---

## 📊 Results Summary

| Evaluation Aspect       | Highlights                                      |
|--------------------------|------------------------------------------------|
| Readability Scores       | FKGL & SMOG indicated clarity for most lectures |
| Semantic Similarity      | Higher in extractive summaries (~0.9+ cosine)  |
| Summary Length           | ~100-150 words abstractive; ~150 lines extractive |
| Notes per Lecture        | 10 bullet points capturing key concepts        |
| Best Lectures (Pitch)    | Psychology, Breakthrough MIT (expressive delivery) |
| Most Challenging Lecture | Cities & Decarbonization (dense academic tone) |

---

## 📱 Web Interface (Prototype)

- Upload `.wav`, `.mp3`, or `.m4a` files (≤ 200MB)
- Choose summary type (extractive/abstractive)
- View transcript, summary, and notes
- Download notes for offline use

---

## 📍 Impact and Future Scope

### Educational Impact:
- Assists students in faster, more effective lecture reviews
- Aids accessibility for auditory learners and differently-abled students

### Future Work:
- 🔹 Add speaker diarization for multi-speaker support
- 🔹 Integrate slide-based visual context for multimodal summaries
- 🔹 Personalize summaries based on user feedback or difficulty level
- 🔹 Deploy as a web app or browser plugin for broader access

---

## 👨‍💻 Team
 
- **Bandaru Jaya Nandini**  
- **Mamidi Leha Sahithi**  
- **Siddareddy Gari Harshika**
- **Kavyasai Yaddanapudi**  
Department of Computer Science and Engineering  
Amrita School of Computing, Bengaluru  
Amrita Vishwa Vidyapeetham, India

---

## 📜 License

This project is developed for academic and educational purposes. Contact authors for collaboration or reuse.

