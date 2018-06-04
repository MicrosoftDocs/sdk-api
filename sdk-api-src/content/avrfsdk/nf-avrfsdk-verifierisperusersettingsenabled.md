---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# VerifierIsPerUserSettingsEnabled function


## -description


Determines whether Application Verifier can use per-user settings.


## -parameters






## -returns



If per-user settings are enabled, the function returns <b>TRUE</b>. Otherwise, it returns <b>FALSE</b>.




## -remarks



Application Verifier settings are stored in the following registry key <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Windows NT\CurrentVersion\Image File Execution Options</b> for native applications and <b>HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Windows NT\CurrentVersion\Image File Execution Options</b> for applications running under WOW64. Only administrators can write to these keys.

Starting with Windows Vista, Application Verifier settings can be stored in <b>HKEY_CURRENT_USER</b>. To enable the use of the per-user settings, the administrator must create a REG_DWORD value named <b>ImageExecutionOptions</b> in the <b>HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager</b> key, set the low-order bit, and reboot the computer. To disable the use of the per-user settings, the administrator must either clear the bit or delete the registry value and reboot the computer.

This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> function to load Verifier.dll and call the <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> function to get the address of this function.





