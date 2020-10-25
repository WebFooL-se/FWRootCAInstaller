# FWRootCAInstaller
Simple IExplorer.exe example of a Installer for a Root CA  
This installer uses Powershell to install the Root CA to Cert:\LocalMachine\Root (Trusted root CA) It will need to be run as Admin.  
```
PowerShell.exe -noprofile -windowstyle hidden -Sta -executionpolicy bypass -Command "Import-Certificate -FilePath cert.cer -CertStoreLocation Cert:\LocalMachine\Root"
```
## Installation

Windows:
```
git clone https://github.com/WebFooL-se/FWRootCAInstaller.git 
```

Download Root CA from your Untangle device:
```
http://untangleip/cert
```

Place cert.cer in the same folder as FWRootCAInstaller.SED.

Start a cmd/Powershell or your commandline of choice. 
go to the folder with FWRootCAInstaller.SED and cert.cer.

Run:
```
iexpress.exe /n FWRootCAInstaller.SED
```

You should now have a FWRootCAInstaller.EXE file in that folder.  

If you want a MSI/MSIX file you can use https://docs.microsoft.com/en-us/windows/msix/overview  
