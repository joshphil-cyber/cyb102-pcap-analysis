# Project 1 - Catch Me If You Can!
Business Email Compromises (BECs) are responsible for many phishing scams, incurring billions of dollars of losses. In this simulated activity, I inspected `.pcap` files using Wireshark to determine which emails are fraudulent and which cars are legitimate.
***
## Goals
- Inspect `.pcap` files and extract their email content
- Identify legitimate vs fraudulent emails
- Correctly identify the bad actor

## Tools
- **Ubuntu VM (Microsoft Azure)**: safe environment to handle malicious email traffic
- **Wireshark**: packet sniffing tool used to inspect `.pcap` files
- **Mozilla Thunderbird**: Mozilla's email client which is compatible with Ubuntu Linux, used to read `.eml` files

## Process
1. Filters:
    - `smtp`
    - `smtp.data.fragment`  
      These filters were used to single out SMTP packets out of all the network traffic.

2. Email Reconstruction
    - On Wireshark, followed TCP stream of SMTP packets to view the full email message.

3. Key Indicators of Phishing
    - Suspicious subjects
    - Malicious IP addresses

4. Identified Bad Actor
    - Traced suspicious `smtp` packets to find a single attacker's IP


## Key Findings
**Malicious IP**: 10.6.1.104

**Subject lines of three phishing emails**:
- Read carefully! - dayrit
- Your private data! - 2645885
- Safe your privacy! - incretible

## Screenshots
On Wireshark, exported IMF object to obtain `.eml` file

Used **Mozilla Thunderbird** as email client to view the email messages contained in the `.eml` files.

![Screenshot 1](Screenshots/em1.png)

![Screenshot 2](Screenshots/em2.png)

![Screenshot 3](Screenshots/em3.png)
## Reflection
This project helped me understand how attackers exploit SMTP protocols, and how blue team cybersecurity specialists can use tools like Wireshark to sniff packets and analyze network traffic.

I developed skills in
- Email Forensics
- Packet Sniffing
- Packet Filtering
- Email Reconstruction
- Identifying malicious network traffic
