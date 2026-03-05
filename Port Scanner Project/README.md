# Comparing Port Scanners
This project is designed to develop two types of port scanners and compare the performance of both. Both scanners scan "scanme.org" to test if the scanner operates as intended. 

## Project Overview
- Developed an Nmap-based port scanner and service scanner that actively probes ports and applies built-in service detection techniques. 
- Developed a custom TCP socket-based scanner that performs basic TCP connect scans.
- Scans for open ports 


## Project Structure and Logic

### Nmap-Based Port Scanner
- **Path:** `Port Scanner Project\Nmap_Port_Scanner.py`
- Scans the target host with service/version detection and automatically checks all ports.
- Automatically integrates banner detection for all open ports. 
- Validates if there is any banner information.
- Outputs the open port number and banner information, inclduing the product, version, and any extra information if provided.
- Displays the time the scanner took to scan the target host.

### Custom TCP-Based Port Scanner
- **Path:** `Port Scanner Project\Socket_Port_Scanner.py`
- Manually scans all ports ranging from 1 to 65535.
- Sends an HTTP GET request for banner grabbing so it can retrive the service banner of ports that do not automiatically send a response upon connection.
- Displays only the header if the banner retrieved has HTTP header/body, otherwise it displays the whole banner.
- Implements threading to improve the scanner's effiency
- Displays the time the scanner took to scan the target host.

## How to Run
Be in the root directory

### Prerequisites
```bash
git clone https://github.com/hhemen101/AIM-PQC-Projects/tree/main
```
- Make sure Nmap itself is downloaded on host machine. https://nmap.org/download.html 
```bash
pip install python-nmap
```