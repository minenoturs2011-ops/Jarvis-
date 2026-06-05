# 🤖 J.A.R.V.I.S. — Your Personal AI Assistant

<div align="center">

**A movie-style AI desktop assistant for Windows.**
Talk to it. It talks back. It runs everything locally on your PC.

**Version 6.0 "Public"**

*Just A Rather Very Intelligent System*

</div>

---

## ✨ What is this?

J.A.R.V.I.S. is a voice assistant inspired by the AI from Iron Man. It lives on your
Windows PC as a glowing animated orb. You talk to it (or type), and it responds with a
natural voice. It can answer questions, open your apps and games, show you pictures,
write code, monitor your system, and remember things about you — all running **locally
and privately** on your own machine. No subscription, no cloud, no data leaving your PC.

### Highlights
- 🔵 **Living orb** that changes color with what it's doing
- 🎙️ **Natural British voice** (offline)
- 🧠 **Local AI** — your conversations never leave your computer
- 💾 **Remembers you** — your name, preferences, and projects
- 🖼️ **Shows pictures** on request
- 🎮 **Launches games & apps** by voice
- 📊 **Live system monitor** (CPU / RAM / GPU)
- ⌨️ **Works by voice OR typing**

---

## 🚀 Installation (Beginner-Friendly)

> **Don't worry if you've never done this before — follow each step in order.**
> The whole thing takes about 15 minutes, most of which is waiting for downloads.

### Step 1 — Install Python
1. Go to **[python.org/downloads](https://www.python.org/downloads/)**
2. Click the big yellow **"Download Python"** button
3. Run the installer
4. ⚠️ **VERY IMPORTANT:** On the first screen, check the box that says
   **"Add Python to PATH"** at the bottom, *then* click Install.

### Step 2 — Install Ollama (the AI engine)
1. Go to **[ollama.com](https://ollama.com)**
2. Click **Download** → **Download for Windows**
3. Run the installer. When it's done, Ollama runs quietly in the background
   (you'll see a small llama icon in your system tray).

### Step 3 — Download J.A.R.V.I.S.
1. Download the Jarvis ZIP file
2. Right-click it → **Extract All**
3. Move the extracted folder somewhere simple, like `C:\Jarvis`

### Step 4 — Run the installer
1. Open the Jarvis folder
2. Double-click **`install.bat`**
3. A black window opens and installs everything + downloads the AI model
   (about 2 GB — this is the longest wait, ~5 minutes)
4. When it says "DONE", close the window.

### Step 5 — Launch!
Double-click **`run_orb.bat`**.

The orb window opens. Wait a few seconds for "model warm — ready to chat" to
appear in the activity feed, then **say "Hey Jarvis"** or **type in the box** at
the bottom. 🎉

---

## ⭐ Make it Better (Optional but Recommended)

These two extras dramatically improve Jarvis. Do them after the basic version works.

### 🎙️ Premium Voice
Double-click **`install_piper.bat`** and choose a voice (option 1, "Alan", sounds
most like movie Jarvis). This replaces the robotic default voice with a natural
neural one that works fully offline.

### 🧠 Smarter AI (extra models)
Double-click **`install_models.bat`** to add a **coding model** and a **reasoning
model**. Jarvis automatically uses the right one for each question. If you skip
this, Jarvis just uses the fast model for everything — totally fine.

> **Tip:** The extra models are larger (~5 GB each) and slower on older GPUs.
> Only add them if you have a good graphics card and want top-tier coding help.

---

## 🗣️ How to Use It

Say **"Hey Jarvis"** then your request, or just type in the box. Try these:

| What you say | What Jarvis does |
|---|---|
| "Hello" | Greets you |
| "What can you do" | Lists all his abilities |
| **"How do you work"** | **Explains his entire architecture** |
| **"Jarvis showcase"** | **Runs a full guided demo** |
| "Show me a picture of a husky" | Opens an image gallery |
| "What's the weather" | Tells you the forecast |
| "Open Chrome" / "Launch Steam" | Opens apps and games |
| "What's my CPU usage" | Reports system stats |
| "Remember that I like sci-fi movies" | Saves a fact about you |
| "What's my name" | Recalls what it knows about you |
| "Write a Python function to sort a list" | Uses the coding model |
| "Run a system diagnostic" | Checks every part of your PC aloud |
| "Goodbye Jarvis" | Orb goes dark (sleep mode) |
| "Wake up Jarvis" | Wakes it back up |
| "Stop" | Interrupts it mid-sentence |

### 🪟 The Window
- **Drag the top bar** to move the window
- **◉ button** (or `H` key) — hide everything but the orb
- **⛶ button** (or `F` key, `ESC` to exit) — fullscreen
- **– ▢ ✕** — minimize, expand, close

---

## 🖥️ System Requirements

| | Minimum | Recommended |
|---|---|---|
| **OS** | Windows 10 | Windows 11 |
| **Python** | 3.10+ | 3.11+ |
| **RAM** | 8 GB | 16 GB |
| **Graphics** | Any (CPU works, slowly) | NVIDIA, 6 GB+ VRAM |
| **Free disk** | 5 GB | 15 GB (all models) |
| **Internet** | For setup & web search | — |

---

## 🔧 Troubleshooting

<details>
<summary><b>Jarvis says "AI offline" or won't answer questions</b></summary>

Ollama isn't running. Make sure the Ollama app is open (llama icon in system tray).
Then open Command Prompt and type `ollama list`. If it's empty, run:
`ollama pull llama3.2:3b`
</details>

<details>
<summary><b>Responses are slow</b></summary>

The **first** question after launch loads the AI into memory (takes 30–60 seconds
once). After that it's fast. Wait for "model warm — ready to chat" in the activity
feed before asking. If it's always slow, close games or heavy browser tabs that are
using your graphics card.
</details>

<details>
<summary><b>No sound / Jarvis won't talk</b></summary>

Open Command Prompt in the Jarvis folder and run `python test_voice.py`. It checks
every voice engine and tells you what works. The easiest fix is usually running
`install_piper.bat` for the offline voice.
</details>

<details>
<summary><b>Microphone not working</b></summary>

Jarvis still works fully by **typing** in the box. For voice, check Windows
microphone permissions (Settings → Privacy → Microphone) and that a mic is connected.
</details>

<details>
<summary><b>Images won't show</b></summary>

Check the activity feed when you ask for a picture — it shows which image source it
tried. If all fail, your network or firewall may be blocking image sites.
</details>

<details>
<summary><b>A command window flashed and closed / errors on launch</b></summary>

Make sure you ran `install.bat` first so all the required components are installed.
</details>

---

## 📦 Making a Shareable EXE (Advanced)

To create a standalone `JARVIS.exe` that doesn't need Python:
1. Run **`build_exe.bat`** (takes 2–5 minutes)
2. Find `JARVIS.exe` in the new `dist` folder
3. Share the whole `dist` folder

> For your own daily use, `run_orb.bat` is better — faster to start and shows logs
> if anything breaks. Build the EXE only to give Jarvis to someone without Python.

---

## 🔒 Privacy

Everything runs **on your computer**. The AI is fully local (Ollama). Your
conversations, your memory, and your voice **never leave your machine**. The only
time Jarvis uses the internet is when *you* ask it to search the web or show a picture.

---

## ❓ FAQ

**Is it free?** Yes, completely. No subscription, no account.

**Does it need internet?** Only for the initial setup and for web searches/images you
request. The AI and voice work fully offline.

**Will it slow down my PC?** It uses your graphics card while thinking, then releases
it. It's designed to stay out of the way.

**Can it control my whole computer?** It can open apps, launch games, adjust volume,
and run diagnostics. It only does what you ask.

**What AI model does it use?** By default `llama3.2:3b` — small, fast, and capable.
You can add bigger models for coding and reasoning.

---

## 🙏 Credits

Built on these excellent open-source projects:
- **[Ollama](https://ollama.com)** — local AI runtime
- **[Piper](https://github.com/rhasspy/piper)** — neural text-to-speech
- **[Three.js](https://threejs.org)** — the animated orb
- **[pywebview](https://pywebview.flowrl.com)** — desktop window

Developed with assistance from Claude (Anthropic).

---

<div align="center">

*"Sometimes you gotta run before you can walk."*

**Enjoy your J.A.R.V.I.S.** 🤖

</div>
