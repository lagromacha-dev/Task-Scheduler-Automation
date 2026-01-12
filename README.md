Automating Task Scheduler Setup with PowerShell
Overview

This guide explains how to use the provided PowerShell script to create a scheduled task that runs a Python script every 5 minutes. This method is dynamic and avoids manual XML editing.

Prerequisites

Windows OS with Task Scheduler available.
PowerShell (installed by default on Windows).
Python installed on your machine.
Your Python script saved in a known directory.


Steps to Use the Script
1. Download the PowerShell Script
Save the script file as CreateScheduledTask.ps1 in any folder (e.g., C:\Automation).

2. Edit the Script
Open the script in a text editor and update these variables:
PowerShell$PythonPath = "C:\Path\To\Python\pythonw.exe"       # Path to your Python executable$ScriptPath = "YourScript.py"                       # Name of your Python script$WorkingDir = "C:\Path\To\Your\Script\Directory"    # Folder where your script is located$TaskName = "AutomationTask"                        # Name for the scheduled taskShow more lines

3. Run the Script

Open PowerShell as Administrator.
Navigate to the folder where you saved the script:
PowerShellcd C:\AutomationShow more lines

Execute the script:
PowerShell.\CreateScheduledTask.ps1``Show more lines



4. Verify the Task

Open Task Scheduler → Look for the task named AutomationTask.
Confirm the trigger is set to run every 5 minutes.
Confirm the action points to your Python script.


