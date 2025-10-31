# Image2GNF Tool – JPG & MP4 to GNF Converter

**A clean, user-friendly Windows GUI tool to convert JPG images or MP4 videos into PlayStation GNF texture arrays using `image2gnf.exe`.**

Perfect for **PS4/PS5 texture modding**

---

## Features

- **JPG Folder to GNF** – Convert hundreds of JPGs into a single `.gnf` file.
- **MP4 to 101 JPG Frames to GNF** – Auto-extracts **101 evenly-spaced frames** using `ffmpeg`.
- **Frames go directly into JPG Input Folder** – No temp files, no cleanup.
- **Preset Commands** (PS5 BC7, PS4 BC7, Fast, Small, Custom)
- **Live Log Output** – See every step in real time.
- **GNF Preview** – Open result instantly in `gnfViewer.exe`.
- **Drag & Drop** – Drop folders directly on input fields.
- **Dark Theme** – Easy on the eyes.
- **Release-Ready** – All binaries in one folder, no installer.

---

## Screenshot

**Tool Interface**
<img width="1093" height="729" alt="Screenshot 2025-10-29 132356" src="https://github.com/user-attachments/assets/3065fe42-4d70-4c08-a7d6-f6d6ee021e61" />



---

## Requirements

All required files are **included** in the release:

| File | Purpose |
|------|--------|
| `Image2GnfTool.exe` | Main GUI app |
| `image2gnf.exe` | Converts JPGs to GNF |
| `gnfViewer.exe` | Preview GNF textures |
| `ffmpeg.exe` | Extract frames from MP4 |
| `libSce*.dll` | Required by `image2gnf.exe` |

> No installation needed. Just download, unzip, run.

---

## How to Use

### 1. **JPG to GNF**
1. Click **Browse** to "JPG Input Folder"
2. Select folder with `.jpg` files
3. Choose **GNF Output Folder**
4. Select a **Preset** (or type custom command)
5. Click **Convert to GNF**

### 2. **MP4 to GNF (101 Frames)**
1. Click **Browse** to "MP4 Input"
2. Select `.mp4` video
3. Make sure **"Extract 101 frames to JPG Input Folder"** is checked
4. Select **JPG Input Folder** (where frames will be saved)
5. Select **GNF Output Folder**
6. Click **Convert to GNF**

> Frames are saved as `frame_0001.jpg`, `frame_0002.jpg`, etc.  
> Existing `frame_*.jpg` files are overwritten.

---

## Presets

| Preset | Command |
|-------|--------|
| **PS5 - BC7 (High Quality)** | `-t 2DArray -f Bc7UNorm -g 1 -x M -e -w -b 0.8 -z 30 -m 4 -l 4KB` |
| **PS5 - BC7 (Fast)** | `-t 2DArray -f Bc7UNorm -g 1 -x M -e -w -b 0.5 -z 15 -m 4 -l 4KB` |
| **PS5 - BC1 (Small Size)** | `-t 2DArray -f Bc1UNorm -g 1 -x M -e -w -b 0.6 -z 20 -m 3 -l 4KB` |
| **PS4 - BC7** | `-t 2DArray -f Bc7UNorm -g 0 -x M -e -w -b 0.7 -z 25 -m 4 -l 64KB` |

> Use **Custom** to write your own `image2gnf` command.

---

## Output

- GNF file: `textures.gnf` in your selected **GNF Output Folder**
- Click **Open GNF Output** to open folder
- Click **Preview GNF** to view in `gnfViewer.exe`

---

## Building from Source

1. Open in **Visual Studio 2022+**
2. Target: **.NET 6.0 or .NET 8.0** (Windows)
3. Build in **Release** mode
4. Copy output `.exe` + all `.dll` + `ffmpeg.exe` into one folder

---

## Folder Structure (Release)

  TBA
