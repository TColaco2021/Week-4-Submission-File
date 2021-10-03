# Week-4-Submission-File: Linux Systems Administration

### Step 1: Ensure/Double Check Permissions on Sensitive Files

Permissions on /etc/shadow should allow only root read and write access.

Command to inspect permissions: ls -l /etc/shadow.

Command to set permissions (if needed): sudo chmod u=rw /etc/shadow

Permissions on /etc/gshadow should allow only root read and write access.

Command to inspect permissions: ls -l /etc/gshadow

Command to set permissions (if needed): sudo chmod u=rw /etc/gshadow

Permissions on /etc/group should allow root read and write access, and allow everyone else read access only.

Command to inspect permissions: ls -l /etc/group

Command to set permissions (if needed): sudo chmod u=rw,g=r,o=r /etc/group

Permissions on /etc/passwd should allow root read and write access, and allow everyone else read access only.

Command to inspect permissions: ls -l /etc/passwd

Command to set permissions (if needed): sudo chmod u=rw,g=r,o=r /etc/passwd
 
### Step 2: Create User Accounts

Add user accounts for sam, joe, amy, sara, and admin.

Command to add each user account (include all five users): sudo adduser sam, sudo adduser joe, sudo adduser amy, sudo adduser sara, sudo adduser admin
Ensure that only the admin has general sudo access.

Command to add admin to the sudo group: sudo usermod -G sudo admin & verify with groups admin.

### Step 3: Create User Group and Collaborative Folder

Add an engineers group to the system.

Command to add group: sudo addgroup engineers

Add users sam, joe, amy, and sara to the managed group.

Command to add users to engineers group (include all four users): sudo usermod -G engineers sam, sudo usermod -G engineers joe, sudo usermod -G engineers amy, sudo usermod -G engineers sara. 

Create a shared folder for this group at /home/engineers.

Command to create the shared folder: mkdir /home/engineers

Change ownership on the new engineers' shared folder to the engineers group.

Command to change ownership of engineer's shared folder to engineer group: sudo chown :engineers /home/engineers

### Step 4: Lynis Auditing

Command to install Lynis: sudo apt install lynis / sudo apt upgrade lynis (if already installed on VM and seeking upgrade to the latest version)

Command to see documentation and instructions: man lynis

Command to run an audit: sudo lynis system audit

Provide a report from the Lynis output on what can be done to harden the system.

Screenshot of report output: 

### Bonus

Command to install chkrootkit: sudo apt install chkrootkit / sudo apt upgrade chkrootkit (if already installed on VM and seeking upgrade to the latest version)

Command to see documentation and instructions: man chkrootkit

Command to run expert mode:  sudo chkrootkit -x

Provide a report from the chkrootkit output on what can be done to harden the system.

Screenshot of end of sample output: 
