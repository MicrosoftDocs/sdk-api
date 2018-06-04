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

# IAMDevMemoryAllocator::Alloc


## -description



<div class="alert"><b>Note</b>  The <b>IAMDevMemoryAllocator</b> interface is deprecated.</div>
<div> </div>
Allocates a memory buffer.




## -parameters




### -param ppBuffer [out]

Pointer that will receive the address of the allocated memory buffer.


### -param pdwcbBuffer [in, out]

Pointer to a <b>DWORD</b> whose input value is the number of bytes to allocate and whose output value is the actual number of bytes allocated.


## -returns



Returns S_OK if the desired quantity of memory was allocated, S_FALSE if memory was unavailable.




## -remarks



Call this method to allocate a block of memory from the available pool.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/bab1e582-928a-408b-a9c5-8e9827e9928b">IAMDevMemoryAllocator Interface</a>



<a href="https://msdn.microsoft.com/d86d3016-bca0-4a0b-946b-f50c49266c67">IAMDevMemoryAllocator::Free</a>
 

 

