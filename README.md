<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="DNS Configuration Exercises"/>
</p>

<h1>File Sharing and Permission Management in Active Directory</h1>
This tutorial demonstrates the creation and management of file shares with various permissions in an Active Directory domain environment.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Active Directory Domain Services
- Windows File Sharing

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>File Sharing Exercise Objectives</h2>

- Creating file shares with distinct permissions
- Testing access permissions from a client machine

<h2>Exercise Steps and Observations</h2>

<h3>Creating Sample File Shares with Various Permissions:</h3>
<ul>
    <li>Logged into DC-1 as domain admin (mydomain.com\jane_admin).</li>
    <li>On DC-1's C:\ drive, created folders: “read-access”, “write-access”, “no-access”, “accounting”.</li>
    <li>Set specific share permissions for the “Domain Users” group on these folders.</li>
</ul>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Setting File Permissions"/>
</p>
<p>
    This step was crucial in establishing different levels of access control for various user groups.
</p>
<br />

<h3>Accessing File Shares as a Normal User:</h3>
<ul>
    <li>From Client-1, logged in as a normal user, navigated to the shared folders on \\dc-1.</li>
    <li>Tested access to each folder, noting which folders were accessible and which allowed file creation.</li>
</ul>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Testing File Share Access"/>
</p>
<p>
    This exercise helped understand how share permissions impact user access in a real-world scenario.
</p>
<br />

<h3>Setting Permissions for an 'ACCOUNTANTS' Security Group:</h3>
<ul>
    <li>Created an “ACCOUNTANTS” Security Group in Active Directory on DC-1.</li>
    <li>Assigned “Read/Write” permissions to the “ACCOUNTANTS” group on the “accounting” folder.</li>
    <li>As a normal user on Client-1, tested access to the “accounting” share before and after being added to the “ACCOUNTANTS” group.</li>
</ul>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Managing Security Group Permissions"/>
</p>
<p>
    The creation and management of a specific security group highlighted the effective control of access rights within an organizational context.
</p>
<br />

<!-- Footer or additional notes -->

