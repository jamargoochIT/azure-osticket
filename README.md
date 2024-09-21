<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>Creating & Configuring an Azure Virtual Machine for osTicket</h1>
This tutorial goes over the process for setting up a virtual machine in Azure with the intent of installing osTicket.<br /><br><br><br><br>



Up first, we’ll need to create a resource group.

![image](https://github.com/user-attachments/assets/e08f0463-c49e-4484-a743-a41e81af5bc4)<br><br><br><br>



 

We’ll set up a resource group by filling out the necessary fields:<br>
- The resource group name – can be whatever you want.
- Region – I chose US East 2<br>
![image](https://github.com/user-attachments/assets/97a7d47d-8206-4d49-bf21-159587406f4a)
- Click Review and Create at the bottom of the page to continue to validation.
- After the resource group has been validated, we’ll click create at the bottom of the screen.<br><br><br><br>


After the resource group has been created, next we’ll need to create a virtual machine.
Type virtual machine into the Azure search bar and then click create, then select the first option, Azure Virtual Machine.
 
![image](https://github.com/user-attachments/assets/f29ea864-1ba4-4d17-a7a3-edad07fc6897)
![image](https://github.com/user-attachments/assets/12012a5d-3154-4715-b606-ca51ce592949)<br><br><br><br>



 

 
Here, we’re going to setup the virtual machine for osTicket. Here are the necessary fields we need to fill out:
- Resource Group – make sure this is the same resource group we created.
- Virtual Machine Name – You can name it whatever you want, but I’ll use vmosticket-1.
- Region – Make sure it’s the same as what we selected for our resource group.
- Image – We’ll want to select Windows 10 Pro, version 22H2 – x64 Gen2<br><br>
![image](https://github.com/user-attachments/assets/7958cb30-443a-45f9-84e9-b6a28897c768)

Now we’ll scroll down to the next section to the remaining fields we need to fill out:
- Size – Here, we’ll choose Standard_E2s_v3 – 2 vcpus, 16GiB memory. This is basically going to affect the speed of the virtual machine, having 2 virtual CPUs with 16 Gigabytes of memory will be fine for what we’re going to need it for.
- Username – You can type what you want here and for the passwords. 
- Password
- Confirm Password
![image](https://github.com/user-attachments/assets/ce91c1a6-18ef-423e-9652-b7465d43cd2b)<br><br><br><br>




Then, at the bottom of the screen, we need to click the box that says:
![image](https://github.com/user-attachments/assets/28555a54-f554-408e-ba4f-a2feb4d70743)
After we’ve done that, click Review + Create.<br><br><br><br>

If you get this error message during validation:
![image](https://github.com/user-attachments/assets/8d543317-061e-4819-9e14-c2df8cd891bb)<br><br>

We’ll need to go back to the basics tab (we can click on the basics tab that’s highlighted in the image above) and click the box that says:
![image](https://github.com/user-attachments/assets/d1f9b8e7-56f9-4b30-bc37-aaa7d7e9fd1d)


If it’s already checked, uncheck it and check it again.
Once we’ve done that, we can simply press review + create.<br><br><br><br>


After the validation completes, click create.
![image](https://github.com/user-attachments/assets/c8edf459-ac28-4c9f-aac7-648c8aa43137)
After the VM has been created, click on Go to resources.<br><br><br><br>

 

We’ll need to take note of the Public IP address so we can use it to remote into the VM.
![image](https://github.com/user-attachments/assets/07181fb8-8305-404b-89a7-c97d8857baac)<br><br><br><br>

In the Windows search bar,<br>
![image](https://github.com/user-attachments/assets/d450847a-6d72-4ef6-aee1-bb4a3e535615)


Type in Remote Desktop and open the app. In the computer field, type in the public IP address for the VM we just created. 
![image](https://github.com/user-attachments/assets/370a1d52-c5ff-4e0c-9e86-7e9ef5efc6a9)
![image](https://github.com/user-attachments/assets/a0a329cd-d4e2-40cc-9913-ed134783013c)<br><br><br><br>
 


 

To log in, we’ll need to use the credentials we created here:
![image](https://github.com/user-attachments/assets/2d923395-9209-4e99-aa84-9600ed4cedfc)<br><br><br><br>
 


After our credentials have been accepted, we’ll get the following message:
![image](https://github.com/user-attachments/assets/30fb44e6-ea73-4488-9080-fcabe46f5814)<br><br><br><br>
 

As it says at the top, it’s telling us the connection to the computer may be unsafe, but it’s not since we created, the VM we’re about to connect to.
We can check the box at the bottom to not be asked this again. Then we can click Yes.<br><br>

And that's it; we should be logged into the virtual machine and ready to install osTicket.<br><br><br><br>

If we ever forget our username or password, go to the main page where it lists all of the virtual machines we’ve created and click on the name of the virtual machine you’ve forgotten the password or username to. After that, click Help->Reset Password, and on the right, it will display our username for the VM and we can reset our password.
![image](https://github.com/user-attachments/assets/352a4ff3-39c3-4f90-bc3a-eea5d08e8291)<br><br>

And that's it for now. See you in the next one!

 
