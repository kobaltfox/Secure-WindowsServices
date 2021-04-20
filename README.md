# Secure-WindowsServices
Our PowerShell script for securing vulnerable Windows services' insecure permissions.

$ACL = Get-ACL $Path; returns an error. Change to:
$ACL = (Get-Item $Path).GetAccessControl('Access') ;
