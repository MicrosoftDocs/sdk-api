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

# IMallocSpy::PreGetSize


## -description


Performs operations required before calling <a href="https://msdn.microsoft.com/abf8cb53-7c1b-4dde-9745-30a45ad030b7">IMalloc::GetSize</a>.


## -parameters




### -param pRequest [in]

The pointer that the caller is passing to <a href="https://msdn.microsoft.com/abf8cb53-7c1b-4dde-9745-30a45ad030b7">GetSize</a>.


### -param fSpyed [in]

Indicates whether the block of memory was allocated while the current spy was active.


## -returns



A pointer to the actual allocation for which the size is to be determined.




## -remarks



The <b>PreGetSize</b> method receives as its <i>pRequest</i> parameter the pointer the caller is passing to <a href="https://msdn.microsoft.com/abf8cb53-7c1b-4dde-9745-30a45ad030b7">IMalloc::GetSize</a>. It must then return a pointer to the actual allocation, which may have altered <i>pRequest</i> in the implementation of either the <a href="https://msdn.microsoft.com/43d8223b-a3fb-432c-ab4e-009d79ad8658">PreAlloc</a> or the <a href="https://msdn.microsoft.com/dd4db69c-3369-4aca-bc05-4c3c6850cc09">PreRealloc</a> method of <a href="https://msdn.microsoft.com/8ba500f7-c070-4788-b7fe-58b6a4e6a94c">IMallocSpy</a>. The pointer to the true allocation is then passed to <b>GetSize</b> as its <i>pv</i> parameter.


<a href="https://msdn.microsoft.com/abf8cb53-7c1b-4dde-9745-30a45ad030b7">IMalloc::GetSize</a> then returns the size determined, and COM passes this value to <a href="https://msdn.microsoft.com/ac619736-a434-46c0-9874-0cb646fdecae">IMallocSpy::PostGetSize</a> in <i>cbActual</i>.

The size determined by <a href="https://msdn.microsoft.com/abf8cb53-7c1b-4dde-9745-30a45ad030b7">GetSize</a> is the value returned by the <a href="https://msdn.microsoft.com/a8fcfd99-7b04-4aa3-8619-272b254551a3">HeapSize</a> function. This is the size originally requested. For example, a memory allocation request of 27 bytes returns an allocation of 32 bytes and <b>GetSize</b> returns 27.




## -see-also




<a href="https://msdn.microsoft.com/abf8cb53-7c1b-4dde-9745-30a45ad030b7">IMalloc::GetSize</a>



<a href="https://msdn.microsoft.com/8ba500f7-c070-4788-b7fe-58b6a4e6a94c">IMallocSpy</a>



<a href="https://msdn.microsoft.com/ac619736-a434-46c0-9874-0cb646fdecae">IMallocSpy::PostGetSize</a>
 

 

