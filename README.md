# windows-lite-2004
 AME scripts

## Updates
Do SSU (Service Stack) Update first and reboot
https://www.catalog.update.microsoft.com/Search.aspx?q=Servicing%20Stack%20Update%20Windows%2010

Then do comulative update last and reboot
https://www.catalog.update.microsoft.com/Search.aspx?q=Cumulative%20Update%20Windows%2010

Make sure you download the Same MONTH and Architecture (x64)

Steps to Extract and Install
```
C:\> expand -F:* <.msu file> <dest>
dism /online /add-package /packagepath=C:\Windows10.0-EXTRACTED-x64.cab
```

Reboot between each one then run
```
dism /online /Cleanup-Image /StartComponentCleanup
```
