Name: Shravani Achal Hendre  
Company: Student  
ID: CT08DU  
Domain: Cyber Security  
Duration: Dec 25 to Jan 25 (4 weeks)  
Mentor: N. Santosh 

**Overview of the Network Vulnerability Scanner Project**  
This project is a simple network vulnerability scanner that performs scans on either IP addresses or URLs to identify potential security risks associated with open ports and outdated software versions. The scanner checks for common vulnerabilities on specific ports and examines web servers for outdated software or misconfigurations. Here's a breakdown of its functionality:

*1. Port Scanning:* 
The scanner checks for common open ports (e.g., FTP, SSH, Telnet, HTTP, HTTPS, etc.). If an open port is detected, it assesses potential vulnerabilities associated with that port (e.g., FTP might allow anonymous login, or SMB could have EternalBlue vulnerabilities).

*2. Vulnerability Identification:* 
For each open port, the scanner prints a list of potential vulnerabilities based on the port being open. Vulnerabilities are predefined for common ports, such as:
- FTP (Port 21) might allow anonymous login.
- SSH (Port 22) might be vulnerable to brute-force attacks if outdated.
- HTTP (Port 80) could be misconfigured or outdated.
- SMB (Port 445) is known for vulnerabilities like EternalBlue.

*3. Web Server Software Check:* 
If a URL is provided, the scanner performs a software check by examining the Server HTTP header. This identifies the web server software (e.g., Apache, Nginx, IIS) and flags potential vulnerabilities related to the server, such as outdated software versions or insecure configurations. If an outdated version of a web server is found, the scanner flags it as a potential risk.

*4. Misconfiguration Detection:* 
The script also checks for possible misconfigurations in the IP address. For instance, if the IP belongs to private IP ranges (e.g., 192.168.x.x or 10.x.x.x), it flags the IP as potentially misconfigured.

*5. Input Validation:*
- The tool validates whether the user input is a valid IP address or a URL, ensuring that only appropriate targets are scanned.
- For IP addresses, it checks if the IP is valid and scans the open ports.
- For URLs, it checks the server version by querying the HTTP header.

*6. Concurrency:* 
Although the script provided does not yet include parallel scanning via ThreadPoolExecutor, the design is laid out in a way that can be enhanced by utilizing threading to speed up the scanning of multiple targets concurrently.

*7. User-Friendly Output:*
1) The scanner outputs a detailed report of its findings, including:
2) Open ports and associated vulnerabilities.
3) Website software details and potential vulnerabilities.
4) Misconfigurations in the network or server setup.

**Key Features:**
- Port scanning to detect common open ports and their associated vulnerabilities.
- Web server software check to identify outdated or insecure versions.
- Misconfiguration detection for private IP ranges and other common misconfigurations.
- User-friendly output with clear reporting of vulnerabilities and misconfigurations.

**Potential Extensions:**
- Multithreading: Improve performance by scanning multiple IPs or URLs concurrently using threading techniques.
- Customizable Ports: Allow users to specify a custom list of ports for scanning.
- Advanced Vulnerability Checks: Integrate with known vulnerability databases (e.g., CVE) to identify specific CVEs associated with the software versions detected.
- Reporting and Logging: Enhance output by saving results to a log file for further analysis or reporting.

**OUTPUT:**
  
  ![image](https://github.com/user-attachments/assets/b2054c9b-8f65-44e0-91ac-419233e002d7)
