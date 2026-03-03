# py-dlp 🎧🎥

A simple Python CLI tool built on top of **yt-dlp** to download:
- 🔉 Audio as MP3 (with optional thumbnail + metadata)
- 🎥 Video as webm or mp4 (with optional resolution limits)

Uses `questionary` for interactive prompts and `rich` for a prettier terminal experience.

---

## What It Does

### Audio
- Extracts audio as MP3
- Optional: embed thumbnail, add metadata
- Choose output folder with `-P <path>`

### Video
- Downloads in webm or mp4
- Cap max height: 1080 / 720 / 480 / 360
- Merges audio + video into your chosen container

---

## Dependencies

### Python Packages
Install from `requirements.txt`:
- `rich`
- `questionary`

Also needs:
- `yt-dlp` (install via pip)

### System Tool
- `ffmpeg` — must be installed and in your PATH

---

## How to Install

### 1. Clone the repo
```bash
git clone https://github.com/karanveer-lca/py-dlp.git
cd py-dlp
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
pip install -U yt-dlp
sudo apt update && sudo apt install -y ffmpeg
python3 main.py
