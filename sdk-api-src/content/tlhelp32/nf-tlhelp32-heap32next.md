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

# Heap32Next function


## -description


Retrieves information about the next block of a heap that has been allocated by a process.


## -parameters




### -param lphe [out]

A pointer to a 
<a href="https://msdn.microsoft.com/c5f1dc66-d44f-4491-b0b7-961b163d0f1f">HEAPENTRY32</a> structure.


## -returns



Returns <b>TRUE</b> if information about the next block in the heap has been copied to the buffer or <b>FALSE</b> otherwise. The 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function returns <b>ERROR_NO_MORE_FILES</b> when no more objects in the heap exist and <b>ERROR_INVALID_DATA</b> if the heap appears to be corrupt or is modified during the walk in such a way that 
<b>Heap32Next</b> cannot continue.




## -remarks



To retrieve information for the first block of a heap, use the 
<a href="https://msdn.microsoft.com/79d01e3a-b11b-46b5-99d0-b445000288a7">Heap32First</a> function.

The <b>Heap32Next</b> function does not maintain a reference to the target process. If the target process dies, the system may create a new process using the same process identifier. Therefore, the caller should maintain a reference to the target process as long as it is using <b>Heap32Next</b>.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/cfa1d2a4-fec0-4089-9351-e0a26f9ecfe3">Traversing the Heap List</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/c5f1dc66-d44f-4491-b0b7-961b163d0f1f">HEAPENTRY32</a>



<a href="https://msdn.microsoft.com/631096fd-cb2c-4b19-aa71-d47060e2715c">Heap Lists and Heap Walking</a>



<a href="https://msdn.microsoft.com/79d01e3a-b11b-46b5-99d0-b445000288a7">Heap32First</a>



<a href="https://msdn.microsoft.com/83732bd6-f4cf-409d-ad17-86503d408dc3">Tool Help Functions</a>
 

 

