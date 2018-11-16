---
UID: NF:winternl.NtClose
title: NtClose function
author: windows-sdk-content
description: Deprecated. Closes the specified handle. NtClose is superseded by CloseHandle.
old-location: winprog\ntclose.htm
tech.root: DevNotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\ntclose.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: NtClose, NtClose function [Windows API], winprog.ntclose, winternl/NtClose, winui.ntclose
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winternl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Ntdll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdll.dll
 - ntoskrnl.exe
api_name:
 - NtClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- NtClose
: 
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




