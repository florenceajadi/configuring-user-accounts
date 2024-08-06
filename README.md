<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Configuring User Accounts</h1>
This tutorial outlines the implementation of configuring user accounts in Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Configure User Accounts](https://youtu.be/cG7M3Z-Cek4)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
  
<h2>Operating Systems Used </h2>

- Windows Server 2022

<h2>High-Level Deployment and Configuration Steps</h2>

- Create a new share called 'Profiles$'
- Create a new Organizational Unit called 'Domain Groups'
- Create a new group name called 'Roaming Profile Users'
- Select a member to the new group
- Link profile to user
- Confirm change has been made


<h2>Deployment and Configuration Steps</h2>

<p>
<img src="" height="80%" width="80%""/>


</p>
<p>
Diagram
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/02e4d919-30bc-4b53-913c-4c1ff708d7f8" height="80%" width="80%""/>
<img src="https://github.com/user-attachments/assets/a40581ba-a2f5-4d44-a210-c719ab0b183d" height="80%" width="80%"" />
<img src="https://github.com/user-attachments/assets/727bc58e-b667-41ce-888c-cc31d018fc2b" height="80%" width="80%"" />
<img src="https://github.com/user-attachments/assets/b3320bc2-3600-46ab-b24e-87ee4ade0365" height="80%" width="80%"" />
  <img src="https://github.com/user-attachments/assets/beac2803-6af7-49e6-9ab2-714076e50a1f" height="80%" width="80%"" />
</p>
<p>
Created a new Share folder on Server Manager called 'Profiles$' so the folder stays hiddern. Also allowing who is permitted to have access to Profiles$.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/8d535a91-9569-425b-82b2-02eaca308d4b" height="80%" width="80%"" />
  <img src="https://github.com/user-attachments/assets/66945c28-96ea-4555-b0fe-ddc7e73af8f3" height="80%" width="80%" />
  <img src="https://github.com/user-attachments/assets/9f3999f7-46e7-4356-a551-c5a124b91cfe" height="80%" width="80%" />
</p>
<p>
Created a new Organizational Unit called 'Domain Groups'. In Domain Groups, created a new group called 'Roaming Profile Users'. Added user 'Jeremy Collins' as one of the members of the group.
</p>
<p>
<img src="https://github.com/user-attachments/assets/5c689ffe-d26a-4d5f-b964-72e2bdd4891e" height="80%" width="80%"" />
  <img src="https://github.com/user-attachments/assets/678c9393-e978-4643-a436-de23d95806a0" height="80%" width="80%"" />
</p>
<p> Selecting principle: 'Roaming Profile Users'</p>
<br />

<p>
  <img src="https://github.com/user-attachments/assets/ed8d4f44-e11a-48e2-93a7-b7e18c770832" height="80%" width="80%"" />
    <img src="https://github.com/user-attachments/assets/3702a061-64dd-420c-b00e-4221bf0c8aad" height="80%" width="80%"" />
  
</p>

<p>
 Given adavanced permission to this folder only on list folder / read data AND create folder / append data. Granting Admins and Roaming Profile Users this folder.
</p>
<p>
<img src="https://github.com/user-attachments/assets/5094b565-b288-460e-831e-d9c060dd4bd0" height="80%" width="80%"" />

</p>
<p> Went back into Roaming Profile Users and clicked on user member Jeremy Collins' profile and added a profile path: \\ADG-vm\Profiles$\%username%  (which case username is jeremy.collins)</p>
<br />


<p>
<img src="https://github.com/user-attachments/assets/8ad70ca7-a8c9-4098-b59e-0637aaec59e3" height="80%" width="80%"" />

</p>

  
<p>
Logged back into Jeremy Collins account and was able to locate the path and see the account is a Roaming profile. </p>
