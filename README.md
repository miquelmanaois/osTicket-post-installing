<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket -  Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Microsoft Azure
- Virtual Machine
- osTicket 
- Item 4
- Item 5

<h2>Good Things to Know</h2>

 - Click on specific positions for a better understanding!
 	- [Roles]
	- [Departments]
	- [Teams] 
	- [Agents]
	- [Users]
	- [SLA]
	
   

<h2>Installation Steps</h2>

<h3>Step 1: Open osTicket and use credentials from installation tutorial </h3>

- If you need help installing osTicket, please see my tutorial [here]

<h3>Step 2: Configure Roles </h3>

- Make sure you are in admin panel (check top right to see which panel you are in)
- Select the Agents tab -> Roles -> Add New Role
	- Name : Supreme Admin
	- Select Permissions tab and check every box under the "Tickets" and "Tasks" section
- Select Add Role
	
<p align="center">
<img src="https://i.imgur.com/Cxy8NM7.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/f1eRIx4.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>


<h3>Step 3: Configure Departments</h3>

- Make sure you are in admin panel (check top right to see which panel you are in)
- Select the Agents tab -> Departments -> Add New Department 
	- Name: System Administrators
- Select Create Dept. 


<p align="center">
<img src="https://i.imgur.com/Cxy8NM7.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/f1eRIx4.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>


<h3>Step 4:  Configure Teams
</h3>

- Make sure you are in admin panel (check top right to see which panel you are in)
- Select the Agents tab -> Teams -> Add New Team
	- Name: Level II Support 
- Go to members tab and select yourself in "Select Agent" dropdown menu
- Select create team. 
	
<p align="center">
<img src="https://i.imgur.com/Ed9wc2j.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/7ryNBQg.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>

<h3>Step 5: Allow anyone to create tickets</h3>

 Make sure you are in admin panel (check top right to see which panel you are in)
- Select the Settings -> User Settings
	- Check box next to: 
		- Registration Required: Require registration and login to create tickets 


<h3>Step 6: Configure Agents</h3>

-  Make sure you are in admin panel (check top right to see which panel you are in)
- Select the Agents tab -> Add New Agents
	- Name: Jane Doe
	- Email : jane.doe@osticket.com
	- Username: jane.doe
	- Click set password and uncheck box that says "send the agent a password reset email
		- Set your password to anything you like
		- uncheck box that says "require password change at next login
		- Select set
- Select Access tab 
	- Under Primary Department 
		- Select department dropdown menu -> System Administrators
		- Select Role dropdown menu -> Supreme Admin
- Select Teams tab
	- Select team dropdown menu -> Level II Support
	- Select Add
- Select Create	
- Create another agent and replace Jane with John.
	- Follow same steps as above except make some changes to Primary Department
		- Select department dropdown menu -> Support
		- Select Role dropdown menu -> View only
	- Extended Accesss 
		- Select Department -> Support
		
<p align="center">
<img src="https://i.imgur.com/QhE5p74.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/I5yvFc4.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>
 
     

<h3>Step 7: Configure Users
</h3>

- Search for Internet Information Services (IIS) and select open
- On the left, select Sites -> Default Website -> osTicket
- On the right, click “Browse *:80”
- Before continuing, head back to and open IIS.


<p align="center">
<img src="https://i.imgur.com/nOv1FP1.png" height="80%" width="80%" alt="Azure Free Account"/>

<h3>Step 8:  Configure SLA
</h3>

- Go back to IIS, Sites -> Default Web Site -> osTicket
- Double-click PHP Manager
- Click “Enable or disable an extension” at the bottom under “PHP Extensions”
- Right click and enable the following
    - php_imap.dll
    - php_intl.dll
    - Php_opcache.dll

 
     
 <p align="center">
<img src="https://i.imgur.com/14pPOdv.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/okabWbT.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>

<h3>Step 9:   Configure Help Topics
</h3>

- Intl Extension should now have a green check mark next to it


<p align="center">
<img src="https://i.imgur.com/okabWbT.png" height="60%" width="60%" alt="Azure Free Account"/>




