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

# IAMDevMemoryAllocator::GetInfo


## -description



<div class="alert"><b>Note</b>  The <b>IAMDevMemoryAllocator</b> interface is deprecated.</div>
<div> </div>
Retrieves information about the memory capabilities.




## -parameters




### -param pdwcbTotalFree [out]

Pointer to the total free memory size.


### -param pdwcbLargestFree [out]

Pointer to the returned largest free memory size.


### -param pdwcbTotalMemory [out]

Pointer to the returned total memory size.


### -param pdwcbMinimumChunk [out]

Pointer to the returned minimum chunk size, giving granularity and alignment rules.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Use this method to find out the total amount of memory available. This method returns values for the entire on-board memory that is available on that device. If multiple filters (devices) share the memory, it will return the amount available to that specific device, which might be a portion of the total amount of on-board memory. This amount will be implementation-specific. For example, the on-board memory manager on the codec might be able to access all 32 megabytes (MB) of memory on the card. However, individual pin implementations of <a href="https://msdn.microsoft.com/bab1e582-928a-408b-a9c5-8e9827e9928b">IAMDevMemoryAllocator</a> only report a portion of this memory.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/bab1e582-928a-408b-a9c5-8e9827e9928b">IAMDevMemoryAllocator Interface</a>
 

 

