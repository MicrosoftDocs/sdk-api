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

# EngAllocMem macro


## -description


The <b>EngAllocMem</b> function allocates a block of memory and inserts a caller-supplied tag before the allocation.


## -parameters




### -param flags

TBD


### -param cj

TBD


### -param tag

TBD






#### - Flags [in]

Specifies how to allocate memory. This parameter can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
FL_NONPAGED_MEMORY

</td>
<td>
Allocate memory from the nonpaged pool. If this flag is not set, the memory is allocated from the system's paged pool.

</td>
</tr>
<tr>
<td>
FL_ZERO_MEMORY

</td>
<td>
Zero-initialize the allocated memory. If this flag is not set, the memory is returned uninitialized.

</td>
</tr>
</table>
 


#### - MemSize [in]

Specifies the number of bytes to allocate.


#### - Tag [in]

Specifies a 4-byte <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">pool tag</a> that uniquely identifies the driver that does the memory allocation. For more information about pool tags, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff544520">ExAllocatePoolWithTag</a>.


## -remarks



When the memory is no longer needed, it should be freed by a call to the <b>EngFreeMem</b> function. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564895">EngFreeMem</a>
 

 

