# DIRB - Web Content Scanner

**DIRB** is a simple yet powerful web content scanner used in cybersecurity to discover hidden files and directories on web servers.  
It works by performing a **dictionary-based brute-force attack**, using wordlists to find existing or hidden web objects.

---

## 📦 Installation

### 🧠 Prerequisites
Ensure your system has:
- **Linux / macOS** (DIRB is pre-installed on Kali Linux)
- `git` and `make` utilities installed

### 🐧 Install on Debian/Ubuntu
```bash
sudo apt update
sudo apt install dirb -y
```

## 🚀 Usage
🔍 Basic Scan
```bash
dirb http://example.com
```

Performs a default scan using the built-in wordlist to find directories and files on the target site.

📄 Scan with Custom Wordlist
```bash
dirb http://example.com /usr/share/wordlists/dirb/common.txt
```

🌐 Scan HTTPS Target
```bash
dirb https://example.com
```

🚫 Exclude Certain Extensions
```bash
dirb http://example.com -X .php,.txt
```
💾 Save Output to File
```bash
dirb http://example.com -o results.txt
```

⚙️ More Options
Option	Description
```bash
-u	Specify user-agent
```
```bash
-p	Use proxy (e.g. -p http://127.0.0.1:8080)
```
```bash
-r	Don’t recursively scan found directories
```
```bash
-z	Set delay between requests (milliseconds)
```
```bash
-N	Skip responses with specific status codes (e.g. -N 403)
```
