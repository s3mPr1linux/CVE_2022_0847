# CVE-2022-0847-DirtyPipe-Exploits
A collection of exploits and documentationi for penetration testers and red teamers that can be used to aid the exploitation of the Linux Dirty Pipe vulnerability.

# About The Vulnerability
- Dirty Pipe (CVE-2022-0847) is a local privilege escalation vulnerability in the Linux kernel that could potentially allow an unprivileged user to do the following:
	- Modify/overwrite arbitrary read-only files like /etc/shadow or /etc/passwd. 
	- Obtain an elevated shell.

## Affected versions
- Linux kernel versions newer than 5.8 are affected.
- So far the vulnerability has been patched in the following Linux kernel versions:
	- 5.16.11
	- 5.15.25
	- 5.10.102
- You can learn more about the vulnerability here: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-0847

# DirtyPipe Vulnerability Scanner
- If you are not sure if a target system is vulnerable, use this really cool bash script developed by @basharkey.
- DirtyPipe Checker: https://github.com/basharkey/CVE-2022-0847-dirty-pipe-checker

# Modifying/overwriting read only files
- This repo contains 2 exploits, the 'new-user.c' exploit can be used to modify or overwrite arbitrary read only files.
- This exploit is a proof of concept that was developed by Max Kellermann and has been modified to add a new user account with root privileges, consequently providing you with an elevated session.
 

## Important Note 
- I do not claim credit/ownership/disclosure of the vulnerability and all corresponding exploits hosted in this GitHub repo.
- All the credit goes to the awesome Max Kellerman, you can check out the official disclosure here: https://dirtypipe.cm4all.com/
