# testinternet
Bash script to monitor internet connectivity on Linux systems

Attempts to ping 8.8.8.8 (Google's DNS service).
If the status changes (online, offline), it outputs the information suitable for a log and also emails someone.

Maintains a state file so can detect how long it has been since the last change.

# Usage
Edit the first few lines to set EMAIL and optionally the IP address to ping and location of statefile.

Use it in a cron job run every minute, eg.
```cron
# Every minute test internet connection
* * * * * $HOME/bin/testinternet >> $HOME/logs/testinternet.log
```

# Notes
This has been tested on gentoo with bash-4.4
