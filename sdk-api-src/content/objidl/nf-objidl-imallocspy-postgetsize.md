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
 

 

