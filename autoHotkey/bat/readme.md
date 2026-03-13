# VS Code Launcher with AutoHotkey Remap

This setup ensures an **AutoHotkey remap script runs automatically whenever Visual Studio Code launches**.
Instead of opening VS Code directly, a `.bat` launcher is used.  
The launcher starts the AutoHotkey script first and then launches VS Code.

## Setup

### 1. Create the Launcher `.bat` File
Create a file such as `vscode-launch.bat` with the following contents.  
Update the paths so they match your system.

```bat
@echo off
start "" "C:\Users\Admin\Documents\AutoHotkey\RemapVisualStudioCode.ahk"
start "" "C:\Users\Admin\AppData\Local\Programs\Microsoft VS Code\Code.exe"
```

Update these paths:
- `C:\Users\Admin\Documents\AutoHotkey\RemapVisualStudioCode.ahk` (path to your **AutoHotkey remap script**)
- `C:\Users\Admin\AppData\Local\Programs\Microsoft VS Code\Code.exe` (path to your **VS Code executable**)

Typical VS Code install path:
C:\Users\<username>\AppData\Local\Programs\Microsoft VS Code\Code.exe

### 2. Move the `.bat` Fil
Move the `.bat` file into the same folder that contains the **Visual Studio Code Start Menu shortcut**.

Common locations:
C:\ProgramData\Microsoft\Windows\Start Menu\Programs
C:\Users\<username>\AppData\Roaming\Microsoft\Windows\Start Menu\Programs

### 3. Create a Shortcut
Right-click the `.bat` file and select: Create shortcut

### 4. Pin the Shortcut to the Taskbar
Right-click the newly created shortcut and select: Pin to taskbar

### 5. Replace the Original VS Code Taskbar Icon
Remove the original **Visual Studio Code** icon from the taskbar and use the new pinned shortcut instead.
