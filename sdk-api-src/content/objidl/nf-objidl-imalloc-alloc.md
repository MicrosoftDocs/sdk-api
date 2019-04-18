---
UID: NF:objidl.IMalloc.Alloc
title: IMalloc::Alloc (objidl.h)
author: windows-sdk-content
description: Allocates a block of memory.
old-location: com\imalloc_alloc.htm
tech.root: com
ms.assetid: c9c9bdac-965f-4b18-9338-28a025930480
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Alloc, Alloc method [COM], Alloc method [COM],IMalloc interface, IMalloc interface [COM],Alloc method, IMalloc.Alloc, IMalloc::Alloc, _com_imalloc_alloc, com.imalloc_alloc, objidl/IMalloc::Alloc
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IMalloc.Alloc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
 

 

