# DVDCast — DVD → Chromecast (Linux)

Cast a DVD to your Chromecast from Linux with one command (or a menu click).

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](#license)
[![Platform: Linux](https://img.shields.io/badge/platform-linux-black.svg)]()
[![VLC](https://img.shields.io/badge/VLC-3.x-orange.svg)]()

> DVDCast discovers your Chromecast via mDNS (Avahi), auto-selects the **longest
> DVD title** with `lsdvd`, and streams it with VLC using a Chromecast-friendly
> **H.264/AAC** transcode so you don’t get “buffering forever.”

---

## Features
- 🔎 **Auto-discover Chromecast** (filters out Nest Hub)
- 💿 **Auto-pick longest title** (`lsdvd`) — override with `TITLE=N` when needed
- 🎥 **Chromecast-compatible transcode** (H.264/AAC) on VLC **3.x**
- 🧠 **Drive auto-detect** (`/dev/sr1`, `/dev/sr0`, `/dev/dvd`) — override with `DEVICE=/dev/srX`
- 🧹 Optional pre-cast **stop** using `catt` so nothing else holds your Chromecast
- 🖱️ Desktop launcher: **DVDCast (DVD → Chromecast)**

---

## Requirements

```bash
sudo apt install -y vlc avahi-utils lsdvd regionset libdvd-pkg
sudo dpkg-reconfigure libdvd-pkg   # installs libdvdcss2 for encrypted discs
# optional controller CLI:
pip3 install --user catt

