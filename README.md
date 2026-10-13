# DeepSeek Desktop for Windows
<img width="1604" height="948" alt="image" src="https://github.com/user-attachments/assets/d055b506-8c0f-4589-a8d6-c9c3df208001" />

**An unofficial desktop application for DeepSeek, built with Electron.**

DeepSeek Desktop for Windows is an independent desktop application that provides access to the official DeepSeek web interface from a dedicated Windows window.

The project focuses on creating a simple desktop experience with persistent sessions, convenient application launching, and Windows executable builds.

> **Development status:** Experimental / Work in Progress.
>
> This is an independent, unofficial project. It is not developed, endorsed, sponsored, or maintained by DeepSeek.

---

## Overview

The main objective of this project is to package the DeepSeek web experience into a Windows desktop application using Electron.

Instead of opening DeepSeek manually in a web browser, users can launch a dedicated desktop application with its own persistent browser session.

The project also serves as a foundation for experimenting with desktop application development using JavaScript, Node.js, and Electron.

## Features

- **Desktop experience:** Access DeepSeek from a standalone Windows application.
- **Persistent sessions:** Electron stores session data locally so users can remain signed in while the provider's session remains valid.
- **Dedicated application window:** Use DeepSeek without browser tabs.
- **Windows support:** Run the project on Windows 10 and Windows 11.
- **Executable builds:** Package the application as a Windows executable using Electron Builder.
- **Development environment:** Run and debug the application with Node.js.
- **Source code available:** Study, modify, and extend the project.

Some authentication methods or embedded browser behaviors may be restricted by the DeepSeek service.

## Technology Stack

| Technology       | Purpose                                       |
| ---------------- | --------------------------------------------- |
| Electron         | Desktop application framework                 |
| JavaScript       | Application logic                             |
| Node.js          | Development environment and runtime tooling   |
| HTML / CSS       | Local application interface, where applicable |
| Electron Builder | Windows executable packaging                  |
| npm              | Dependency and script management              |
| PowerShell       | Windows development and build commands        |

## Requirements

Before running the project, install:

- Windows 10 or Windows 11 (64-bit recommended).
- Node.js LTS and npm.
- Git, if you plan to clone the repository.
- A stable internet connection to access DeepSeek.

Official resources:

- Node.js: [https://nodejs.org/](https://nodejs.org/)
- Electron: [https://www.electronjs.org/](https://www.electronjs.org/)
- Electron Builder: [https://www.electron.build/](https://www.electron.build/)
- DeepSeek: [https://chat.deepseek.com/](https://chat.deepseek.com/)

## Installation

### 1. Clone the repository

Open PowerShell:

```powershell
git clone https://github.com/YOUR_USERNAME/DeepSeek-Desktop-Electron-Windows.git
```

Move into the project directory:

```powershell
cd DeepSeek-Desktop-Electron-Windows
```

Replace `YOUR_USERNAME` with the actual GitHub account name.

Alternatively, download the repository as a ZIP file and extract it.

### 2. Install dependencies

```powershell
npm.cmd install
```

Using `npm.cmd` avoids some PowerShell execution-policy issues associated with `npm.ps1`.

### 3. Start the application

```powershell
npm.cmd start
```

The Electron application should launch in a new window.

### 4. Sign in to DeepSeek

After launching the application:

1. Wait for the DeepSeek interface to load.
2. Select the sign-in option.
3. Authenticate using a method supported by DeepSeek.
4. Start using the application.

Session persistence depends on DeepSeek's authentication policies and the Electron browser environment.

## Building for Windows

To generate Windows executables, run:

```powershell
npm.cmd run dist:win
```

After a successful build, open the distribution directory:

```powershell
explorer.exe .\dist
```

Depending on the project's Electron Builder configuration, the output may include an installer, a portable executable, or both.

### Alternative startup scripts

If included in your project version, you can also use:

```text
INICIAR_WINDOWS.bat
COMPILAR_EXE_WINDOWS.bat
```

These batch scripts simplify launching and building the application.

## Development Workflow

A recommended workflow for contributing to or modifying this project is:

1. Clone the repository.
2. Install dependencies.
3. Open the project in Visual Studio Code.
4. Create a development branch.
5. Implement your changes.
6. Run available tests and launch the application.
7. Generate an executable to validate the Windows build.
8. Submit a pull request.

For development:

```powershell
code .
npm.cmd start
```

## Troubleshooting

### PowerShell blocks npm.ps1

If PowerShell displays an execution-policy error, use:

```powershell
npm.cmd install
npm.cmd start
```

This avoids changing your system-wide execution policy.

### Electron native binding error

If a native binding cannot be loaded:

1. Verify that you installed a supported Node.js version.
2. Check that the Electron installation completed.
3. Install the Microsoft Visual C++ Redistributable if required.
4. Reinstall the project's dependencies if necessary.

### Login does not work

Some authentication providers restrict sign-in through embedded Chromium environments.

If authentication fails:

- Check whether DeepSeek works in a regular browser.
- Verify your network connection.
- Update project dependencies where appropriate.
- Review Electron console and network errors.

The application cannot guarantee that every login method offered by DeepSeek will function inside Electron.

### Blank window

If the application opens but displays no content:

- Verify internet access.
- Check whether DeepSeek is reachable.
- Review the Electron developer console.
- Investigate possible GPU rendering or browser compatibility issues.

## Privacy and Security

The application uses the official DeepSeek website to provide its chat interface.

Important considerations:

- Messages submitted through the embedded interface are processed by the DeepSeek service according to its policies.
- Session cookies and related browser data may be stored locally by Electron.
- This project does not provide end-to-end encryption for messages sent to DeepSeek.
- Users should avoid publishing session data, credentials, API keys, or personal information in the repository.
- Session persistence is not equivalent to a guarantee of permanent authentication.

For production use, Electron security recommendations should be applied, including process isolation, safe navigation handling, restricted permissions, and regular dependency updates.

## Roadmap

Planned or potential improvements include:

- [ ] Improve the desktop user interface.
- [ ] Add loading indicators and more informative error messages.
- [ ] Improve authentication compatibility where officially supported.
- [ ] Introduce configurable application settings.
- [ ] Improve session management.
- [ ] Add application update notifications.
- [ ] Improve Windows installation and packaging.
- [ ] Add automated tests.
- [ ] Improve error logging and diagnostics.
- [ ] Expand documentation and contribution guidelines.

Roadmap items are proposals, not guarantees of implementation.

## Contributing

Contributions, bug reports, and suggestions are welcome.

To contribute:

1. Fork the repository.
2. Create a feature branch.
3. Make your changes.
4. Test your changes.
5. Open a pull request describing the implementation.

Please avoid including personal authentication tokens, session files, or credentials in issues or pull requests.

## Disclaimer

DeepSeek Desktop for Windows is an unofficial, independent application.

DeepSeek and associated trademarks belong to their respective owners.

This project is provided for software development, learning, and experimentation. Compatibility with the DeepSeek web service may change at any time.

## License

A license has not yet been specified in this README. Add a `LICENSE` file to the repository before declaring an open-source license.

---

**Built with Electron, Node.js, and JavaScript.**
