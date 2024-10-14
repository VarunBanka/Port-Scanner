# Python Port Scanner

A simple Python-based port scanner to check open ports on target IP addresses. This tool is useful for scanning multiple ports on one or more targets in a quick and easy way.

## Features

- Scans specified number of ports on the target IP addresses.
- Supports scanning multiple targets at once by separating IP addresses with commas.
- Displays open ports in real-time.

## Requirements

- Python 3.x
- The following Python packages are required:
  - `socket`: Standard Python library for network connections.
  - `termcolor`: Used to color terminal output.

The script will attempt to install `termcolor` automatically if it’s not already installed.

## Installation

1. Clone the repository or download the script:

   ```bash
   git clone https://github.com/your-username/port-scanner.git
   ```

2. Navigate to the project folder:

   ```bash
   cd port-scanner
   ```

3. Ensure you have Python 3 installed. You can check the version with:

   ```bash
   python --version
   ```

## Usage

1. Run the script. If  dependencies are not installed, the script will install them automatically:
   ```bash
   python port_scanner.py
   ```

2. Enter the target(s) to scan. You can scan multiple IP addresses by separating them with commas (`,`).

   Example:

   ```
   [*] Enter Targets To Scan (split them by ,): 192.168.1.1, 192.168.1.2
   ```

3. Enter the number of ports you want to scan. For example, to scan the first 1000 ports, enter:

   ```
   [*] Enter How Many Ports You Want To Scan: 1000
   ```

4. The script will then scan the specified ports for each target and display any open ports in the terminal.

   Example output:

   ```
   [+] Port Opened 22
   [+] Port Opened 80
   ```

### Example

Here’s a basic example to scan ports 1-100 on a local machine:

```bash
python port_scanner.py

[*] Enter Targets To Scan (split them by ,): 127.0.0.1
[*] Enter How Many Ports You Want To Scan: 100
```

The script will display open ports like:

```
[+] Port Opened 22
[+] Port Opened 80
```

## Notes

- This script uses a basic try/except block to handle connection errors, meaning it only reports successful connections.
- The scan might take time depending on the number of ports and targets.

## License

This project is licensed under the GNU License. Feel free to use, modify, and distribute this tool.

## Disclaimer

This tool is designed for educational purposes only. Make sure you have permission to scan the targets you're working on.
```