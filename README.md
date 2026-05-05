<div align="center">

```
██╗  ██╗███████╗██╗   ██╗██╗      ██████╗  ██████╗  ██████╗ ███████╗██████╗ 
██║ ██╔╝██╔════╝╚██╗ ██╔╝██║     ██╔═══██╗██╔════╝ ██╔════╝ ██╔════╝██╔══██╗
█████╔╝ █████╗   ╚████╔╝ ██║     ██║   ██║██║  ███╗██║  ███╗█████╗  ██████╔╝
██╔═██╗ ██╔══╝    ╚██╔╝  ██║     ██║   ██║██║   ██║██║   ██║██╔══╝  ██╔══██╗
██║  ██╗███████╗   ██║   ███████╗╚██████╔╝╚██████╔╝╚██████╔╝███████╗██║  ██║
╚═╝  ╚═╝╚══════╝   ╚═╝   ╚══════╝ ╚═════╝  ╚═════╝  ╚═════╝ ╚══════╝╚═╝  ╚═╝
```

### Endpoint Monitoring — Keylogging

*An educational demonstration of keyboard input capture and system monitoring techniques.*

<br/>

<img src="https://img.shields.io/badge/Python-3.x-3776ab?style=for-the-badge&logo=python&logoColor=white&labelColor=1a1a2e"/>
<img src="https://img.shields.io/badge/pynput-Keyboard%20Capture-ef4444?style=for-the-badge&logoColor=white&labelColor=1a1a2e"/>
<img src="https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20macOS-10b981?style=for-the-badge&logoColor=white&labelColor=1a1a2e"/>
<img src="https://img.shields.io/badge/Purpose-Educational%20Only-f59e0b?style=for-the-badge&logoColor=white&labelColor=1a1a2e"/>

<br/><br/>

> ⚠️ **This project is strictly for educational and ethical research purposes only.**
> Running this tool on any system without explicit authorization is illegal and unethical.
> The author bears no responsibility for misuse.

<br/>

</div>

---

## 📖 What is This Project?

**Endpoint Monitoring — Keylogging** is an educational Python project that demonstrates how keystroke capture works at the system level. It is designed to help cybersecurity students and developers understand the mechanics of input monitoring — a technique frequently studied in endpoint security, digital forensics, and ethical hacking courses.

By understanding how keyloggers work, security professionals can better design detection systems, write better endpoint protection software, and identify malicious activity on compromised systems. This project makes that learning accessible through clean, readable Python code.

---

## ✨ Features

- ⌨️ **Keystroke Capture** — Records all keyboard input in real time
- 📄 **File Logging** — Saves captured keystrokes to a local log file
- 🔑 **Special Key Handling** — Detects and logs special keys (Enter, Space, Backspace, etc.)
- 🕐 **Timestamp Logging** — Each session logged with date and time
- 🛑 **Clean Stop** — Graceful exit on defined key or keyboard interrupt
- 🪶 **Lightweight** — Single script, minimal dependencies

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| Python 3.x | Core scripting language |
| `pynput` | Cross-platform keyboard input capture |

---

## 📁 Project Structure

```
Endpoint-Monitoring-Keylogging/
│
├── keylogger.py        # Main keylogging script — capture and logging logic
├── requirements.txt    # Python dependencies
└── README.md           # Project documentation
```

---

## 🧠 How It Works

```
Program starts
      │
      ▼
pynput listener attached to keyboard
      │
      ▼
Key pressed by user
      │
      ├── Regular key  →  Character appended to log
      ├── Special key  →  [KEY_NAME] appended to log
      └── Stop key     →  Listener stopped, log saved
      │
      ▼
Keystrokes written to log file
      │
      ▼
Session ends — log file saved locally
```

The `pynput` library attaches a non-blocking listener to the operating system's keyboard input stream. Every key event is intercepted, classified as either a regular character or a special key, formatted into a readable string, and appended to the output log file. The listener runs in a background thread, keeping the script responsive while capturing all input.

---

## ⚙️ Requirements

- Python 3.x installed
- pip package manager

**Install dependencies:**
```bash
pip install -r requirements.txt
```

**Or install directly:**
```bash
pip install pynput
```

---

## ▶️ Usage

**1. Clone the repository:**
```bash
git clone https://github.com/18PriyanshuK/Endpoint-Monitoring-Keylogging.git
cd Endpoint-Monitoring-Keylogging
```

**2. Install dependencies:**
```bash
pip install -r requirements.txt
```

**3. Run the keylogger:**
```bash
python keylogger.py
```

**4. Stop the logger:**
```
Press Ctrl+C  or the defined stop key
```

**5. View the log:**
```bash
cat keylog.txt        # Linux / macOS
type keylog.txt       # Windows
```

---

## 📋 Sample Output

```
=== Session Started: 2026-04-30 10:32:15 ===

Hello[Space]World[Enter]
This[Space]is[Space]a[Space]test[Enter]
password123[Enter]
[Backspace][Backspace][Backspace]
[Escape]

=== Session Ended: 2026-04-30 10:33:02 ===
```

---

## 🔐 Ethical and Legal Notice

```
┌─────────────────────────────────────────────────────────┐
│                   ⚠️  IMPORTANT NOTICE                   │
│                                                          │
│  This tool is provided SOLELY for educational purposes.  │
│                                                          │
│  ✅ Allowed:                                             │
│     • Running on your own personal device                │
│     • Academic study and cybersecurity coursework        │
│     • Ethical research in authorized lab environments    │
│                                                          │
│  ❌ Prohibited:                                          │
│     • Running on any device without explicit permission  │
│     • Capturing credentials or sensitive data of others  │
│     • Any use for surveillance, stalking, or espionage   │
│                                                          │
│  Unauthorized use may violate computer fraud laws        │
│  including the IT Act 2000 (India) and similar           │
│  legislation in other jurisdictions.                     │
└─────────────────────────────────────────────────────────┘
```

---

## 🔮 Future Enhancements

- [ ] Encrypted log file output
- [ ] Email delivery of captured logs (for authorized monitoring demos)
- [ ] GUI interface for start/stop control
- [ ] Screenshot capture at intervals
- [ ] Active window title logging
- [ ] Detection evasion study (for IDS/AV research)

---

## 🤝 Contributing

Contributions for educational improvements are welcome.

```bash
# Fork the repository
git fork https://github.com/PriyanshuKhambalkar/Endpoint-Monitoring-Keylogging.git

# Create a feature branch
git checkout -b feature/your-improvement

# Commit and push
git commit -m "Add: your improvement"
git push origin feature/your-improvement
```

---

## 📚 Learning Resources

If you want to understand this project deeper:

- [pynput Documentation](https://pynput.readthedocs.io/)
- [OWASP — Keystroke Logging](https://owasp.org/www-community/attacks/Keystroke_logging)
- [NIST — Endpoint Security Guide](https://csrc.nist.gov/)

---

## 📜 License

This project is licensed under the [MIT License](https://github.com/PriyanshuKhambalkar/Endpoint-Monitoring-Keylogging/blob/35bd50c9a7f01c6dd836e8a2925c0edd4eb31b82/LICENSE) - see the LICENSE file for details.<br/> 
For commercial use or redistribution, please get in touch with the author.

---

## 👤 Author

**Priyanshu Khambalkar**

---

<div align="center">

*Built with Python · pynput · For Educational Use Only*

⭐ **Star this repo if it helped your cybersecurity learning**

</div>
