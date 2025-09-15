# Commands
**File & Directory Management**
```groovy
ls -l         # List files with details
ls -la        # List all files including hidden
cd /path      # Change directory
pwd           # Print current directory
mkdir logs    # Create a new directory
rm -rf dir/   # Remove directory forcefully
cp file1 file2   # Copy files
mv file1 file2   # Move/Rename file
```

**File Viewing & Editing**
```groovy
cat file.log         # View file content
less file.log        # Scroll through file (quits with 'q')
tail -f file.log     # View live logs (useful for apps)
head -n 20 file.log  # View first 20 lines
nano file.txt        # Edit file in nano editor
vim file.txt         # Edit file in vim
```

**Searching & Filtering (Logs / Configs)**
```groovy
grep "ERROR" app.log          # Search for "ERROR" in logs
grep -i "error" app.log       # Case-insensitive search
grep -r "DB_HOST" /etc/       # Recursive search in config files
awk '{print $1}' access.log   # Extract first column
sed 's/foo/bar/g' file.txt    # Replace foo with bar
sort file.txt | uniq -c       # Sort + count unique entries
```

**Process & Resource Management**
```groovy
ps aux                # List all running processes
top                   # Real-time system processes
htop                  # Better process monitor (if installed)
kill -9 <PID>         # Kill process forcefully
df -h                 # Check disk usage
du -sh *              # Size of files/folders in directory
free -m               # Memory usage
uptime                # System load & uptime
```

**User & Permission Management**
```groovy
whoami                # Current user
id                    # User & group info
chmod 755 file.sh     # Change file permissions
chown user:group file # Change ownership
sudo su -             # Switch to root
adduser devops        # Add new user
passwd devops         # Set password
```


**Networking (Servers & Connectivity)**
```groovy
ping google.com            # Check connectivity
curl -I http://app.com     # Test HTTP headers
wget http://file.tar.gz    # Download file
netstat -tulnp             # Check open ports (deprecated in some distros)
ss -tulnp                  # Alternative to netstat
telnet host 22             # Test connectivity to a port
nc -zv host 80             # Netcat port test
```

**Services & Systemd**
```groovy
systemctl status nginx     # Check service status
systemctl start nginx      # Start service
systemctl stop nginx       # Stop service
systemctl restart nginx    # Restart service
journalctl -u nginx -f     # View live service logs
systemctl list-unit-files  #  all available systemd unit files
```

**Compression & Archives**
```groovy
tar -cvf logs.tar logs/    # Create tar archive
tar -xvf logs.tar          # Extract tar archive
gzip file.txt              # Compress file
gunzip file.txt.gz         # Decompress file
```

**SSH & Remote Management**
```groovy
ssh user@server           # SSH into server
scp file user@server:/tmp # Copy file to remote server
rsync -avz dir/ server:/backup/   # Sync files efficiently
```

**Docker & Containers (common for DevOps)**
```groovy
docker ps                # List running containers
docker images            # List images
docker logs -f <id>      # View container logs
docker exec -it <id> sh  # Get shell into container
docker stop <id>         # Stop container
docker rm <id>           # Remove container
```
