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

# IMalloc::Alloc


## -description


Allocates a block of memory.


## -parameters




### -param cb [in]

The size of the memory block to be allocated, in bytes.


## -returns



If the method succeeds, the return value is a pointer to the allocated block of memory. Otherwise, it is <b>NULL</b>.

Applications should always check the return value from this method, even when requesting small amounts of memory, because there is no guarantee the memory will be allocated.




## -remarks



The initial contents of the returned memory block are undefinedâ€”there is no guarantee that the block has been initialized, so you should initialize it in your code. The allocated block may be larger than <i>cb</i> bytes because of the space required for alignment and for maintenance information.

If <i>cb</i> is zero, <b>Alloc</b> allocates a zero-length item and returns a valid pointer to that item. If there is insufficient memory available, <b>Alloc</b> returns <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>



<a href="https://msdn.microsoft.com/047f281e-2665-4d6d-9a0b-918cd3339447">IMalloc</a>
 

 

