# NOTE:
**This guide is mainly focused on PowerShell commands that could be used for enumeration purposes, yet you can find some commands that are used for other purposes than enumeration. 

# **Enumeration**
PowerShell is a windows built-in comman-line interface (CLI)
`ipconfig` - Information about IP configuration (including your own IP address)
`hostname` - Displays the hostname of a current machine
`systeminfo` - Display information about the current system
`Get-ExecutionPolicy -List` - Display the PowerShell execution policy
`[Environment]::Is64BitProcess` - Check whether the current machine is 64 bits *(Returns true if the current system is 64 bits)*
`Get-Command` - lists Commandlets (cmdlet), functions, aliases, workflows, filters, scripts, and apps that are available to use in PS
`Get-Command *process*` (e.g `Get-Command *firewall*`) - commands containing the specified process 
`Get-Process -Name "process-name"` (e.g `Get-Process -Name "powershell"`) - Get information on particular process | NOTE: The process must be running
`whoami` - show the current user
`whoami /priv` - display current user's privileges
`net localgroup` - lists all groups
`net localgroup groupname` (e.g `net localgroup guests`) - info on particular groups
`arp -a` - ARP table
`netstat -ano` - dispays network connections 
`tasklist` - displays a list of currently running processes
`tasklist /m` - shows DLL processes loaded by processes
`route print` - display the local machine's IP routing table 

# **Other Useful Commands**
`nslookup example.com` - Get the IP address of a domain
`ipconfig /flushdns` - Flush the DNS Resolver Cache
`Get-Process -Name "process-name" | Kill` (e.g `Get-Process -Name "powershell | Kill` - this command should close the running powershell app, stopping the powershell) - Stop a running process, close an app