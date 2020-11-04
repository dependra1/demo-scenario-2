# demo-scenario-2
<#Macro Life, a healthcare company has recently setup the entire Network and Infrastructure on Azure. 
The infrastructure has different components such as Virtual N/W, Subnets, NIC, IPs, NSG etc.
The IT team currently has developed PowerShell scripts to deploy each component where all the properties of each resource is set using PowerShell commands.
The business has realized that the PowerShell scripts are growing over period of time and difficult to handover when new admin is on-boarded in the IT.
The IT team has now decided to move to ARM based deployment of all resources to Azure.
All the passwords are stored in an Azure Service known as key Vault. The deployments needs to be automated using Azure DevOps using IaC (Infrastructure as Code).#>

1) What are different artifacts you need to create - name of the artifacts and its purpose
A - 

2) List the tools you will to create and store the ARM templates.<br/>  
A - To create ARM templates, we can use VS code and store the templates in local repos, Azure Git repos or Github repos. For this scenario, I have used Github repos.  

3) Explain the process and steps to create automated deployment pipeline. 
A - i) sync the github repository to VS code where we will commit the changes or deploy new templates
    ii) In the build pipeline, set the deploy trigger to "Enable continuous integration"
    iii) Set the target resource group and subscription
    iv) Create appropriate stages as per the environments and setup appropriate triggers (eg: dev, uat, prod)
    v) In this way, whenever there is a code commit to master branch, pipeline will be triggered automatically

4) Create a sample ARM template you will use to deploy a Windows VM of any size
A- Added to repos.

5) Explain how will you access the password stored in Key Vault and use it as Admin Password in the VM ARM template.
A
