# Video Transcription and Braille Conversion System

> An AI-powered system to transcribe videos into text, generate subtitles, and convert them into Braille for accessibility.

---

## Table of Contents

* [Overview](#overview)
* [Features](#features)
* [Installation](#installation)
* [Usage](#usage)
* [Dependencies](#dependencies)
* [File Structure](#file-structure)
* [Acknowledgements](#acknowledgements)
* [License](#license)

---

## Overview

This project is an **AI-powered video transcription and accessibility tool** that:

1. Extracts audio from videos.
2. Transcribes audio to text using OpenAI's **Whisper** model.
3. Restores punctuation with Hugging Face transformer models.
4. Generates **SRT subtitle files** for videos.
5. Converts subtitles into **Braille text** for visually impaired users.
6. Displays subtitles synchronized with video playback.

It can be used for educational videos, accessibility tools, or content summarization.

---

## Features

* Extract audio from any video format using FFmpeg.
* High-accuracy transcription using Whisper.
* Automatic punctuation restoration.
* SRT subtitle generation.
* Braille conversion for subtitles.
* Real-time subtitle display with OpenCV.

---

## Installation

1. Clone the repository:

```bash
git clone <repo_url>
cd <repo_folder>
```

2. Install Python dependencies:

```bash
pip install -r requirements.txt
```

3. Install FFmpeg:

* **Windows:** Download from [FFmpeg official website](https://ffmpeg.org/download.html) and add it to your PATH.
* **Linux / Ubuntu:**

```bash
sudo apt update
sudo apt install ffmpeg
```

---

## Usage

1. Place your video file in the project folder, e.g., `video.mp4`.
2. Update the paths in the script:

```python
video_path = "video.mp4"
output_srt_path = "output_subtitles.srt"
output_braille_file = 'braille_output.txt'
```

3. Run the script:

```bash
python video_transcription_braille.py
```

4. Outputs:

* `output_subtitles.srt` → Generated subtitles file.
* `braille_output.txt` → Braille transcription.
* OpenCV window → Video playback with synchronized subtitles.

5. Press **`q`** to exit the video window.

---

## Dependencies

* Python 3.10+
* [FFmpeg](https://ffmpeg.org/)
* Python libraries:

```text
ffmpeg-python
whisper
pydub
numpy
opencv-python
transformers
srt
```

Install all dependencies with:

```bash
pip install ffmpeg-python whisper pydub numpy opencv-python transformers srt
```

---

## File Structure

```text
project/
│
├─ video_transcription_braille.py   # Main script
├─ requirements.txt                 # Python dependencies
├─ video.mp4                        # Input video file
├─ output_subtitles.srt             # Generated subtitles
└─ braille_output.txt               # Generated Braille text
```

---

## Acknowledgements

* [OpenAI Whisper](https://github.com/openai/whisper) – Speech-to-text transcription.
* [Hugging Face Transformers](https://huggingface.co/models) – Punctuation restoration.
* [FFmpeg](https://ffmpeg.org/) – Audio extraction.
* [Pydub](https://github.com/jiaaro/pydub) – Audio processing.
* [OpenCV](https://opencv.org/) – Video display and subtitle overlay.

---

## License

This project is licensed under the MIT License.
