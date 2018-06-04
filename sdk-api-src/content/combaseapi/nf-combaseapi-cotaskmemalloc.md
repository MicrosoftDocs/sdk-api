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

# CoTaskMemAlloc function


## -description


Allocates a block of task memory in the same way that <a href="https://msdn.microsoft.com/c9c9bdac-965f-4b18-9338-28a025930480">IMalloc::Alloc</a> does.


## -parameters




### -param cb [in]

The size of the memory block to be allocated, in bytes.


## -returns



If the function succeeds, it returns the allocated memory block. Otherwise, it returns <b>NULL</b>.




## -remarks



<b>CoTaskMemAlloc</b> uses the default allocator to allocate a memory block in the same way that <a href="https://msdn.microsoft.com/c9c9bdac-965f-4b18-9338-28a025930480">IMalloc::Alloc</a> does. It is not necessary to call the <a href="https://msdn.microsoft.com/d1d09fbe-ca5c-4480-b807-3afcc043ccb9">CoGetMalloc</a> function before calling <b>CoTaskMemAlloc</b>.

The initial contents of the returned memory block are undefined – there is no guarantee that the block has been initialized. The allocated block may be larger than <i>cb</i> bytes because of the space required for alignment and for maintenance information.

If <i>cb</i> is 0, <b>CoTaskMemAlloc</b> allocates a zero-length item and returns a valid pointer to that item. If there is insufficient memory available, <b>CoTaskMemAlloc</b> returns <b>NULL</b>. Applications should always check the return value from this function, even when requesting small amounts of memory, because there is no guarantee that the memory will be allocated.




## -see-also




<a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>



<a href="https://msdn.microsoft.com/83014a3e-198d-4b4b-91aa-0c0804c8e1bf">CoTaskMemRealloc</a>



<a href="https://msdn.microsoft.com/c9c9bdac-965f-4b18-9338-28a025930480">IMalloc::Alloc</a>
 

 

