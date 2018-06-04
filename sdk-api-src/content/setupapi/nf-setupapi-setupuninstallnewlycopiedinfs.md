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

# SetupUninstallNewlyCopiedInfs function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupUninstallNewlyCopiedInfs</b> function uninstalls INF files (.inf), precompiled INF files (.pnf), and catalog files (.cat) that are previously installed during the committal of the specified file queue.

A caller of this function must have administrative privileges; otherwise, the function fails.


## -parameters




### -param FileQueue

TBD


### -param Flags [in]

Flags to use with 
<b>SetupUninstallNewlyCopiedInfs</b>. No flags are defined currently. This parameter must be 0 (zero).


### -param Reserved [in]

Reserved. This parameter must be <b>NULL</b>.


#### - QueueHandle [in]

Handle to an open and committed file queue. This queue contains the newly installed INF, PNF, or CAT files that 
<b>SetupUninstallNewlyCopiedInfs</b> uninstalls.


## -returns



If the parameters passed in are valid, the return value is <b>TRUE</b> (nonzero), which does not necessarily mean that any INFs are uninstalled.

If some of the parameters passed in are invalid, the return value is <b>FALSE</b> (zero). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/c532f435-7393-49f0-975c-4c0ecca64407">SetupCommitFileQueue</a>



<a href="https://msdn.microsoft.com/70cec8c7-7954-44d7-93f5-711368f72bf7">SetupUninstallOEMInf</a>
 

 

