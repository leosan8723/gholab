# MapLeadBot portable

Portable Windows build of **MapLeadBot**: a scanner for local businesses on
Google Maps that need a (better) website. This repo ships ONLY the two
executables you need — no config, no API keys, no user data.

## What's inside

| File | What it is |
|---|---|
| `MapLeadBot.exe` | The app (one-file build, no Python required on the target PC) |
| `gosom.exe` | Third-party scraper binary ([gosom/google-maps-scraper](https://github.com/gosom/google-maps-scraper) v1.18.1, Windows amd64) |

## Quick start

1. Download both files into one folder.
2. Double-click `MapLeadBot.exe` and answer the questions (or open the web GUI).
3. Everything is created next to the exe: `ai_config.json`, `prompts/`,
   `output/`, `exclude.txt` (optional).

Notes:

- The first scraper run downloads its browser — keep internet on, it can take
  a few minutes.
- AI judgement is optional; enter your endpoint/key/model in the GUI's
  **AI settings** on each PC. Never copy `ai_config.json` from one PC to
  another (it holds the key in plain text).
- Windows 10/11 64-bit only.
- Source code of MapLeadBot: see the project repository (SRS: `leadbot.py`,
  `aijudge.py`, `webgui.py`, `apppaths.py`; built with PyInstaller via
  `build_exe.bat`).
