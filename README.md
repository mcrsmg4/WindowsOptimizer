# WindowsOptimizer
<p align="center">
  <img src="[https://media.discordapp.net/attachments/1396902883340976248/1396904529932325036/Untitled-1.png](https://cdn.discordapp.com/attachments/1396902883340976248/1396904529932325036/Untitled-1.png?ex=687fc839&is=687e76b9&hm=75acc559d47e4b52e2f39a998b184f3fc207bcc975cab35ed4240cd2608569ba&)" width="200" alt="Windows Optimizer Logo" />
</p>

> A powerful, customizable Windows Tweaks & App Installer GUI tool  
> Simplify optimizing your Windows experience with curated tweaks and one-click installs.

---

## Table of Contents

1. [About WindowsOptimizer](#about-windowsoptimizer)  
2. [Features](#features)  
3. [Installation](#installation)  
4. [Usage](#usage)  
5. [How It Works](#how-it-works)  
6. [Configuration & Customization](#configuration--customization)  
7. [Command Line Options](#command-line-options)  
8. [Troubleshooting](#troubleshooting)  
9. [Contributing](#contributing)  
10. [Releases & Updates](#releases--updates)  
11. [Discord Community](#discord-community)  
12. [License](#license)  
13. [Acknowledgements](#acknowledgements)  

---

## About WindowsOptimizer

WindowsOptimizer is a lightweight, user-friendly tool designed to help users apply a curated set of Windows system tweaks and install popular applications effortlessly. It wraps complex PowerShell scripting inside an intuitive GUI, making it accessible to both casual users and power users.

- Automates registry tweaks to optimize performance and UI  
- Disables unnecessary Windows services for speed  
- Installs apps via Chocolatey and Winget with a simple check-box interface  
- Built-in elevation prompt for administrator privileges  
- Modular design for easy extension and customization

Designed to be open-source and community-driven, WindowsOptimizer encourages developers to contribute, extend, and improve its functionality.

---

## Features

- **User-friendly Windows Forms GUI** to select tweaks and apps  
- **Curated list of essential apps:** Chrome, Firefox, VS Code, 7zip, Discord, and more  
- **Registry and service optimizations** targeting gaming, UI, and keyboard responsiveness  
- **Automated package installation** using Chocolatey and Winget  
- **Auto-detection and installation of Chocolatey if missing**  
- **Elevated PowerShell execution with error handling**  
- **Modular PowerShell script generation** to allow easy updating or custom tweak additions  
- **Cross-compatibility** with Windows 10+  
- **Extensive logging and pause for user review after execution**

---

## Installation

WindowsOptimizer is distributed as a ZIP file containing the batch wrapper and embedded PowerShell script.

### Download

- Grab the latest release ZIP from the [Releases page](https://github.com/mcrsmg4/WindowsOptimizer/releases)  
- Extract anywhere convenient on your Windows machine

### Requirements

- Windows 10 or later  
- PowerShell 5.1 or higher (built-in on Windows 10+)  
- Internet connection for app installs (Chocolatey/Winget)

### Running

Double-click the `WindowsOptimizer.bat` file to launch the GUI. The script handles elevation and runs the embedded PowerShell script automatically.

---

## Usage

1. Launch `WindowsOptimizer.bat` (requires admin privileges).  
2. In the GUI window, check the tweaks and applications you want to apply/install.  
3. Click **Apply Tweaks + Install**.  
4. The script will run with elevated permissions and display progress.  
5. Upon completion, a pause will let you review any output or errors.  
6. Close the window when done.

---

## How It Works

WindowsOptimizer leverages a batch file wrapper to create and run a temporary PowerShell script:

- The batch file generates a PowerShell script dynamically in the temp folder.  
- This PowerShell script builds a Windows Forms GUI with checkbox options.  
- On confirmation, it runs system tweaks via registry and service modifications.  
- It checks for Chocolatey and installs it if necessary, then installs selected apps using Chocolatey or Winget.  
- The batch file ensures the process runs with full administrator privileges and handles elevation prompts.

This hybrid approach balances ease of distribution (batch wrapper) with powerful scripting capabilities (PowerShell).

---

## Configuration & Customization

Developers and power users can customize or extend WindowsOptimizer by editing the PowerShell script:

- Modify or add apps in the `$apps` array  
- Change registry tweaks or add new ones inside the elevated `Start-Process` block  
- Adjust GUI layout or button behavior within the form creation code  
- Enable logging by redirecting output to a file for troubleshooting  
- Integrate new package managers or add custom install commands

> **Note:** To contribute, clone the repo, edit the PowerShell script, and test thoroughly before submitting pull requests.

---

## Command Line Options

Currently, WindowsOptimizer does not support command line arguments but contributions to add this feature are welcome!

Planned features may include:

- Silent mode for automated scripting  
- Selection of specific tweaks or apps via CLI  
- Output logging and error reporting options

---

## Troubleshooting

- **Script fails to run:** Ensure you launch the batch file with administrator privileges.  
- **PowerShell execution policy errors:** The script sets policy bypass temporarily but check if your system policy restricts it.  
- **Chocolatey not installing:** Verify internet connectivity and unblock script execution.  
- **App installs failing:** Check if Winget or Chocolatey commands run manually on your system.  
- **UI not appearing:** Confirm PowerShell version and Windows Forms assemblies are available.

If you encounter issues, please open an issue in this repo or join the [Discord server](#discord-community) for live help.

---

## Contributing

We welcome contributions from everyone! Whether you want to:

- Add new tweaks or apps  
- Improve the GUI interface  
- Fix bugs or optimize scripts  
- Write documentation or examples

Please follow this process:

1. Fork the repository  
2. Create a feature branch  
3. Commit your changes with clear messages  
4. Submit a Pull Request describing your improvements

Before submitting, ensure:

- Code is well-commented and formatted  
- Scripts run without errors  
- New features are documented

See the [CONTRIBUTING.md](CONTRIBUTING.md) (coming soon) for detailed guidelines.

---

## Releases & Updates

Official releases will be available in the [Releases](https://github.com/mcrsmg4/WindowsOptimizer/releases) section as ZIP packages.  

- Use releases for stable, tested versions.  
- Clone the repo for bleeding-edge development or to contribute.  
- Each release includes detailed changelogs and upgrade notes.

---

## Discord Community

Join the official Discord to discuss, ask questions, get support, and collaborate:  
[https://discord.gg/VHgW6ctWnh](https://discord.gg/VHgW6ctWnh)

---

## License

WindowsOptimizer is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

## Acknowledgements

- Thanks to the open-source community for PowerShell and Chocolatey  
- Inspiration from various Windows tweak collections  
- Special thanks to contributors and testers who make this project better

---

*This README was made with the intent to be comprehensive, clear, and welcoming to users and developers alike. Feel free to submit suggestions or improvements!*

