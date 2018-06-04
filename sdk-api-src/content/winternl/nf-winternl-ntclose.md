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

# NtClose function


## -description


Deprecated. Closes the specified handle. <b>NtClose</b> is superseded by <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>.


## -parameters




### -param Handle [in]

The handle being closed.


## -returns



The various NTSTATUS values are defined in NTSTATUS.H, which is distributed with the Windows DDK.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The handle was closed.  

</td>
</tr>
</table>
 




## -remarks



The <b>NtClose</b> function closes handles to the following objects. 



<ul>
<li>Access token</li>
<li>Communications device </li>
<li>Console input </li>
<li>Console screen buffer </li>
<li>Event </li>
<li>File </li>
<li>File mapping </li>
<li>Job </li>
<li>Mailslot </li>
<li>Mutex </li>
<li>Named pipe </li>
<li>Process </li>
<li>Semaphore </li>
<li>Socket </li>
<li>Thread </li>
</ul>
Because there is no import library for this function, you must use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>.




