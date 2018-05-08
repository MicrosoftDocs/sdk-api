---
UID: NF:objidl.IMallocSpy.PostGetSize
title: IMallocSpy::PostGetSize
author: windows-driver-content
description: Performs operations required after calling IMalloc::GetSize.
old-location: com\imallocspy_postgetsize.htm
old-project: com
ms.assetid: ac619736-a434-46c0-9874-0cb646fdecae
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: IMallocSpy interface [COM],PostGetSize method, IMallocSpy.PostGetSize, IMallocSpy::PostGetSize, PostGetSize, PostGetSize method [COM], PostGetSize method [COM],IMallocSpy interface, _com_imallocspy_postgetsize, com.imallocspy_postgetsize, objidl/IMallocSpy::PostGetSize
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ObjIdl.h
api_name:
-	IMallocSpy.PostGetSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMallocSpy::PostGetSize


## -description


Performs operations required after calling <a href="https://msdn.microsoft.com/abf8cb53-7c1b-4dde-9745-30a45ad030b7">IMalloc::GetSize</a>.


## -parameters




### -param cbActual [in]

The number of bytes in the allocation, as returned by <a href="https://msdn.microsoft.com/abf8cb53-7c1b-4dde-9745-30a45ad030b7">GetSize</a>.


### -param fSpyed [in]

Indicates whether the block of memory was allocated while the current spy was active.


## -returns



The value returned by <a href="https://msdn.microsoft.com/abf8cb53-7c1b-4dde-9745-30a45ad030b7">IMalloc::GetSize</a>, which is the size of the allocated block of memory, in bytes.




## -remarks



The size determined by <a href="https://msdn.microsoft.com/abf8cb53-7c1b-4dde-9745-30a45ad030b7">GetSize</a> is the value returned by the <a href="https://msdn.microsoft.com/a8fcfd99-7b04-4aa3-8619-272b254551a3">HeapSize</a> function. This is the size originally requested. For example, a memory allocation request of 27 bytes returns an allocation of 32 bytes and <b>GetSize</b> returns 27.




## -see-also




<a href="https://msdn.microsoft.com/abf8cb53-7c1b-4dde-9745-30a45ad030b7">IMalloc::GetSize</a>



<a href="https://msdn.microsoft.com/8ba500f7-c070-4788-b7fe-58b6a4e6a94c">IMallocSpy</a>



<a href="https://msdn.microsoft.com/7bebc327-490e-4a41-8043-5d7211e645f5">IMallocSpy::PreGetSize</a>
 

 

