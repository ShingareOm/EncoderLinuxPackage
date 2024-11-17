# Encoder Electron App (Package created using ChatGPT) 

This is an **Electron** application that wraps the **Encoder ReactJS** project, which allows users to encode and decode text using various encoding formats such as Uppercase, Lowercase, SHA256, and Base64.

The Electron app provides a desktop version of the React-based web application, making it easily accessible on your local machine without needing a browser.

## Features

- **Text Encoding Options**:
  - Uppercase
  - Lowercase
  - SHA256
  - Base64 Encoding/Decoding
- **Desktop Application**: A native desktop application built with Electron.
- **Responsive UI**: Responsive design for a seamless user experience.
- **State Management**: Uses React's `useState` hook for managing state in the app.
- **Event Handling**: Handles user inputs and actions effectively.

## Technologies Used

- **ReactJS**: JavaScript library for building user interfaces.
- **Electron**: Framework for building cross-platform desktop apps using web technologies (HTML, CSS, and JavaScript).
- **Bootstrap**: CSS framework for building responsive, mobile-first websites.
- **CryptoJS**: JavaScript library for cryptographic algorithms (used for SHA256 encoding).
- **Base64 Encoding/Decoding**: Used for encoding/decoding data in Base64 format.

## Demo

You can check out the live demo of the web version of this application [here](https://encoder-topaz.vercel.app).

## Getting Started

To get started with the **Electron** version of the app, follow these instructions:

### Requirements

Before proceeding with the build process, make sure you have the following installed:

1. **Electron** – for building the Electron app.
2. **Electron Packager** – for packaging the app into distributable formats.
3. **Electron Debian Installer** – for creating `.deb` installer packages for Debian-based systems.
4. nodejs and npm installed

### Step-by-Step to complete the requirement

#### 1. **Install Electron**

To install Electron globally, run the following command:

```bash
sudo npm install -g electron --unsafe-perm=true
```

> **Note**: The `--unsafe-perm=true` flag is sometimes necessary for some Linux environments (particularly with system-level dependencies).

#### 2. **Install Electron Debian Installer**

To create `.deb` installer packages for your app, install the **electron-installer-debian** package globally:

```bash
sudo npm install -g electron-installer-debian
```

#### 3. **Install Electron Packager**

**Electron Packager** is used for packaging your Electron app into a distributable format for different platforms. Install it globally:

```bash
sudo npm install -g electron-packager
```

---

### Verify Installation

To verify that the tools are installed correctly, you can check their versions:

```bash
electron --version
electron-packager --version
electron-installer-debian --version
```

---

### Summary of Commands:

```bash
# Install Electron
sudo npm install -g electron --unsafe-perm=true

# Install Electron Debian Installer
sudo npm install -g electron-installer-debian

# Install Electron Packager
sudo npm install -g electron-packager
```
---

# Installation

### 1. Clone the Repository

Clone the repository from GitHub:

```bash
git clone https://github.com/mskian/electron-example.git
cd electron-example
```

### 2. Install Dependencies

Install the required dependencies using **Yarn**:

```bash
yarn install
```

### 3. Build the Electron Package for Linux

To package the Electron app for Linux, run:

```bash
yarn package-linux
```

This will generate the necessary files to distribute your application on Linux.

### 4. Build the `.deb` Installer Package

To create a `.deb` installer package for your Linux distribution, run:

```bash
yarn create-debian-installer
```

This will generate a `.deb` file that you can use to install the app on a Linux system.

---

### Summary of Commands:

```bash
git clone https://github.com/mskian/electron-example.git
cd electron-example
yarn install
yarn package-linux
yarn create-debian-installer
```



### Usage

1. Open the Electron application.
2. Enter the text you want to encode or decode in the input box.
3. Choose one of the encoding options:
   - Uppercase: Converts the text to uppercase letters.
   - Lowercase: Converts the text to lowercase letters.
   - SHA256: Applies SHA256 hashing to the text.
   - Base64 Encode: Encodes the text into Base64 format.
   - Base64 Decode: Decodes the Base64 encoded text back to the original format.
4. The result will be displayed below the input field.

## Code Overview

- **main.js**: This is the entry point for the Electron app. It initializes and opens the Electron window.
- **src/App.js**: The main React component that handles the UI and user interaction.
- **TextForms.js**: Contains utility functions for encoding/decoding text.
  - `toUppercase`: Converts the input text to uppercase.
  - `toLowercase`: Converts the input text to lowercase.
  - `toSHA256`: Hashes the input text using SHA256.
  - `toBase64`: Encodes the text to Base64.
  - `fromBase64`: Decodes the Base64 text back to the original format.

## Future Enhancements

- Improve UI/UX design for better user interaction.
- Add additional encoding/decoding methods.
- Provide better error handling and validations for inputs.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## About

This is a simple desktop application built using **ReactJS** and **Electron** for encoding/decoding text in various formats.
