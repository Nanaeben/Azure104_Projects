Create a virtual network and an Azure Bastion host

Follow these steps:
1. Logon to portal.azure.com
2. Enter credentials for your subscription
3. Search for Resource Group and create a resource group by giving a preferred name
4. After Resource Group creation, In the portal, search for and select Virtual networks.
5. On the Virtual networks page, select + Create.
6. On the Basics tab of Create virtual network, enter network name and other information
7. Select Next to proceed to the Security tab.
8. In the Azure Bastion section, select Enable Azure Bastion.
9. n Azure Bastion, enter the hostname and create a public IP
10. Select Next to proceed to the IP Addresses tab.
11. In the address space box in Subnets, select the default subnet.
12. In Edit subnet, change the default name to subnet-1
13. Select Save and proceed to next tab
14. Select Review + create at the bottom of the window. When validation passes, select Create.

Create virtual machines

1. In the portal, search for and select Virtual machines.
2. In Virtual machines, select + Create, and then select Azure virtual machine.
3. On the Basics tab of Create a virtual machine, enter name vm-1, select RG, enter username and password, select none for Public inbound rule and proceed to the next tab.
4. Select the Networking tab and select vnet-1 as network with its subnet, select none for Public IP, and advance for NSG and select nsg-1
5. Leave the rest of the settings at the defaults and select Review + create.
6. Afterwards, select create and repeat the same process to create another VM

Connect to a virtual machine

1. In the portal, search for and select Virtual machines.
2. On the Virtual machines page, select vm-1.
3. In the Overview information for vm-1, select Connect.
4. On the Connect to virtual machine page, select the Bastion tab.
5. Select Use Bastion.
6. Enter the username and password that you created when you created the VM, and then select Connect.
7. At the bash prompt for vm-1, enter ping -c 4 vm-2
8. Repeat step 7 on VM 2 , enter ping -c 4 vm-1