# Lab 8 Nmap Network Scanning Enumeration

Objective

This project aimed to build comprehensive skills in network scanning, host discovery, service enumeration, and OS fingerprinting using Nmap. The objective was to identify potential attack surfaces, understanding network behaviors, and gather reconnaissance data, all of which are core tasks for both defenders and attackers. The lab reinforced knowledge of TCP/UDP scanning, service version detection, NSE scripting, and vulnerability mapping.

Skills Learned

- Performing host discovery, port scanning, and full network reconnaissance
- Enumerating open ports, running services, and version information
- Using Nmap scripting Engine (NSE) for vulnerability detection
- Interpreting scan results to identify outdated or misconfigured services
- Understanding how reconnaissance data informs security decisions and investigations

Tools Used

- Nmap (SYN scans, UDP scans, OS detection, version detection)
- NSE scripts for vulnerability assessment and service enumeration
- Linux CLI for managing scan outputs and analyzing results
- Target VMs (Kali, Metasploitable, Metasploitable3) for realistic scanning scenarios

Steps
1. Executed a comprehensive nmap -A scan to perform simultaneous OS detection, full service version fingerprinting, script-based vulnerability checks, and network path tracing.       This combined output identifies exposed services such as Apache, MySQL, OpenSSH, vsFTPd, SMTP, PostgreSQL, and SMB while correlating them to the target operating system and n      network topology to build a complete, end-to-end security profile of the host
   
   <img width="468" height="372" alt="image" src="https://github.com/user-attachments/assets/9bffe9db-51b8-4cbb-a8fd-f56e22eb58f2" />
   <img width="468" height="243" alt="image" src="https://github.com/user-attachments/assets/d72bf552-d8bc-478d-942f-89e487ceda7e" />
   <img width="468" height="209" alt="image" src="https://github.com/user-attachments/assets/0ff84ceb-34f9-4b2b-b700-ff3e9474eb45" />
   <img width="468" height="191" alt="image" src="https://github.com/user-attachments/assets/6d83a51d-c7f0-466e-be10-9ca8afc1eb13" />

2. Identified insecure SMB signing configuration using NSE scripts, exposing the Windows host to potential man-in-the-middle and relay attacks
   
   <img width="468" height="387" alt="image" src="https://github.com/user-attachments/assets/a1a9079e-b511-4960-aaa4-0d692f2d2280" />
   <img width="468" height="216" alt="image" src="https://github.com/user-attachments/assets/ed2ad942-e118-402c-92eb-457c31fd7c5e" />
   
3. Generated an aggregated NSE vulnerability summary report consolidating FTP, SMB, SSH, SQL, Telnet, and RDP security findings into a single analyst-ready output
   
   <img width="468" height="387" alt="image" src="https://github.com/user-attachments/assets/71a7bdce-fd2c-47bb-97cf-15ea253779c7" />
   <img width="468" height="210" alt="image" src="https://github.com/user-attachments/assets/6143a4e1-42ef-40d7-b050-6960e84e67e1" />
   <img width="468" height="427" alt="image" src="https://github.com/user-attachments/assets/4fbd021b-fd4e-4ef4-9952-fae36b72041b" />

4. Performed SMB share enumeration to identify accessible network shares and assess potential lateral movement and data exposure risk
   
   <img width="468" height="183" alt="image" src="https://github.com/user-attachments/assets/457112ec-9283-415b-a550-83f6128ba9ed" />
 
5. Confirmed Windows host vulnerability to EternalBlue (MS17-010) using NSE scripts, identifying active SMBv1 remote code execution exposure
    
   <img width="468" height="183" alt="image" src="https://github.com/user-attachments/assets/b4881d62-19c4-4de9-aa67-a7303855ed83" />
 
6. Documented a full attack path analysis mapping how exposed Linux and Windows services—including SMB, RDP, and outdated daemons—could be chained together during an intrusion
    
    <img width="468" height="216" alt="image" src="https://github.com/user-attachments/assets/4f96d22e-60e3-4c5b-ae2a-005eadedbe81" />
    <img width="468" height="216" alt="image" src="https://github.com/user-attachments/assets/b7b73af9-d4ff-4ab3-a331-86e853b0c121" />

7. Recorded final NSE challenge validation and proof-of-vulnerability output confirming that anonymous FTP access was properly restricted while the Windows host remained
   vulnerable to EternalBlue (MS17-010). These final results provide high-confidence verification of active SMBv1 remote code execution risk, solidifying the exploitation findings
   and reinforcing the urgency of proper patching and SMB hardening.

    <img width="468" height="342" alt="image" src="https://github.com/user-attachments/assets/018837bd-76de-4a4d-a087-501c4a650323" />
    <img width="468" height="271" alt="image" src="https://github.com/user-attachments/assets/b2250204-c4bb-40f4-8adb-e28f7a452a4a" />
    
