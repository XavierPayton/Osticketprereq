<p align="center">
<img src="https://i.imgur.com/9bXBwVm.png" alt="osTicket logo"/>
</p>

<h1>Group Policy - Implementation </h1>
This tutorial demonstrates the implementation of a group policy in active directory that will block mircosoft edge for users.<br />


<h2>Video Demonstration:</h2>

- ### https://vimeo.com/1081026150/3bd8014f33?ts=0&share=copy

<h2>Environments and Technologies Used:</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Domain Control Server
- Active Directory
- Group Policy Managment 
- Control Panel (Inside Windows)

<h2>Operating Systems Used:</h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Implementstion Steps:</h2>

<p>
<img src="https://i.imgur.com/4y3dS95.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We will have our virtual machines set up in Azure. One will be our domain server controller (ACTIVE). The other will be our virtual machine for our regular everyday users (CLIENT 1)
</p>
<br />

<p>
<img src="https://i.imgur.com/TXvc9Ud.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
You will log into the "Domain Control Server" using "Remote Desktop". When you're in, you will access the "Server Manager" and "Click" on "Tools" in the top right corner. Then you will click on "Group Policy Management".
</p>
<br />

<p>
<img src="https://i.imgur.com/nQ4o0YH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click on whichever "Domain Policy" that contains your "users". Then click "CREATE A GPO IN THIS DOMAIN, AND LINK IT HERE". After creating a name for the GPO right click the newly created GPO and click "EDIT"
</p>
<br />

<p>
<img src="https://i.imgur.com/sAkWy3s.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On the right side under "User Configuration" Click "Policies" > "Adminisrative Templates: Policies" > "System". Scroll all the way down in the system settings  and click "Don't Run Specified Windows Applications"
</p>
<br />

<p>
<img src="https://i.imgur.com/EvKHkji.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
When here click "Enabled". Then under "options" and "list of dissallowed applications" click "Show" and Type in "msegde.exe" Click > "OK" > "Apply" > "OK"
</p>
<br />

<p>
<img src="https://i.imgur.com/D9EhKIR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
You will need to update the GPO for the Group Policy settings to take effect immediatley, click the "Windows Icon" in the bottom left of the computer. Open up the "Control Panel". When opened type in "gpupdate /force", this will update the GPO to be enacted immediatley.
</p>
<br />

<p>
<img src="https://i.imgur.com/VFv0dsM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Log into your Virtual Machine for active directory users and log in as a user.
</p>
<br />

<p>
<img src="https://i.imgur.com/FyxigzA.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
"Microsoft Edge" has been blocked. Not accessible for users.
</p>
<br />

<h2>Deletion Steps:</h2>

<p>
<img src="https://i.imgur.com/e23Bvy3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go back into your "Domain Server Controller" virtual machine and open up the "server Manager". Go to "Tools" in the top right corner and Click on "Group policy Manager". Go to your newly created group policy under the GPU with all of your users, right click the GPO and hit delete.
</p>
<br />

<p>
<img src="https://i.imgur.com/xz8uHuo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Update the group policy in the "Control Panel" on both Virtual Machines.
</p>
<br />

<p>
<img src="https://i.imgur.com/o1lG1DL.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Users can now access Microsot Edge.
</p>
<br />
