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

# NdrOleAllocate function


## -description


The <b>NdrOleAllocate</b> function is used by RPC to allocate memory for an object interface. This function is a wrapper for the <a href="_com_cotaskmemalloc">CoTaskMemAlloc</a> function.


## -parameters




### -param Size

TBD




#### - size [in]

Memory to allocate, in bytes.


## -returns



Returns a void pointer to the allocated space upon success. Returns null upon failure due to insufficient memory.




## -remarks



To return a pointer other than a void, use a type cast on the return value. The memory pointed to by the return value is guaranteed to be suitably aligned for the storage of any type of object. If the <i>Size</i> parameter is zero, <b>NdrOleAllocate</b> allocates a zero-length item in the heap and returns a valid pointer to that item. Always check the return value from <b>NdrOleAllocate</b>, even if the amount of memory requested is small.




## -see-also




<a href="_com_cotaskmemalloc">CoTaskMemAlloc</a>
 

 

