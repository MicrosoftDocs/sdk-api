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

# SetupPromptReboot function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupPromptReboot</b> function asks the user if he wants to reboot the system, optionally dependent on whether any files in a committed file queue were in use during a file operation. If the user answers "yes" to the prompt, shutdown is initiated before this routine returns.


## -parameters




### -param FileQueue [in]

Optional pointer to a handle to the file queue upon which to base the decision about whether shutdown is necessary. If <i>FileQueue</i> is not specified, 
<b>SetupPromptReboot</b> assumes shutdown is necessary and asks the user what to do.


### -param Owner [in]

Handle for the parent window to own windows created by this function.


### -param ScanOnly [in]

Indicates whether or not to prompt the user when 
<b>SetupPromptReboot</b> is called. 




If <b>TRUE</b>, the user is never asked about rebooting, and system shutdown is not initiated. In this case, <i>FileQueue</i> must be specified. If <b>FALSE</b>, the user is asked about rebooting, as previously described.

Use <i>ScanOnly</i> to determine if shutdown is necessary separately from actually initiating a shutdown.


## -returns



The function returns a combination of the following flags or –1 if an error occurs.

To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
					




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/65ccd3d1-1846-48cb-9fe6-ab5c69845e01">SetupPromptForDisk</a>
 

 

