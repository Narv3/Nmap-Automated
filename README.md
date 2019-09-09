# Nmap-Automated
nmap script that automates scanning as well as for vulns.
Helpful for scanning on HTB and OSCP practice machines.

# In-Progress:
Fixing errors with checking CVEs as well as goBuster when used with hosts that redirect. 
Working on adding more features... (dirb and other fun things)


# Features:
1. **Quick:**	Shows all open ports quickly (~15 seconds)  
1. **Basic:**	Runs Quick Scan, then a runs more thorough scan on found ports (~5 minutes)  
1. **UDP:**	  Runs "Basic" on UDP ports (~5 minutes)  
1. **Full:** 	Runs a full range port scan, then runs a thorough scan on new ports (~5-10 minutes)  
1. **Vulns:**	Runs CVE scan and nmap Vulns scan on all found ports (~5-15 minutes)  
1. **Recon:**	Runs "Basic" scan "if not yet run", then suggests recon commands "i.e. gobuster, nikto, smbmap" based on the found ports, then prompts to automatically run them  
1. **All:**  	Runs all the scans consecutively (~20-30 minutes)  
   
# Requirements:
**Required:** Gobuster v3.0 or higher, as it is not backward compatible.  
You can update gobuster on kali using:  
```
apt-get update
apt-get install gobuster --only-upgrade  
```
**Recommended:** nmap vulners scrip "for CVE scan"  
https://github.com/vulnersCom/nmap-vulners  
  
  
# Examples of use:
./nmap.sh <TARGET-IP> <TYPE>  
./nmap.sh 10.1.1.1 All  
./nmap.sh 10.1.1.1 Basic  
./nmap.sh 10.1.1.1 Recon  

**If you want to use it anywhere on the system, create a shortcut using:**  
```ln -s /PATH-TO-FOLDER/nmapAutomator.sh /usr/local/bin/```

Disclaimer:
Thanks to (21y4d) for the original script.  
