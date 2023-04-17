# Ethical-Hacking-Checklist

Ensure you have permission before conducting any testing!

1. Reconnaissance
   a. Passive
      - Google Dorking: `site:example.com, inurl, intext, etc.`
      - WHOIS Lookup: `whois example.com`
      - DNS Recon: `dnsrecon -d example.com`
   b. Active
      - Nmap: `nmap -sn <IP_range>` (ping sweep)
      - Nmap: `nmap -p- <target_IP>` (port scanning)

2. Enumeration
   a. DNS Enumeration
      - Dig: `dig @<DNS_server> example.com AXFR`
      - Nmap: `nmap --script dns-brute <target_IP>`
   b. SMB Enumeration
      - Nmap: `nmap --script smb-enum-shares <target_IP>`
      - Smbclient: `smbclient \\\\<target_IP>\\<share_name> -U <username>`
   c. SNMP Enumeration
      - Snmpwalk: `snmpwalk -c public -v1 <target_IP>`
      - Onesixtyone: `onesixtyone <target_IP>`
   d. Web Application Enumeration
      - Nikto: `nikto -h <target_URL>`
      - Dirb: `dirb <target_URL>`

3. Vulnerability Assessment
   a. Nmap NSE Scripts
      - Nmap: `nmap --script vuln <target_IP>`
   b. OpenVAS
      - Setup and run OpenVAS on target systems
   c. Metasploit Framework
      - Search for modules: `search <vulnerability>`
      - Use a module: `use <module_name>`

4. Exploitation
   a. Metasploit Framework
      - Set options: `set <option> <value>`
      - Run exploit: `exploit or run`
   b. Manual Exploitation
      - Research and use known exploits for identified vulnerabilities
   c. Web Application Exploitation
      - SQL Injection: `sqlmap -u <target_URL>`
      - XSS: Test payloads, use automated tools like `XSStrike`

5. Post-Exploitation
   a. Privilege Escalation
      - Linux: `linPEAS, LinEnum`
      - Windows: `winPEAS, PowerUp, Sherlock`
   b. Lateral Movement
      - PsExec: `psexec.py <username>:<password>@<target_IP>`
      - Mimikatz: `sekurlsa::logonpasswords`
   c. Data Exfiltration
      - Identify and collect sensitive information

6. Clean Up
   a. Remove artifacts, backdoors, and logs

7. Reporting
   a. Document findings, recommendations, and mitigations

----- End of Checklist -----
