# Hare Krishna
# Red-Hat---Linux

## Linux commands
```
 1. [user@host]$ whoami
     user
     
 2. Combine two commands
    [user@host]$ command1;command2
    
 3. [user@host ~]$ date
     wed May 26 08:13:50 IST 2021
    [user@host ~]$ date +%R
     08:13
    [user@host ~]$ date +%r
     10:14:07 AM
    [user@host ~]$ date +%x
     05/26/2021
     
 4. [user@host ~]$ passwd
    Changing password for user user.
    Current password: old_password
    New password: new_password
    Retype new password: new_password
    passwd: all authentication tokens updated successfully.
    
 5. The file command scans the
    beginning of a file's contents and displays what type it is.
    
    [user@host ~]$ file /etc/passwd
    /etc/passwd: ASCII text
    [user@host ~]$ file /bin/passwd
    /bin/passwd: setuid ELF 64-bit LSB shared object, x86-64, version 1
    (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2,
    for GNU/Linux 3.2.0, BuildID[sha1]=a3637110e27e9a48dced9f38b4ae43388d32d0e4,
    stripped
    [user@host ~]$ file /home
    /home: directory
    
  6. The cat command allows you to create single or multiple files, view the contents of files, concatenate the contents from
     multiple files, and redirect contents of the file to a terminal or files.
      
     [user@host ~]$ cat /etc/passwd     // view the content of file
     root:x:0:0:root:/root:/bin/bash
     bin:x:1:1:bin:/bin:/sbin/nologin
     daemon:x:2:2:daemon:/sbin:/sbin/nologin
     
     [user@host ~]$ cat file1 file2 // display content of multiple files
     
  7. head /etc/passwd  //  by default top 10 lines
     [user@host ~]$ tail -n 3 /etc/passwd    // bottom 3 lines
     
  8. The wc command counts lines, words, and characters in a file. It takes a -l, -w, or -c option to
     display only the number of lines, words, or characters, respectively.
     
     [user@host ~]$ wc /etc/passwd
      45 102 2480 /etc/passwd
     [user@host ~]$ wc -l /etc/passwd ; wc -l /etc/group
     45 /etc/passwd
     70 /etc/group
     [user@host ~]$ wc -c /etc/group /etc/hosts
     966 /etc/group
     516 /etc/hosts
     1482 total
     
  9. Tab completion - It allows a user to quickly complete commands or file names after they have typed
     enough at the prompt to make it unique. If the characters typed are not unique, pressing the Tab
     key twice displays all commands that begin with the characters already typed.
     
     [user@host ~]$ pas Tab+Tab
     passwd paste pasuspender
     [user@host ~]$ pass Tab
     [user@host ~]$ passwd
     Changing password for user user.
     Current password: 
     
 10. Continuing a Long Command on Another Line
 
     [user@host]$ head -n 3 \
     > /usr/share/dict/words \
     > /usr/share/dict/linux.words

 11. history
 
     The !number command expands to the command matching the number specified. The !string command 
     expands to the most recent command that begins with the string specified.
 
 12. Ctrl+A - Jump to the beginning of the command line.
     Ctrl+E - Jump to the end of the command line.
     Ctrl+U - Clear from the cursor to the beginning of the command line.
     Ctrl+K - Clear from the cursor to the end of the command line.
     Ctrl+LeftArrow - Jump to the beginning of the previous word on the command line.
     Ctrl+RightArrow - Jump to the end of the next word on the command line.
     Ctrl+R - Search the history list of commands for a pattern.
     
 13. Esc+ copies the last argument of previous commands.

```
## Managing Files From Command Line-

```
Important Red Hat Enterprise Linux Directories
Location      -       Purpose
/usr - Installed software, shared libraries, include files, and read-only program data.
Important subdirectories include:
• /usr/bin: User commands.
• /usr/sbin: System administration commands.
• /usr/local: Locally customized software.
/etc - Configuration files specific to this system.
/var - Variable data specific to this system that should persist between boots. Files
that dynamically change, such as databases, cache directories, log files,
printer-spooled documents, and website content may be found under /var.
/run - Runtime data for processes started since the last boot. This includes process
ID files and lock files, among other things. The contents of this directory are
recreated on reboot. This directory consolidates /var/run and /var/lock
from earlier versions of Red Hat Enterprise Linux.
/home - Home directories are where regular users store their personal data and
configuration files.
/root - Home directory for the administrative superuser, root.
/tmp - A world-writable space for temporary files. Files which have not been
accessed, changed, or modified for 10 days are deleted from this directory
automatically. Another temporary directory exists, /var/tmp, in which files
that have not been accessed, changed, or modified in more than 30 days are
deleted automatically.
/boot - Files needed in order to start the boot process.
/dev - Contains special device files that are used by the system to access hardware.

```
#### Navigating paths

```

1. The pwd command displays the full path name of the current working directory for that shell.
2. The ls command lists directory contents for the specified directory or, if no directory is given, for the current working directory.
[user@host ~]$ pwd
/home/user
[user@host ~]$ ls
Desktop Documents Downloads Music videos

3. Use the cd command to change your shell's current working directory.
 [user@host ~]$ cd Videos
 [user@host Videos]$ pwd
 /home/user/Videos

4. The touch command normally updates a file's timestamp to the current date and time
   without otherwise modifying it.




```
 
