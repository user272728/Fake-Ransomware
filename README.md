# **Fake Ransomware**

## **Overview**

**Fake Ransomware** is a prank project designed to simulate the experience of ransomware in a controlled and harmless environment. This project displays a fullscreen message, accompanied by a countdown and a progress bar, giving the illusion that the machine is undergoing file encryption. It restricts user input until a specific key or code is entered, at which point the program exits.

This software **does not actually encrypt any files** and is intended purely for educational or prank purposes to demonstrate how a ransomware-like interface might behave.

---

## **Features**

- Fullscreen interface that imitates a typical ransomware message.
- Displays a dramatic warning with a countdown timer.
- Shows a fake "encryption progress" bar.
- Temporarily disables user input to simulate control over the system.
- User can escape the prank by entering a specific "code."
- Optional shutdown feature triggered after the progress bar reaches 100%.

---

## **How It Was Made**

The project was built using **Python** and **Tkinter** to create the user interface. Tkinter, a popular library for GUI applications in Python, was used to design the fullscreen message and the progress bar. Additionally, **ctypes** was utilized to briefly block user input, giving the user the sense of being locked out of their system.

The program progresses over a 20-second interval, during which the countdown timer ticks down and the progress bar fills up. If the user does not enter the specific key or "code" within the given time, the program shuts down the system to simulate a catastrophic event. However, all of this is purely for show—no files or system settings are modified.

The executable was created using **PyInstaller**, a tool that converts Python scripts into standalone executables. The following command was used to package the script into a single file, setting the icon and ensuring no terminal window is shown upon execution:

```bash
pyinstaller --noconsole --onefile --icon=lock_folder_padlock_file_security_icon_219492.ico --name "Fake Ransomware" prank.py
