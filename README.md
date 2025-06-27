
# 🧨 Pico Ducky: Advanced Recon & Extractor

Turn a **Raspberry Pi Pico** into a stealthy and powerful **BadUSB device** using this high-speed, low-observable script collection. Built on **CircuitPython**, this project allows the Pico to emulate a USB keyboard (HID), inject a **PowerShell payload**, perform rapid system reconnaissance on Windows targets, and store results back onto the device.

> ⚠️ **For educational and ethical testing purposes only. Unauthorized use is prohibited.**

---

## 🚀 Features

* **🕵️‍♂️ Stealth Execution**
  Executes entirely via a hidden PowerShell instance — no popups, no visible windows.

* **🔐 Admin Escalation**
  Attempts to bypass UAC (User Account Control) to obtain elevated system privileges for deeper access.

* **📡 Comprehensive Reconnaissance**
  Collects valuable data including:

  * Wi-Fi passwords
  * System and OS details
  * Network configuration
  * Running processes

* **🧠 Smart Fallback Logic**
  If the initial USB drive label search fails, the script falls back to alternative logic to identify the Pico device.

* **📝 Automated Logging**
  Uses PowerShell’s `Start-Transcript` to log the entire session into a structured and readable report saved on the device.

---

## ⚙️ How It Works

1. Connect the Raspberry Pi Pico to a Windows machine.
2. The Pico emulates a keyboard and injects a PowerShell payload.
3. The payload executes a hidden recon routine.
4. Results are saved back to the Pico for later review.

---

## 🧪 Limitations

| Limitation          | Description                                                                                    |
| ------------------- | ---------------------------------------------------------------------------------------------- |
| **Target OS**       | Works only on **Windows 10 & 11**. Not compatible with macOS or Linux.                         |
| **UAC Bypass**      | Not guaranteed. Depends on admin rights and default UAC settings. Might fail on secure setups. |
| **Keyboard Layout** | Assumes a **US-QWERTY** layout. Other layouts may cause incorrect input.                       |
| **Antivirus/EDR**   | May be flagged or blocked by advanced security tools and endpoint protection systems.          |

---

## 📁 Project Structure

| File/Folder      | Description                                              |
| ---------------- | -------------------------------------------------------- |
| `payloads/`      | Contains PowerShell payload scripts injected by the Pico |
| `circuitpython/` | CircuitPython boot and device setup scripts              |
| `README.md`      | Project documentation                                    |

---

## 📦 Requirements

* ✅ Raspberry Pi Pico (or Pico W)
* ✅ USB connection to Windows 10/11 machine
* ✅ CircuitPython installed on Pico
* ✅ Basic knowledge of PowerShell and HID scripting

---

## 🧰 Setup Instructions

1. Flash the **CircuitPython UF2** firmware to your Raspberry Pi Pico.
2. Copy the script files to the Pico’s mounted USB storage.
3. Plug the Pico into a **target Windows machine**.
4. The payload will run automatically, and logs will be saved on the Pico.

---

## 📚 Resources

* [CircuitPython for Raspberry Pi Pico](https://circuitpython.org/board/raspberry_pi_pico/)
* [Microsoft PowerShell Documentation](https://learn.microsoft.com/en-us/powershell/)

---

## ⚠️ Disclaimer

> This tool is intended **only** for:
>
> * Ethical hacking
> * Security auditing
> * Educational use in **controlled environments**

**Do not** use this tool on systems you do not own or have explicit permission to test. Misuse of this tool may be illegal and unethical.
**The author assumes no responsibility** for any damage or consequences resulting from use.



