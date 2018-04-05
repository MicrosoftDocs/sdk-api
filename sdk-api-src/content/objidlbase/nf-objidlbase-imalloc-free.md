---
UID: NF:objidlbase.IMalloc.Free
title: IMalloc::Free method
author: windows-driver-content
description: Frees a previously allocated block of memory.
old-location: com\imalloc_free.htm
old-project: com
ms.assetid: d65411ea-13d5-4932-a757-d897311e9e28
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: Free method [COM], Free method [COM], IMalloc interface, Free,IMalloc.Free, IMalloc, IMalloc interface [COM], Free method, IMalloc::Free, _com_imalloc_free, com.imalloc_free, objidlbase/IMalloc::Free
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidlbase.h
req.include-header: ObjIdl.h
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
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	objidlbase.h
api_name:
-	IMalloc.Free
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMalloc::Free method


## -description


Frees a previously allocated block of memory.


## -parameters




### -param pv [in]

A pointer to the memory block to be freed. If this parameter is <b>NULL</b>, this method has no effect.


## -returns



This method does not return a value.




## -remarks



This method frees a block of memory previously allocated through a call to <a href="https://msdn.microsoft.com/c9c9bdac-965f-4b18-9338-28a025930480">IMalloc::Alloc</a> or <a href="https://msdn.microsoft.com/37de166a-04a5-4a10-83b3-dd19d0bb48a4">IMalloc::Realloc</a>. The number of bytes freed equals the number of bytes that were allocated. After the call, the block of memory pointed to by <i>pv</i> is invalid and can no longer be used.




## -see-also




<a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>



<a href="https://msdn.microsoft.com/047f281e-2665-4d6d-9a0b-918cd3339447">IMalloc</a>
 

 

