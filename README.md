## Bash Backup Script

### Description
This script provides functionality to back up files and directories either locally on your device or to a remote server via SSH using `scp`. You can select to back up folders or files either on the local device or over the network to other servers. The script creates a compressed `.tar.gz` backup file and stores logs with details of the backup process.

### Features
- **Local Backup:** Allows you to choose files or directories to back up on your local device.
- **Remote Backup:** Provides the option to back up to a remote server via SSH, using the `scp` protocol.
- **Event Logging:** All backup-related events are logged in a file for tracking operations and potential issues.
- **Flexible Functions:** Supports backup of both folders and files, whether they are on the local device or on remote servers.
- **Compression:** The script compresses the backups using `tar` to `.tar.gz` format.

### How to Use
1. **Local Backup:**
   - You will be prompted to enter the path of the file or directory you want to back up.
   - Then, you will be asked to specify the destination path to store the backup.
   - The script will create the backup locally in the specified destination folder.
[backup1](backup1.png)
2. **Remote Backup:**
   - In this case, you’ll enter the path on your local device, the remote destination path, and the IP address and user of the remote server.
   - The file or directory will be backed up and transferred to the remote server using `scp`.
[backup2](backup2.png)
### Requirements
- **SSH Access:** The remote server should be configured to accept SSH connections.
- **Tools:** Ensure that the tools `scp` and `tar` are available on your system.
- **Permissions:** You need the necessary permissions to access the required files on your system and enough privileges to run scripts and perform backups.

### How to Install
1. Clone the repository to your machine:
    ```bash
    git clone https://github.com/username/repository-name.git
    cd repository-name
    ```

2. Make the script executable:
    ```bash
    chmod +x backup.sh
    ```

3. Run the script:
    ```bash
    ./backup.sh
    ```

### Notes
- Ensure that remote servers are reachable via SSH.
- The script creates a `.tar.gz` backup file, temporarily stored in `/tmp/` before being transferred to the destination.
