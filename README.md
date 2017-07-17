# ARM Template of SQL Server 2016 SP1 Enterprise on windows server 2016

# Steps To Deploy using powershell

1. Login-AzureRMAccount
2. New-AzureRmResourceGroup -Name sql-16 -Location "West US"
3. Update adminPassword and validation_key in Template.
4. Change chef_server_url and validation_client_name in Template.
5. New-AzureRmResourceGroupDeployment -Name sql-16 -ResourceGroupName sql-16 -TemplateFile
 C:\chef-repo\azure-templates\sql2016-win2016-Enterprise\deploy.json -TemplateParameterFile C:\chef-repo\azure-templates
\sql2016-win2016-Enterprise\params.json