<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Setup and Configuration</h1>
This lab outlines the prerequisites for Installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- Database(MySQL)

<h2>Operating Systems Used </h2>

- Windows 10 Enterprise(x64) Gen2</b> 

<h2>Installation</h2>
<h3>STEP 1.)
We need to prepare our virtual machine and add our operating system which will be Windows 10 Enterprise(x64). We will navigate to "images" and select our operating system here 
<img width="1907" height="799" alt="AzureVM" src="https://github.com/user-attachments/assets/0a2b20a9-0fc5-4847-b11a-9e78df991ad1" />


<h3>STEP 2.)
Once our virtual machine is deployed and running we will begin the next step of connecting to our virtual machine utilizing remote desktop connection(RDC). We will need our virtual machines public Ip address and login information that we created during the process of making the virtual machine in Azure. Once we login we will then open up powershell to ping the virtual machine to confirm everything is connected.
<img width="548" height="384" alt="Screenshot 2026-04-28 054218" src="https://github.com/user-attachments/assets/bfdc5c31-445b-470c-9dbe-80d38546cb50" />


<h3>STEP 3.)
Now that our virtual machine is working we are going to download the osTicket file within the virtual machine to begin extracting all of the tools needed create and run osTicket.
<img width="1125" height="572" alt="Screenshot 2026-04-28 060641" src="https://github.com/user-attachments/assets/270497c8-37e6-4da6-bbdb-2169c8c0842c" />


<h3>STEP 4.)
Next we are going to install/enable ISS in windwos with CGI(World Wide Web Services)
<img width="1036" height="586" alt="Screenshot 2026-04-28 061148" src="https://github.com/user-attachments/assets/e1f72408-d39e-4163-8c0f-edc2e42af7e5" />


<h3>STEP 5.) 
Next we are going to install the PHP manager for IIS
<img width="457" height="375" alt="Screenshot 2026-04-28 062850" src="https://github.com/user-attachments/assets/b9806faa-b74e-47a9-a969-00dd58544b73" />


<h3>STEP 6.)
Next we are going to install the rewrite module
<img width="454" height="356" alt="Screenshot 2026-04-28 063831" src="https://github.com/user-attachments/assets/57c92361-60c7-4d8f-a873-7ff59de180c7" />


<h3>STEP 7.)
Next we are going to create a directory for PHP in the C:/ drive, within the PHP directory we are going to unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) 
<img width="1123" height="635" alt="Screenshot 2026-04-28 064702" src="https://github.com/user-attachments/assets/52c2d185-7116-41a6-9f33-480add6c28fe" />


<h3>STEP 8.)
Next we are going to unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder
<img width="1089" height="634" alt="Screenshot 2026-04-28 065240" src="https://github.com/user-attachments/assets/327d130d-14b7-4036-aae8-ffc9f3414fb5" />


<h3>STEP 9.)
Next we are going to install VC_redist exe 
<img width="441" height="275" alt="Screenshot 2026-04-28 065800" src="https://github.com/user-attachments/assets/43ad6f82-2155-425d-90d2-ed159f0365a4" />


<h3>STEP 10.)
Next we are going to install MYSQL,once installed we will create our username and password for the program.
<img width="453" height="356" alt="Screenshot 2026-04-28 071353" src="https://github.com/user-attachments/assets/2aa2251b-8d24-48b3-8f23-6a3d9b1627a4" />

 <h3>STEP 11.) We are going to open IIS and run as administrator,from there we are going to register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe),afterwards we can Reload IIS and confirm we can stop and start the server.
 <img width="721" height="443" alt="Screenshot 2026-04-28 071849" src="https://github.com/user-attachments/assets/7995405d-a622-4185-922f-b288907dac69" />


 <h3>STEP 12.) 
 We will install osTicket v1.15.8. From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”. Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
<img width="726" height="582" alt="Screenshot 2026-04-28 073102" src="https://github.com/user-attachments/assets/9d6b3143-a036-4992-82f5-d9288c692225" />


 <h3>STEP 13.)
 To confirm osTicket is working we will reload IIS. Next we will go to sites and then default and then we should see an option to click osTicket. After we click osTicket,on the right we will click “Browse *:80”.
 <img width="1641" height="723" alt="Screenshot 2026-04-28 074000" src="https://github.com/user-attachments/assets/0d359846-852d-4b95-bd37-dc72a4e76c42" />



