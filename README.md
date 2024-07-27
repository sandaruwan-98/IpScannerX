# IP Address Scanner Tool

This Python script scans a specified range of IP addresses within a network to identify active devices. It sends ping requests to each IP address and determines if the address is active based on the response.

## How It Works

1. **Import Necessary Libraries**:
    - `subprocess`: For executing ping commands.
    - `threading`: For concurrent execution of ping requests.
    - `platform`: To determine the operating system.

2. **Ping Function**:
    - `ping_ip(ip, active_ips)`: Sends a ping request to the given IP address. If the ping is successful, the IP address is added to the `active_ips` list.

3. **IP Scanning Function**:
    - `scan_ips(network_prefix, start_range, end_range)`: Iterates through the specified range of IP addresses and uses threads to ping each address. Limits the number of active threads to avoid overwhelming the system.

4. **Main Execution Block**:
    - Prompts the user for the network prefix and IP range.
    - Calls `scan_ips` to perform the scan and prints the active IP addresses.

## Features

- Scans a specified range of IP addresses within a network.
- Identifies active devices by sending ping requests.
- Uses threading for faster scanning.
- Supports both Windows and Unix-based operating systems.



6. Enter the network prefix (e.g., `192.168.1`).

7. Enter the start and end range for the IP addresses.

8. View the list of active IP addresses.

## Requirements

- Python 3.x
- Administrative privileges (required for pinging on some systems)
