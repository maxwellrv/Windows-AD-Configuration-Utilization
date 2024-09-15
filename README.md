# Windows-AD-Configuration-Utilization
Microsoft Acitive Directory is a very powerful tool that any IT administrator can utilize, not only to leverage their responsibilities and hone new skills, but also add efficiency to the enterprise that they work for. Many may think that Microsoft AD is a thing of the past and that Azure infrastructure is the future. However, being able to navigate Active Directory efficiently can be a skill that is indespensible even to a cloud provider. Much of the cloud infrustructure raved about today has a basis that points back to the way AD was and still is utilized, simply because it is a system that just works. Therefore, I have included a project on being able to deploy and navigate Microsoft AD in a sandbox environment. So now any tech praticioner that wants to hone their skills for IT or cloud management has an idea on what it takes and where to start.

I began with finding an ISO file of Windows Server 2022 online. Once found and downloaded onto my PC, I then spun up this file in VirtualBox. As a disclaimer, anyone wanting to do this will need to input some information in order to have access to a free trial of this software. It is nothing too invasive or extensive, just things such as your name, email, and phone number.

![image](https://github.com/user-attachments/assets/f5b4e7b2-d83f-43b6-b0a7-ea9853c7b382)
![image](https://github.com/user-attachments/assets/1d2f5228-c0be-4d4b-8b23-085f5a128ca8)

I then began to configure the server to install AD, DNS, and DHCP features and capabilities. This will most likely need to be configured anytime a new windows server is spun up. I then created a new domain (forest) to my server, thus appointing it as a domain controller. 
Security Disclaimer: Having only one domain controller in a network can be considered a vulnerability. Therefore, it can be common to divide the authority and files among multiple controllers. This however is just for demonstration purposes on a basic level so I did not create and configure more than one controller for the time being.

![image](https://github.com/user-attachments/assets/f85e39a7-401f-4e66-ba9b-ba276f7fe3db)
![image](https://github.com/user-attachments/assets/7c5e49a8-d027-4755-9cab-6c4912fc839b)



I configured AD with a new organizational unit. This is a more broad categorization method for networks that users and groups can fall into. In this case, I labeled this OU as “Test Organizational Unit” and created two users - “Test User 1” and “Test User 2”.  I then created a group and placed these users with it. Groups help add easement to managing departments and groups of people within an organization. However, if need be, an administrator can go and configure user credentials, authorizations, and accessibilities individually within a group. 

![image](https://github.com/user-attachments/assets/3aa2c96d-aa61-4865-844d-5d05566451d7)

Domains and Users were officially configured. Now I was able to navigate over to a new Windows 10 VM in VirtualBox and add it to the domain in the settings. I found this setting in the advanced system settings category of the PC properties. Before this step, I made sure to configure the DNS server machine as the Windows Server by using its IP address. As a result, I was then able to restart my VM and log in with the domain credentials of User 1 that I configured on my server.

![image](https://github.com/user-attachments/assets/a165c1bb-d1b8-4770-b6aa-b60c54629269)
![image](https://github.com/user-attachments/assets/4f15523b-fb2c-4ce7-9dc5-7018f378b0b0)
![image](https://github.com/user-attachments/assets/91ca2fbc-e372-403f-bf64-9fb1320a4381)
