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

# tagTHREADENTRY32 structure


## -description


Describes an entry from a list of the threads executing in the system when a snapshot was taken.


## -struct-fields




### -field dwSize

The size of the structure, in bytes. Before calling the 
<a href="https://msdn.microsoft.com/d4cb7a19-850e-43b5-bda5-91be48382d2a">Thread32First</a> function, set this member to <code>sizeof(THREADENTRY32)</code>. If you do not initialize <b>dwSize</b>, 
<b>Thread32First</b> fails.


### -field cntUsage

This member is no longer used and is always set to zero.


### -field th32ThreadID

The thread identifier, compatible with the thread identifier returned by the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a> function.


### -field th32OwnerProcessID

The identifier of the process that created the thread.


### -field tpBasePri

The kernel base priority level assigned to the thread. The priority is a number from 0 to 31, with 0 representing the lowest possible thread priority. For more information, see <b>KeQueryPriorityThread</b>.


### -field tpDeltaPri

This member is no longer used and is always set to zero.


### -field dwFlags

This member is no longer used and is always set to zero.


## -see-also




<a href="https://msdn.microsoft.com/d4cb7a19-850e-43b5-bda5-91be48382d2a">Thread32First</a>



<a href="https://msdn.microsoft.com/5efe514e-626c-4138-97a0-bdad217c424f">Thread32Next</a>
 

 

