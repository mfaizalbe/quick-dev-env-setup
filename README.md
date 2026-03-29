# 📂 Repo: `quick-dev-env-setup`

```
quick-dev-env-setup/
│
├── README.md
├── Brewfile                       # Lists all packages and casks for brew bundle.
├── setup-dev-environment.sh       # Bash script for macOS/Linux/WSL with progress bars
└── setup-windows-oneclick.ps1     # PowerShell script for Windows with progress bars
```

---

## 1️⃣ `README.md`

# Development Environment Setup

This repository provides a **quick setup** for anyone setting up a development environment on a new machine.

---

## Supported Operating Systems

| OS | Script |
|----|--------|
| Windows 10/11 (via WSL) | `setup-windows-oneclick.ps1` |
| Linux / WSL (Ubuntu) | `setup-dev-environment.sh` |
| macOS (Homebrew) | `setup-dev-environment.sh` |

---

## Tools Installed

- Linux Terminal / WSL
- Visual Studio Code
- Git
- Docker
- Terraform
- Node.js (LTS via NVM)
- Python 3.11+
- Kubectl
- Helm
- AWS CLI

---

## Usage Instructions

### 🪟 Windows (One-Click)

1. Open **PowerShell as Administrator**.
2. Run:

```powershell
Set-ExecutionPolicy Bypass -Scope Process
.\setup-windows-oneclick.ps1
````

> The script installs WSL (if missing), Git, and runs the Linux/macOS setup script automatically in WSL.
> Watch **progress bars and colored messages**. Logs are automatically saved.

---

### 🍎 macOS / Linux / WSL

1. Open **Terminal**.
2. Run:

```bash
chmod +x setup-dev-environment.sh
./setup-dev-environment.sh
```

> The script detects your OS, installs all required tools, shows **progress bars**, and logs everything automatically.

---

### ✅ Verification

The setup scripts automatically check:

```bash
git --version
docker --version
aws --version
terraform --version
node --version
python3 --version
kubectl version --client
helm --version
code --version
```

---

### 📂 Logs

* Each run creates a timestamped log file (`setup-log-YYYYMMDD-HHMMSS.txt`) in the same folder.
* Use logs for troubleshooting.

---

### Notes

* For Windows, always use **WSL** for Linux-based commands.
* Scripts are beginner-friendly for students changing laptops or joining new teams.
* If a tool fails, consult the official documentation or `Required Hardware and Software.docx`.

---


## 2️⃣ `setup-dev-environment.sh` (macOS/Linux/WSL)

- Bash script with **progress bars** and color-coded output.  
- Installs all major dev tools (Git, Docker, Terraform, Node.js via NVM, Python3, Kubectl, Helm, AWS CLI).  
- Logs everything to a timestamped file.  

*(Use the script from the previous response with progress bar function `progress_bar()` and `install_tool()`.)*

---


## 3️⃣ `setup-windows-oneclick.ps1` (Windows)

- PowerShell script with **progress bars** and color-coded output.  
- Checks and installs WSL + Ubuntu, Git via winget.  
- Copies and runs `setup-dev-environment.sh` inside WSL.  
- Logs everything automatically.  

*(Use the PowerShell script from the previous response with `Show-Progress` function.)*

---

### ✅ Features of This Repo

1. **One-click installation** for macOS, Linux, WSL, and Windows.
2. **Color-coded output** for success/failure/info.
3. **Progress bars** for each tool to give visual feedback.
4. **Automatic logging** with timestamped files for troubleshooting.
5. **Verification of all installed tools** at the end.

---

### 🚀 Quick Start

#### macOS / Linux / WSL

```bash
git clone https://github.com/mfaizalbe/quick-dev-env-setup.git
cd quick-dev-env-setup
chmod +x setup-dev-environment.sh
./setup-dev-environment.sh
```

#### Windows

```powershell
git clone https://github.com/mfaizalbe/quick-dev-env-setup.git
cd quick-dev-env-setup
Set-ExecutionPolicy Bypass -Scope Process
.\setup-windows-oneclick.ps1
```

> Watch **progress bars** for each tool and check the log file if anything fails.

---

### 🙏 Acknowledgements
[NTU SCTP - Coaching 1: Developer Tools Setup Review](https://docs.google.com/document/d/17FHtNo1hWOK3sxRcwcGphUtV4CWPtUkeYk2ZP90VAEI)
