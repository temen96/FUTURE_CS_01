🧃 Web Application Penetration Testing Report

OWASP Juice Shop



👤 Student Information
 • Name: Temen Alemayehu
 • Course: Cyber Security Internship – Task 1
 • Date: March 19, 2026



📌 Project Overview

This project presents a web application penetration testing assessment conducted on OWASP Juice Shop, a deliberately vulnerable application designed for security training.

The goal of this task was to identify, exploit, and document common web vulnerabilities based on the OWASP Top 10.



🎯 Objectives
 • Identify security vulnerabilities in the application
 • Perform exploitation of discovered issues
 • Intercept and analyze HTTP traffic
 • Provide remediation and security recommendations



🧪 Testing Environment
 • Operating System: Kali Linux
 • Browser: Mozilla Firefox
 • Target Application: OWASP Juice Shop (Localhost)



🛠️ Tools Used
 • Burp Suite – Intercepting and modifying HTTP requests
 • Mozilla Firefox – Web browsing and testing
 • Kali Linux – Penetration testing platform



🔍 Methodology

The testing process followed a structured penetration testing approach:
 1. Reconnaissance
 • Explored application features and functionality
 2. Interception
 • Configured proxy and captured HTTP traffic using Burp Suite
 3. Analysis
 • Examined requests and responses for vulnerabilities
 4. Exploitation
 • Performed IDOR attack
 • Executed XSS payload injection
 5. Documentation
 • Recorded findings and captured evidence



🚨 Vulnerabilities Identified

🔴 Insecure Direct Object Reference (IDOR)
 • Unauthorized access to other users’ data by modifying request parameters
 • Example: Changing /rest/basket/6 to /rest/basket/5

Impact:
 • Exposure of sensitive user data
 • Privacy violation



🟠 Cross-Site Scripting (XSS)
 • Injection of malicious JavaScript into user input fields

Payload Used:
       <script>alert('XSS')</script>
  Impact:
 • Execution of malicious scripts
 • Session hijacking and phishing risks



🟡 Traffic Interception & Analysis
 • Successfully intercepted HTTP requests using Burp Suite

Observed Endpoints:
 • /rest/products
 • /rest/basket/{id}



📸 Screenshots

All evidence is available in the screenshots/ directory, including:
 • Burp Suite interception
 • IDOR request manipulation
 • XSS payload execution     
⚠️ Risk Summary
 Vulnerability         Severity         Risk Level     
IDOR                    High             Critical
XSS                     Medium           Moderate
Traffic Analysis        Low              Informational 
🛡️ Recommendations
 • Implement proper authorization checks
 • Validate and sanitize all user inputs
 • Apply output encoding
 • Use Content Security Policy (CSP)
 • Conduct regular security testing



📄 Report

The full detailed report is available in the report/ directory.



🏁 Conclusion

This assessment revealed critical vulnerabilities that could compromise user data and system security. Fixing these issues will significantly improve the application’s security posture.



⚡ Author Note

This project is part of a cybersecurity internship task and is intended for educational purposes only.
