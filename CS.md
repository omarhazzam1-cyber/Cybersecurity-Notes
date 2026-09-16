\==================== LINUX REVIEW CHEAT SHEET \====================

&nbsp;

## 1\. USERS & GROUPS

| Command/Concept | Description/Details |
| ----- | ----- |
| USER | An account on the Linux machine. |
| GROUP | A collection of users who can share permissions. |
| groupadd developers | Create a group. |
| usermod \-aG developers ahmed | Add Ahmed to the developers group. |
| groups ahmed | See what groups Ahmed belongs to. |
| getent group developers | See the developers group and its members. |
| *WHY IT MATTERS: Groups make it easier to manage access for many users at once.* |  |

## 2\. PERMISSIONS

| Command/Concept | Description/Details |
| ----- | ----- |
| Categories | OWNER | GROUP | OTHERS |
| r, w, x | read (4), write (2), execute (1) |
| 7, 6, 5, 4, 0 | rwx, rw-, r-x, r--, \--- |
| chmod 770 /project | Owner=rwx, Group=rwx, Others=--- |
| chgrp developers /project | Change the group assigned to /project. |
| ls \-ld /project | Check folder's owner, group, and permissions. |
| *WHY IT MATTERS: LEAST PRIVILEGE \- Only give people the access they actually need.* |  |

## 3\. PROCESSES

| Command/Concept | Description/Details |
| ----- | ----- |
| PROCESS / PID | A program running / Process ID (unique number). |
| sleep 300 | Start a process that sleeps for 300 seconds. |
| ps aux | Show running processes. |
| ps aux | grep sleep | Search the process list for "sleep". |
| kill \[PID\] | Stop/terminate the process with the given PID. |
| Ctrl \+ C | Stop a command currently running in the terminal. |
| *WHY IT MATTERS: Useful for troubleshooting and security investigations to know what is running.* |  |

## 4\. NETWORKING

| Command/Concept | Description/Details |
| ----- | ----- |
| ip \-br addr | Show network interfaces and IP addresses. |
| 127.0.0.1 | LOCALHOST \= the machine itself. |
| ping \[IP\] | Test communication with self, VM, or external IPs. |
| Ping Results | Packets transmitted, received, and packet loss. |
| Ping Failure | Doesn't mean offline; could be firewall, routing, etc. |
| *WHY IT MATTERS: Helps diagnose network connectivity issues.* |  |

## 5\. PORTS & SERVICES

| Command/Concept | Description/Details |
| ----- | ----- |
| PORT / SERVICE | Network entry point / Program listening for connections. |
| ss \-tuln | Show listening network ports. |
| ss \-tulnp | Show listening ports \+ associated processes. |
| *WHY IT MATTERS: Helps you see what your machine is listening for.* |  |

## 6\. ECHO & FILE REDIRECTION

| Command/Concept | Description/Details |
| ----- | ----- |
| echo "text" | Display "text" in the terminal. |
| echo "text" \> file | Put "text" into file (OVERWRITES contents). |
| echo "text" \>\> file | Add "text" to END of file (APPENDS contents). |
| cat file | Display the contents of file. |
| *WHY IT MATTERS: Lets you save command output and modify files for automation.* |  |

&nbsp;