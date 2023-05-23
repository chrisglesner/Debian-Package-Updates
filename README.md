# Debian-Package-Updates
Verifies internet connectivity via pings. If successful, then runs 'apt-get update' and 'apt-get upgrade'. If pings aren't successful, then the script closes.

I set this up as a cronjob as a root user. 

Please note that there could potentially be a few security risks.
  a) This script will auto-install any packages obtained from the repository. This is done with the '-y' flag attached to the 'apt-get upgrade' command. Administrators should be careful with exactly which packages they're installing on their systems.
  b) Running cronjobs as the 'root' user could prove fatal if a threat actor gains control over the cronjob and subsequently has full administrative privileges. [
  
 By running this script, you incur this risk. I have this ran on a VM.
