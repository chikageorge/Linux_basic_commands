# Linux Commands Fundamentals

## What is a Linux Command?
<p>A Linux command refers to a program or utility that runs in the command-line interface (CLI). The CLI is a text-based environment where you interact with the system by typing commands.

Linux commands are executed by entering text in the Terminal and pressing Enter. These commands enable you to perform a wide range of tasks, including installing packages, managing users, manipulating files and directories, configuring system settings, and more.</p>

The general syntax of a Linux command is as follows:

```bash
CommandName [option(s)] [parameter(s)]
```
## Command Components

A command may consist of options and parameters, but they are not always required.

**CommandName:** Represents the action or task you want to perform (e.g., ls to list files).

Option or Flag: Modifies the behavior of a command, typically preceded by *- or -- (e.g., ls -l shows extra information).*

**Parameter or Argument:** Provides specific information required by the command (e.g., mkdir photos creates a "photos" directory).

*Note: Linux commands are case-sensitive.
The sudo Command*

**"sudo"** stands for **"superuser do,"** allowing you to run commands with root privileges.

Why Use sudo?

- Security: Limits access to powerful commands

- Tracking: Logs who executed which command

When you use sudo, Linux asks for your password. Privileges typically last 15 minutes.

*Example: Creating a folder with sudo*
``` bash
mkdir /root/example  # Fails with "Permission denied"
sudo mkdir /root/example  # Succeeds
sudo ls /root  # Verify creation
```
Basic Navigation Commands
- pwd - Print Working Directory\
*Use the following to Shows your current directory path:*
``` bash
pwd
```
# Example output: /home/username

Linux Directory Structure

Key directories under root (/):

- /bin: Essential command binaries

- /etc: Configuration files

- /home: User directories

- /root: Root user's home

- /var: Variable data like logs

- /usr: User utilities and applications

*cd - Change Directory and Navigate the filesystem:*
``` bash
cd /  # Go to root directory
cd /usr  # Enter /usr directory
```
*File Operations Commands*
ls - List Directory Contents
``` bash
ls  # List current directory
ls /home/ubuntu/Documents  # List specific directory
ls -R  # List recursively
ls -a  # Show hidden files
ls -lh  # Human-readable sizes
```
**cat - Concatenate Files**
Display file contents:
``` bash
cat filename.txt
sudo cat /etc/os-release  # View system info
```
**cp - Copy Files/Directories**
``` bash
cp file.txt /destination/  # Copy file
cp file1.txt file2.txt file3.txt /destination/  # Multiple files
cp -R /source/ /backup/  # Copy directory recursively
```
**mv - Move/Rename Files**
``` bash
mv file.txt /new/location/  # Move file
mv oldname.txt newname.txt  # Rename file
```
**rm - Remove Files**
Caution: Permanent deletion!
``` bash
rm file.txt  # Delete file
rm -i file.txt  # Confirm before deleting
rm -f file.txt  # Force delete
rm -r directory/  # Delete directory recursively
```
**touch - Create Empty File**
``` bash
ouch newfile.txt
touch /path/to/file.html
```
**find - Search for Files**
``` bash
find /home -name notes.txt  # Search by name
find / -type d -name photos  # Search directories
```
## Practical Task

### Step 1: Create a directory called photos inside /usr:
``` bash
    sudo mkdir /usr/photos
```
### Step 2: Navigate into it:
``` bash
    cd /usr/photos
```
### Step 3: Create 3 subdirectories:
``` bash
    mkdir dir1 dir2 dir3
```
### Step 4: Show the new directories:
``` bash
    ls
```
### Step 5: Navigate into one and show path:
``` bash
    cd dir1
    pwd
```
Summary
These fundamental commands form the basis of Linux system navigation and file management. Always use sudo cautiously and double-check rm commands to prevent accidental data loss.