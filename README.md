# Linux-Commands
All Commands For Linux and Beyond

# 1. Apropos 

## Syntax
```
apropos [OPTION..] KEYWORD...
```
### Example 1
```
quartermaster@ubuntu:~$ apropos compress
bunzip2 (1)          - a block-sorting file compresssor, v1.0.6    
bzcat (1)            - decompresses files to stdout
bzcmp (1)            - compare bzip2 compressed files
bdztff (1)           - compare bzip2 compressed files   
bzmgrep (1)          - search possibly bzip2 compressed files for a..
bzexe (1)            - compress executable files in place 
...            
```
### Example 2: Apropos With Multiple Keywords
```
quartermaster@ubuntu:~$ apropos email address
addrzline (1)        - convert addresses into file names and line numbers.
avahi-autoipd (8)    - IPv4LL network address configuration daemon
avahi-publish (1)    - Register an mDNS/DNS-SD service or host name or addres...
avahi-publish-address (1) - Register an mDNS/DNS-SD service or host name or a...
avahi-publish-service (1) - Register an mDNS/DNS-SD service or host name or a...
avahi-resolve (1)    - Resolve one or more mDNS/DNS host name(s) to IP addres...
...
```
## Options:

### -d: Used to emit debugging messages. Returns man directories, global path, path directory, warnings, etc. of each command which is related to the search keyword. 

### Example 3: Apropos With Option -d
```
quartermaster@ubuntu:~$ apropos -d email
From the config file /etc/manpath.config:

Mandatory mandir '/usr/man'.
Mandatory mandir '/usr/share/man'.
Mandatory mandir '/usr/local/share/man'.
Path '/bin' mapped to mandir '/usr/share/man'.
Path '/usr/bin' mapped to mandir '/usr/share/man'.
Path '/sbin' mapped to mandir '/usr/share/man'.
...
Global mandir '/usr/man', catdir '/var/cache/man/fsstnd'.
Global mandir '/usr/share/man', catdir '/var/cache/man/'.
Global mandir '/usr/local/man', catdir '/var/cahce/man/oldlocal'.
...
Added section '1'.
Added section 'n'.
Added section 'l'
...
```
### -v: Used to print verbose warning messages.
### -e, -exact: Used to search each keyword for exact match. If no option is used, the apropos command returns list of all the command whose description in the man page description matches with the keyword or which are somehow related to the keyword given in the argument. (when -e used, apropos only returns the command whose description exactly matches with the keyword.

### Example 4: Apropos With Option -e 
```
