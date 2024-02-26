# Enhanced Secure Password Generator (espg)

This script generates a secure password with a mix of numbers, lowercase and uppercase letters, and special characters, ensuring strong password security. It is designed to work on both macOS and Linux, automatically detecting the operating system to use the appropriate clipboard command and character shuffle utility.

## Features

- Generates a secure password with a specified length between 8 and 64 characters.
- Automatically copies the generated password to the clipboard.
- Outputs a SHA-512 hash of the generated password for verification purposes.

## Requirements

- OpenSSL
- `xclip` for Linux clipboard management or `pbcopy` for macOS.
- `gshuf` (part of `coreutils` on macOS) or `shuf` on Linux for character shuffling.

## Installation

### OpenSSL

OpenSSL is usually pre-installed on Linux and macOS. If for some reason it's missing, you can install it using the following commands:

#### Linux (Debian/Ubuntu)
```bash
sudo apt-get update
sudo apt-get install openssl
```

#### Linux (Fedora)
```bash
sudo dnf install openssl
```

#### macOS
OpenSSL should be pre-installed. If required, it can be installed via Homebrew:
```bash
brew install openssl
```

### Clipboard Utility

#### Linux (xclip)
```bash
sudo apt-get install xclip # Debian/Ubuntu
sudo dnf install xclip     # Fedora
```

#### macOS
`pbcopy` is pre-installed on macOS.

### Coreutils (for gshuf on macOS)
```bash
brew install coreutils
```

## Usage

1. Make the script executable:
   ```bash
   chmod +x espg
   ```

2. Run the script and follow the prompts:
   ```bash
   ./espg
   ```

The script will ask for the desired password length, generate the password, copy it to your clipboard, and display the SHA-512 hash for verification.

Please ensure you paste your password from the clipboard to a secure location immediately after generation.

## Security Disclaimer

This tool is provided "as is", without warranty of any kind. Use of this tool is at your own risk. In no event shall the author or contributors be liable for any claim, damages, or other liability arising from, out of, or in connection with the software or the use or other dealings in the software.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
