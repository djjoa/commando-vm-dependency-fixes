# commando-vm-dependency-fixes
Simple repo to fix the current depencendy issues with `wingdb.flare v10.0.10586.22`. 

# Issue
Returning a 404 because the link  https://codemachine.com/downloads/win10rs1/X86%20Debuggers%20And%20Tools-x86_en-us.msi is invalid. 

## Example error output 
```
PS C:\Users\commando\Downloads\commando-vm-master\commando-vm-master> cinst.exe -y windbg.flare --ignore-checksums
Chocolatey v0.10.15
Installing the following packages:
windbg.flare
By installing you accept licenses for the packages.
Progress: Downloading windbg.flare 10.0.10586.22... 100%

windbg.flare v10.0.10586.22
windbg.flare package files install completed. Performing other installation steps.
Attempt to get headers for https://codemachine.com/downloads/win10rs1/X86%20Debuggers%20And%20Tools-x86_en-us.msi failed.
  The remote file either doesn't exist, is unauthorized, or is forbidden for url 'https://codemachine.com/downloads/win10rs1/X86%20Debuggers%20And%20Tools-x86_en-us.msi'. Exception calling "GetResponse" with "0" argument(s): "The remote server returned an error: (404) Not Found."
Downloading windbg.flare
  from 'https://codemachine.com/downloads/win10rs1/X86%20Debuggers%20And%20Tools-x86_en-us.msi'
ERROR: The remote file either doesn't exist, is unauthorized, or is forbidden for url 'https://codemachine.com/downloads/win10rs1/X86%20Debuggers%20And%20Tools-x86_en-us.msi'. Exception calling "GetResponse" with "0" argument(s): "The remote server returned an error: (404) Not Found."
The install of windbg.flare was NOT successful.
Error while running 'C:\ProgramData\chocolatey\lib\windbg.flare\tools\chocolateyInstall.ps1'.
 See log for details.

Chocolatey installed 0/1 packages. 1 packages failed.
 See the log for details (C:\ProgramData\chocolatey\logs\chocolatey.log).

Failures
 - windbg.flare (exited 404) - Error while running 'C:\ProgramData\chocolatey\lib\windbg.flare\tools\chocolateyInstall.ps1'.
 See log for details.
 ```
# Solution
Either download the missing packages using https://web.archive.org and set up your own reference for the chocolatey install for windb.flare or reference the files from within this repo.


