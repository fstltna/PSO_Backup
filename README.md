# PSO Backup - backup script for Phantasy Star Online Servers on Linux (1.0.0)
Creates a hot backup of your PSO Server and optionally copies it to a offsite server.

Official support sites: [Official Github Repo](https://github.com/fstltna/SyncBackup) - [Official Forum](https://pso.gameplayer.club/index.php/forum/server-tools) 

---

1. Make sure ssh-keygen is installed: "apt install ssh-keygen"
2. Run "ssh-keygen" and when asked for the password just press enter twice
3. Run "ssh-copy-id -i ~/.ssh/id_rsa.pub your-destination-server" - This will ask you for your remote password. This is normal.
4. Edit the settings at the top of psobackup.pl if needed
5. After the first run edit the ~/.psobackuprc and change your settings if you want to use the offsite backup feature. The next run it should save to your remote host.
6. create a cron job like this:

        1 1 * * * ~/PSO_Backup/psobackup.pl

7. This will back up your PSO installation at 1:01am each day, and keep the last 5 backups.

If you need more help visit https://pso.gameplayer.club/index.php/forum/server-tools and check out this website: https://superuser.com/questions/555799/how-to-setup-rsync-without-password-with-ssh-on-unix-linux
