# Standard Operating Procedure (SOP) for Setting Up a Windows Server
## _Integrated IT Services Limited_
## 340 John Angus drive Winnipeg 
+1 204-230-6515

Version 1.0
Written by: Francis Uluocha
Approved by: Mike Bamiloye
Date: 11/20/2024
  
# Objective
This SOP provides a step-by-step guide to set up a Windows Server, ensuring a reliable and secure installation and configuration for production or development environments.

# Application
This procedure applies to IT administrators responsible for deploying a Windows Server as a file server, domain controller, application host, or other roles within an organization.

Prerequisites
Before starting, ensure the following:
Hardware Requirements: Confirm server hardware meets Windows Server version requirements. Example: 
    CPU: 1.4 GHz (64-bit processor)
    RAM: 2 GB (minimum)
    Disk Space: 32 GB (minimum)
Installation Media: Bootable USB/DVD with the appropriate Windows Server ISO.
Network Configuration: Static IP details, domain information (if applicable).
Administrator Credentials: Access to create or manage an admin account.

Procedure steps

Step 1: Install Windows Server
Insert Installation Media: Boot the server using the USB/DVD.
Boot to Installation Media: 
Restart the server and access the BIOS/UEFI by pressing the designated key (e.g., F2, F12, or Delete).
Set the boot priority to the USB/DVD and save changes.
Start Installation: Follow the on-screen instructions: 
Select language, time, and keyboard input.
Click Install Now.
Enter Product Key: Provide the license key or choose "I don't have a product key" to activate later.
Choose Installation Type: 
Server with Desktop Experience: Includes GUI.
Server Core: Command-line only (for advanced users).
Partition the Disk: 
Select the drive and format or create new partitions as necessary.
Click Next to begin installation.
Complete Installation: The server will restart several times. Once finished, create an administrator account and set a strong password.

Step 2: Configure Initial Server Settings
Log In: Use the administrator credentials created during setup.
Run Server Manager: This launches automatically after login.
Configure Network Settings: 
Open Control Panel > Network and Sharing Center > Change Adapter Settings.
Right-click the active network adapter, select Properties, and configure: 
Static IP
Subnet mask
Default gateway
Preferred DNS server
Rename Server: 
Go to Server Manager > Local Server > Computer Name.
Click Change, provide a meaningful name, and restart.
Install Updates: 
Open Settings > Windows Update > Check for updates and install all pending updates.

Step 3: Configure Roles and Features
Launch Add Roles and Features Wizard: 
In Server Manager, click Manage > Add Roles and Features.
Follow the Wizard: 
Choose Role-based or feature-based installation.
Select the server from the server pool.
Add required roles: 
Example: Active Directory Domain Services for a domain controller, or File and Storage Services for a file server.
Install Selected Roles: Review and confirm the selection to start the installation. Restart if prompted.

Step 4: Secure the Server
Enable Windows Firewall: 
Open Control Panel > Windows Defender Firewall > Turn Windows Defender Firewall On or Off.
Configure Anti-Virus/Anti-Malware: Install a security solution as per organizational policy.
Set User Account Control (UAC): 
Adjust UAC settings to prevent unauthorized changes to the system.
Create Backups: 
Set up regular backups using Windows Server Backup or third-party tools.

Step 5: Final Testing
Verify Network Connectivity: Test the server’s connection to the network and other resources.
Check Installed Roles: Ensure roles (e.g., AD DS, File Services) are functioning as expected.
Document Configurations: Record all configuration settings, including IP, hostname, and installed roles.

Resources
[Include any resources that can help the reader execute the procedure safely and effectively.]
