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

# SetupLogErrorW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupLogError</b> function writes an error message to a log file. It is meant to be used during the installation of Windows, but it is always available. It is not intended to be used after the operating system is installed — the event log should be used instead.


## -parameters




### -param MessageString [in]

Pointer to the string that should be saved to Setup's log. The message must end with a return-linefeed combination (\r\n). You should use a null-terminated string. The null-terminated string should not exceed the size of the destination buffer. The message is always saved to the action log, setupact.log. If <i>Severity</i> is <b>LogSevWarning</b>, <b>LogSevError</b>, or <b>LogSevFatalError</b>, Setup also saves the message to the error log, setuperr.log. Both logs are stored in the Windows directory.


### -param Severity [in]

Severity of the message, one of the following: <b>LogSevInformation</b>, <b>LogSevWarning</b>, <b>LogSevError</b>, or <b>LogSevFatalError</b>.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<ul>
<li>The action log is intended for recording all modifications made to the system during installation of Windows.</li>
<li>The error log is intended for errors during installation of Windows only.</li>
<li>The <i>MessageString</i> parameter may be formatted further by Setup (though it does no additional processing now).</li>
<li>The error log will be presented to the user at the end of system  setup.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>
 

 

