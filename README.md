# Steps:

1. Download the (ViveTool-vx.x.x.zip)[https://github.com/thebookisclosed/ViVe/releases] file.
2. Open terminal as admin
3. Enter `cd c:\folder\path\ViveTool-v0.x.x` (CTRL + l)
4. `.\ViVeTool /enable /id:44353396`
5. Restart PC 
6. Open File Explorer (Windows key + E).
7. Type the following path on the address bar and press Enter: `C:\Windows\system32`
8. Search `IntegratedServicesRegionPolicySet.json` and right click and open properties
9. Security tab > **Advanced** button > Change the Owner > Enter **Administrator** > Ok.
10. Click the edit **Edit** button from the **Security Tab**
11. Select the **Administrators** item from the "Group or user names" section.
12. Check the Allow option for Full control from the "Permissions for Administrators" section.
13. If **Edit** isn't working to this. Open a Command Prompt or PowerShell as an administrator.
Use the following command to take ownership:
`takeown /f "C:\Windows\System32\IntegratedServicesRegionPolicySet.json" `
Use this to grant permissions:
` icacls "C:\Windows\System32\IntegratedServicesRegionPolicySet.json" /grant YourUsername:F `
14.In the **IntegratedServicesRegionPolicySet.json** file for the “Edge is uninstallable.” setting, change the “defaultState” option from disabled to **enabled**.
15. Find out the region by running `reg query "HKEY_USERS\.DEFAULT\Control Panel\International\Geo" `
16. Open Microsoft Edge > Settings > System and Performance > Turn off the *Startup boost toggle* switch under the **System** section.

_Once you complete the steps, Microsoft Edge will be completely removed from Windows 11 or 10, depending on the operating system. If the option to remove the browser is still unavailable, restart the computer a few times to ensure the system recognizes the changes._
