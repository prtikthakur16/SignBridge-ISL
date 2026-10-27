# SignBridge-ISL
Bidirectional Indian Sign Language Translator &amp; Learning Companion
---

## Key Features

- **ISL to Speech/Text:** Tracks hand and upper-body landmarks in real time and synthesizes regional spoken voice output.
- **Speech to Sign Visualizer:** Converts incoming spoken words into sequential sign demonstrations using an indexed visual avatar.
- **Interactive Sign Tutor:** Live camera feedback comparing user hand positions against standard sign language templates to teach foundational vocabulary.
- **Edge / Low-Resource Feasibility:** Designed to run on standard mobile and laptop webcams without dedicated cloud inference.

---

## System Architecture

1. **Vision Pipeline:** MediaPipe Holistic / Hands extracts 21 key points per hand and pose coordinates at 30 FPS.
2. **Translation Engine:** Normalized coordinate arrays pass into a lightweight temporal sequence classifier.
3. **Synthesis Engine:** Generated text is rendered to the UI and vocalized via standard Text-to-Speech (TTS) libraries.
4. **Interactive Tutor:** Compares cosine similarity between real-time user hand joint vectors and reference gesture landmarks.

---

## Project Structure

```text
SignBridge-ISL/
├── README.md              # Project overview and run guide
├── LICENSE                # MIT License
├── architecture.md        # Detailed system pipeline breakdown
├── requirements.txt       # Python dependencies
├── app.py                 # Core application entry point
├── sample_data/           # Keypoint landmark templates & test data
│   └── sample_test.json   # Sample hand coordinate frame data
