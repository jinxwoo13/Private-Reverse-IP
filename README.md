# Private Reverse IP Lookup Tool

This tool is a powerful, multi-threaded script designed to perform reverse IP lookups. It scans a list of IP addresses to identify the domains hosted on them using the Private API.

## Features

*   **High-Speed Scanning**: specific multi-threading support to scan multiple IPs simultaneously.
*   **Smart Retry Mechanism**: Includes exponential backoff for handling API timeouts and server errors (500s), ensuring reliable results.
*   **Result Persistence**: Automatically saves found domains to `reversed.txt`.
*   **Telegram Integration**: Option to send the results file directly to your Telegram via Bot API.
*   **Robust Error Handling**: Gracefully handles network errors and invalid inputs.

## Usage

1.  **Prepare your Input**:
    Create a text file (default is `ips.txt`) in the same directory as the script. Add one IP address per line.

    Example `ips.txt`:
    ```text
    192.168.1.1
    10.0.0.1
    172.16.0.1
    ```

2. **For Powershell Executable (.exe):**
    ```powershell
    .\Private Reverse IP.exe
    ```

2. **For CMD Executable (.exe):**
    ```cmd
    Private Reverse IP.exe
    ```

3.  **Follow the Prompts**:
    *   **IP List File**: Press Enter to use the default `ips.txt`, or type the name of your custom file.
    *   **Threads**: Enter the number of concurrent threads you want to use (e.g., 10, 50). Higher numbers speed up scanning but may trigger rate limits.
    *   **Telegram Setup**: (Optional) Enter your Telegram Bot Token and Chat ID to receive the result file via Telegram after the scan completes. Press Enter to skip.

## Output

*   **Console**: Real-time progress showing scanned IPs, found domains count, and errors.
*   **File**: All discovered domains are appended to `reversed.txt` in the script's directory.
*   **Telegram**: If configured, `reversed.txt` is sent as a document to your specified chat.

## Disclaimer

This tool is intended for security research and educational purposes only. The author is not responsible for any misuse of this tool. Use it only on systems you own or have explicit permission to test.
