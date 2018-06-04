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

# SetupIterateCabinetW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupIterateCabinet</b> function iterates through all the files in a cabinet and sends a notification to a callback function for each file found.


## -parameters




### -param CabinetFile [in]

Cabinet (.CAB) file to iterate through.


### -param Reserved [in]

Not currently used.


### -param MsgHandler [in]

Pointer to a <a href="https://msdn.microsoft.com/41eaa57a-e116-443c-93ee-397456a5c466">FileCallback</a> routine that will process the notifications 
<b>SetupIterateCabinet</b> returns as it iterates through the files in the cabinet file. The callback routine may then return a value specifying whether to decompress, copy, or skip the file.


### -param Context [in]

Context value that is passed into the routine specified in <i>MsgHandler</i>. This enables the callback routine to track values between notifications, without having to use global variables.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>
 

 

