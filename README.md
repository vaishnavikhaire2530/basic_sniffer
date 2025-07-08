# basic_sniffer
Features:
Captures all live packets on the network interface.
Extracts and displays:
Source and Destination IP addresses
Transport protocol (TCP/UDP/Other)
Source and Destination ports (if TCP or UDP)
Raw payload (up to 50 bytes)
Differentiates between TCP, UDP, and other IP-based traffic.
Handles and prints a simple message for non-IP packets.

How It Works:
The script uses scapy.sniff() to capture packets.
For each captured packet:
It checks if it contains an IP layer.
If present, it prints IP source/destination and protocol number.
It checks for TCP or UDP headers and displays their port info.
If the packet contains raw payload (Raw), it prints the first 50 bytes.
Packets without an IP layer are noted as “Non-IP Packet.”

Usage:
Run the script with Python (requires administrator/root privileges):
bash
Copy
Edit
sudo python packet_sniffer.py
Press Ctrl+C to stop the capture.

Dependencies:
Python 3
Scapy (pip install scapy)
