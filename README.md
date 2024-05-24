# osticket-prereqs

---

<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Setup Guide: Requirements and Installation</h1>
This guide provides detailed instructions for setting up osTicket, the open-source help desk ticketing system, covering prerequisites and the installation process.<br />

<h2>Environments and Technologies Utilized</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating System Utilized</h2>

- Windows 10 (21H2)

<h2>Prerequisites</h2>

- Microsoft Azure (Virtual Machine)
- HeidiSQL
- osTicket Installation Files (Download Link Provided)

<h2> Tutorial Instructions </h2>
<h3> Step 1: Enabling IIS in Windows </h3> Begin by accessing the "Control Panel", then "Programs", and "Programs and Features". From there, select "Turn Windows features on or off", and check the box for "Internet Information Services".
</p>
<br />
<img src="https://i.imgur.com/hDMysuo.png" height="80%" width="80%" alt="Enable IIS"/>

</p>
<p>
<h3> Step 2: Installing Web Platform Installer </h3> Download the Web Platform Installer from the provided link and run the installer.
</p>
<br />

<p>
<img src="https://i.imgur.com/kOh6Ezy.png" height="80%" width="80%" alt="Web Platform Installer"/>
</p>
<p>
Within the Web Platform Installer, search and install "MySQL 5.5" and all versions of "PHP" up to 7.3.25. Note that some files may fail to download, but their links are provided for manual download.
</p>
<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/RtPT3ki.png" height="80%" width="80%" alt="Download Failures"/>
</p>
<p>
<h3> Step 3: Installing osTicket v1.15.8 </h3> Download osTicket from the provided link and extract the contents. Copy the "upload" folder to "C:\inetpub\wwwroot" and rename it to "osTicket".
</p>
<br />
<img src="https://i.imgur.com/KMC03rb.png" height="80%" width="80%" alt="Extract All"/>
In the "Downloads" folder, open the osTicket folder, copy the "upload" folder, navigate to "This PC', "Windows (C:)", "inetpub", "wwwroot", and paste the "upload" folder here. Then, rename it to "osTicket".
</p>
<br />
<h3> Step 4: Reloading IIS </h3> Go back to IIS Manager, click "Restart" on the right side, then navigate to "Sites" > "Default Web Site" > "osTicket" > "Browse *:80" to open osTicket in a web browser.
</p>
<br />
<img src="https://i.imgur.com/yDjIe1l.png" height="80%" width="80%" alt="Restart IIS"/>
</p>
<p>
<h3> Step 5: Enabling Extensions in IIS </h3> In IIS Manager, navigate to "Sites" > "Default" > "osTicket", double click on "PHP Manager", and click "Enable or Disable an Extension". Enable "php_imap.dll", "php_intl.dll", and "php_opcache.dll", then refresh the osTicket site in your browser.
</p>
<br />
<img src="https://i.imgur.com/YeSYmiK.png" height="80%" width="80%" alt="enable php"/>
</p>
<p>
<h3> Step 6: Renaming ost-config.php </h3> In File Explorer, go to the osTicket folder, click on the "Include" folder, and rename "ost-sampleconfig.php" to "ost-config.php".
</p>
<br />
<img src="https://i.imgur.com/ECwKXOp.png" height="80%" width="80%" alt="rename ost-config"/>
</p>
<p>
<h3> Step 7: Assigning Permissions to ost-config.php </h3> Right-click on ost-config.php, go to "Properties", "Security", "Advanced", and "Disable Inheritance". Click "Add", type "Everyone" in the space provided, click "Check Names", then "Ok", and allow "Full Control".
</p>
<br />
<img src="https://i.imgur.com/6SmEdXP.png" height="80%" width="80%" alt="ost-config permissions 1"/>
</p>
<p>
<h3> Step 8: Continuing osTicket Setup in Browser </h3> Enter the database information in osTicket setup, and note the login and password details for later use.
</p>
<p>
<h3> Step 9: Downloading and Installing HeidiSQL </h3> Download HeidiSQL from the provided files, install it, and create a new database named "osTicket" in HeidiSQL using the MySQL username and password set up earlier.
</p>
<br />
<img src="https://i.imgur.com/xwNtYY0.png" height="80%" width="80%" alt="new database"/>
</p>
<p>
Back in the osTicket setup in the browser, enter the MySQL database information, click "Install Now", and osTicket should be successfully installed.
</P>
<br />
<img src="https://i.imgur.com/bLQ99x4.png" height="80%" width="80%" alt="Congrats"/>
