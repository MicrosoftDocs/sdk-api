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

# CoTaskMemRealloc function


## -description


Changes the size of a previously allocated block of task memory.


## -parameters




### -param pv [in, optional]

A pointer to the memory block to be reallocated. This parameter can be <b>NULL</b>, as discussed in Remarks.


### -param cb [in]

The size of the memory block to be reallocated, in bytes. This parameter can be 0, as discussed in Remarks.


## -returns



If the function succeeds, it returns the reallocated memory block. Otherwise, it returns <b>NULL</b>.




## -remarks



This function changes the size of a previously allocated memory block in the same way that <a href="https://msdn.microsoft.com/37de166a-04a5-4a10-83b3-dd19d0bb48a4">IMalloc::Realloc</a> does. It is not necessary to call the <a href="https://msdn.microsoft.com/d1d09fbe-ca5c-4480-b807-3afcc043ccb9">CoGetMalloc</a> function to get a pointer to the OLE allocator before calling <b>CoTaskMemRealloc</b>.

The <i>pv</i> parameter points to the beginning of the memory block. If <i>pv</i> is <b>NULL</b>, <b>CoTaskMemRealloc</b> allocates a new memory block in the same way as the <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> function. If <i>pv</i> is not <b>NULL</b>, it should be a pointer returned by a prior call to <b>CoTaskMemAlloc</b>.

The <i>cb</i> parameter specifies the size of the new block. The contents of the block are unchanged up to the shorter of the new and old sizes, although the new block can be in a different location. Because the new block can be in a different memory location, the pointer returned by <b>CoTaskMemRealloc</b> is not guaranteed to be the pointer passed through the <i>pv</i> argument. If <i>pv</i> is not <b>NULL</b> and <i>cb</i> is 0, then the memory pointed to by <i>pv</i> is freed.

<b>CoTaskMemRealloc</b> returns a void pointer to the reallocated (and possibly moved) memory block. The return value is <b>NULL</b> if the size is 0 and the buffer argument is not <b>NULL</b>, or if there is not enough memory available to expand the block to the specified size. In the first case, the original block is freed; in the second case, the original block is unchanged.

The storage space pointed to by the return value is guaranteed to be suitably aligned for storage of any type of object. To get a pointer to a type other than <b>void</b>, use a type cast on the return value.




## -see-also




<a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>



<a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>



<a href="https://msdn.microsoft.com/37de166a-04a5-4a10-83b3-dd19d0bb48a4">IMalloc::Realloc</a>
 

 

