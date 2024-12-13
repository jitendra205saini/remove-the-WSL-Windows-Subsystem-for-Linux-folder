# remove-the-WSL-Windows-Subsystem-for-Linux-folder

To remove the WSL (Windows Subsystem for Linux) folder from File Explorer in Windows 11, you can follow these steps:

## Method 1: Using the Registry Editor
   ### 1. Open the Registry Editor: 
  - Press Win + R to open the Run dialog.
  - Type regedit and press Enter.
  ### 2.Navigate to the following path:

```
HKEY_CURRENT_USER\Software\Classes\CLSID\{B2B4A4D1-2754-4140-A2EB-9A76D9D7CDC6}


```
### 3.Delete the entry:
- Right-click on the ``` {B2B4A4D1-2754-4140-A2EB-9A76D9D7CDC6}  ``` folder.

- Select ``` Delete ```.

### 4. Restart your computer to apply the changes.

## Method 2: Using a Registry File
### 1.Open Notepad:

- Press``` Win + R``` to open the Run dialog.

- Type ```notepad ```and press Enter.

### 2.Copy and paste the following code into Notepad:
```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Classes\CLSID\{B2B4A4D1-2754-4140-A2EB-9A76D9D7CDC6}]
@=""
"System.IsPinnedToNameSpaceTree"=dword:00000000
```
### 3.Save the file:

- Click on File > Save As.

- Choose a location (e.g., Desktop) and name the file ```Remove-WSL.reg```.

- Ensure the ```Save as type``` is set to ```All Files```.

### 4.Double-click the saved .reg file to merge it:

- When prompted, click ```Run ```> ```Yes ```(UAC) > ```Yes``` >``` OK```.

### 5.Restart your computer to apply the changes.

## Method 3: Uninstalling WSL (Optional)
If you no longer need WSL, you can uninstall it:

### 1.Open PowerShell as Administrator:

- Press Win + X and select Windows PowerShell (Admin).

### 2.Run the following command to list installed WSL distributions:

- powershell
```
wsl --list --verbose
```
### 3.Unregister the distribution you want to remove:

- powershell
```
wsl --unregister <distribution_name>
```
### 4.Restart your computer to apply the changes.

These methods should help you remove the WSL folder from File Explorer. If you encounter any issues or need further assistance, feel free to ask!

