Objective

The purpose of this lab is to learn how to manage identities and access in Azure using Microsoft Entra ID, Security Groups, and Role-Based Access Control (RBAC).

Resources Used
Microsoft Entra ID
Azure Resource Group
Azure Virtual Machine
Security Groups
Azure RBAC
Step 1: Create a Resource Group
Sign in to the Azure Portal.
Go to Resource Groups.
Click Create.
Enter the Resource Group name:
IAM-Lab-RG
Select a region.
Click Review + Create and then Create.
Step 2: Create a Virtual Machine
Go to Virtual Machines.
Click Create.
Enter the VM name:
TestVM
Choose the required image and size.
Configure administrator credentials.
Click Review + Create and then Create.
Step 3: Create Entra ID Users
Go to Microsoft Entra ID.
Select Users.
Click New User.
Create the following users:
AdminUser
VMOperator
ReaderUser
Save the users.
Step 4: Create Security Groups
Go to Microsoft Entra ID.
Select Groups.
Click New Group.
Create:
VM-Admins
VM-Readers
Save the groups.
Step 5: Add Users to Groups
VM-Admins Group

Add:

AdminUser
VMOperator
VM-Readers Group

Add:

ReaderUser
Step 6: Assign RBAC Roles
Open TestVM.
Select Access Control (IAM).
Click Add Role Assignment.
Assign VM Contributor Role
Role: Virtual Machine Contributor
Member: VM-Admins
Assign Reader Role
Role: Reader
Member: VM-Readers
Step 7: Verify Access
Members of VM-Admins can manage the virtual machine.
Members of VM-Readers can view resources but cannot make changes.
Lab Outcome

Successfully implemented Azure Identity and Access Management by:

Creating Entra ID users
Creating security groups
Managing group memberships
Assigning RBAC roles
Applying the principle of least privilege
