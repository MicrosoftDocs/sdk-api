---
UID: NF:combaseapi.CoTaskMemAlloc
title: CoTaskMemAlloc function
author: windows-sdk-content
description: Allocates a block of task memory in the same way that IMalloc::Alloc does.
old-location: com\cotaskmemalloc.htm
old-project: com
ms.assetid: c4cb588d-9482-4f90-a92e-75b604540d5c
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: CoTaskMemAlloc, CoTaskMemAlloc function [COM], _com_CoTaskMemAlloc, com.cotaskmemalloc, combaseapi/CoTaskMemAlloc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: REGCLS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoTaskMemAlloc
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
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
 

 

