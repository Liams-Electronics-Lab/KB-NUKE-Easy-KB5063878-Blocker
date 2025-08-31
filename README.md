<img width="1268" height="978" alt="Screenshot 2025-08-31 184312" src="https://github.com/user-attachments/assets/3ca18458-839f-4f20-bfbc-d1f74ace3769" />


# KB NUKE - Windows Update Blocker

A PowerShell tool to block the problematic Windows update KB5063878, which causes issues with certain SSDs.
This is an easy to use reversable multi-stage blocker tool for this specific update, no other Windows updates are blocked. 


## Features

- **Scheduled Task Method** - Creates an automated script that uses PSWindows Update to check on startup if the specific update is queued and hides it if found.
- **Group Policy Method** - Uses Microsoft's Known Issue Rollback mechanism, this creates and activates a group policy that blocks the specific update. 
- **NUKE Mode** - Applies both methods for maximum protection  
- **Auto-removal** - Scheduled task automatically removes itself after a specified date, default is set to 2026/01/01.  
- **Group Policy Editor installer** - Enables gpedit.msc on Windows Home editions  

## Requirements

- Windows 10/11  
- Administrator privileges  
- PowerShell execution policy allowing scripts  

## Usage

1. Download `PowerShell-GUI-Script.ps1`  
2. Right-click and "Run with PowerShell" or run from an elevated PowerShell prompt  
3. Choose your preferred blocking method:  
   - **I** - Install scheduled task blocker  
   - **G** - Apply Group Policy block  
   - **N** - NUKE (both methods)  
   - **U** - Uninstall all blocking  

## Uninstall

Use option **U** to completely remove all blocking components including:

- Scheduled tasks  
- Script files  
- Registry entries  
- ADMX template files  

## Notes

- The tool requires administrator privileges to function  
- Scheduled task method requires PSWindowsUpdate module (auto-installed)  
- Group Policy method should work on all Windows editions  
- Safe to run multiple times  

## Disclaimer

This tool modifies Windows update behavior. Use at your own discretion. Always maintain system backups.
