# Check Probe Config - SQL Server on Azure VM
Check the Probe Port configuration for Always On Listener when working with Azure Load Balancer on Azure VM

Run the below script from one of the node elevated PowerShell 

#-- Validation of Probe Port configuration written by Ghufran Khan: \
################################################# \
Clear-Host \
Get-ClusterResource \` \
| Where-Object {$_.ResourceType.Name -like "IP Address"} \` \
| Get-ClusterParameter \` \
| Where-Object {($_.Name -like "Network") -or ($_.Name -like "Address") -or ($_.Name -like "ProbePort") -or ($_.Name -like "SubnetMask")}

More Scripts by Me: https://github.com/ghkhan89?tab=repositories

Find me on Facebook: https://www.facebook.com/GhufranKhan89 
