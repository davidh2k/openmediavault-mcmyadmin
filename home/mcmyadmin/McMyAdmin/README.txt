McMyAdmin Readme

1) Installation
2) Configuration
3) Execution
4) Notes

http://mcmyadmin.com/

1) Installation
 I) Prerequisites
  a) Windows:
    - Microsoft .NET Framework version 3.5
	  http://www.microsoft.com/downloads/en/details.aspx?FamilyID=333325fd-ae52-4e35-b531-508d977d32a6

	- Optional: IKVM runtime
	  http://www.ikvm.net/
	  
  b) GNU/Linux and similar:
    - 64-bit systems, GNU Lib C 2.5 or Newer
    - 32-bit systems, Mono 2.10.3 or Newer

  c) Mac OS
    - Mono Runtime for Mac OS
	  http://www.mono-project.com/

  c) All Platforms:

	- Java Runtime
	  http://www.java.com/en/download/
	  
 II) Instructions
	Windows) Unpack MCMA2-Latest.zip into an empty directory, or 
	into the same location as an existing McMyAdmin installation.
	
	Linux) Unpack MCMA2_glibc25.zip into an empty directory, or
	into the same location as an existing McMyAdmin installation.

	Mac OS) Unpack MCMA2-Latest.zip into an empty directory, or 
	into the same location as an existing McMyAdmin installation.

2) Configuration
 The main configuration file is McMyAdmin.conf. This file is not included
 in the main archive. If no McMyAdmin.conf is present, then the contents of
 McMyAdmin.conf.default will be copied into a new McMyAdmin.conf.
 
 If you are installing McMyAdmin on a remote system, you will need to change
 your default login before you can access it remotely.

 You can do this by invoking McMyAdmin with the --setpass argument:
 McMyAdmin.exe/MCMA2_glibc25 --setpass NEWPASSWORD
 
3) Execution
 I) Windows
	Run McMyAdmin.exe directly.
	
 II) GNU/Linux and similar
	64-bit systems, Execute MCMA2_Linux_x86_64
	32-bit systems, run mono McMyAdmin.exe

 III) Mac OS
    Run mono McMyAdmin.exe from the command line
 
 Assuming that you are using the default port and hostname settings, You can 
 then browse locally by navigating to:
    http://localhost:8080/
 
 The text console left by the McMyAdmin process can be used in the same way
 as the normal Minecraft server console. You can enter commands as normal.
 To use McMyAdmin specific commands, prepend them with a forward slash. E.g.
 /restart to restart the server from the console.
 
 4) Notes 
  I) Security
   While every effort is made to make sure that McMyAdmin is secure, there 
   are of course no guarentees that it is. It is a web server and should be
   treated as one.
   
   Therefore it should not be run as a root or administrative user and should
   be run as a seperate user that only has permission to access the
   installation directory and the files it contans. Any files within the
   nested McMyAdmin folder (containing McMyAdmin.html) can be accessed via the
   web interface (so long as the user is logged in).
   
   If you are using the default password to log in, you will not be able to
   access the control panel via a remote IP address. Only local IPs (127.0.0.1)
   will be accepted.
   
   McMyAdmin collects the following information about your server and sends it
   to a PhonicUK controlled server:
   
   * The name of the server
   * Its IP address/port
   * Current status (running, stopped)
   * Number of active players
   * Maximum number of players
   * McMyAdmin version
   * Minecraft server version
   * Whether or not to appear in public lists (configurable via web UI)
   * The servers uptime
   * The name of any detected virtualized environments (VMWare, Xen, OpenVZ, etc)
   * Information about your McMyAdmin Licence

   This information is used for licence management and quality control. No
   information is sent other than items explicitly mentioned in the list above.
   
  II) Created files.
   McMyAdmin will create the following files in its directory:
   - McMyAdmin.conf (Main configuration file if it doesn't exist)
   - userhistory.json (Lifetime stats for any users that visit the server)
   - groupinfo.json (Information about groups and user permissions)
   - schedule.json (The server schedule)
   - UserInfo.txt (Data for MCMA Users)