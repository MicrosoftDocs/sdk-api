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

# IMallocSpy::PreFree


## -description


Performs operations required before calling <a href="https://msdn.microsoft.com/d65411ea-13d5-4932-a757-d897311e9e28">IMalloc::Free</a>. This method ensures that the pointer passed to <b>Free</b> points to the beginning of the actual allocation.


## -parameters




### -param pRequest [in]

A pointer to the block of memory that the caller is passing to <a href="https://msdn.microsoft.com/d65411ea-13d5-4932-a757-d897311e9e28">Free</a>.


### -param fSpyed [in]

Indicates whether the block of memory to be freed was allocated while the current spy was active.


## -returns



The value to be passed  to <a href="https://msdn.microsoft.com/d65411ea-13d5-4932-a757-d897311e9e28">IMalloc::Free</a>.




## -remarks



If <a href="https://msdn.microsoft.com/43d8223b-a3fb-432c-ab4e-009d79ad8658">IMallocSpy::PreAlloc</a> modified the original allocation request passed to <a href="https://msdn.microsoft.com/c9c9bdac-965f-4b18-9338-28a025930480">IMalloc::Alloc</a> (or <a href="https://msdn.microsoft.com/37de166a-04a5-4a10-83b3-dd19d0bb48a4">IMalloc::Realloc</a>), <b>PreFree</b> must supply a pointer to the actual allocation, which COM will pass to <a href="https://msdn.microsoft.com/d65411ea-13d5-4932-a757-d897311e9e28">IMalloc::Free</a>. For example, if the <b>PreAlloc</b>/<a href="https://msdn.microsoft.com/eaf2cb92-afdb-4f1f-a46a-83b6c72db07f">PostAlloc</a> pair attached a header used to store debug information to the beginning of the caller's allocation, <b>PreFree</b> must return a pointer to the beginning of this header so that all of the block that was allocated can be freed.




## -see-also




<a href="https://msdn.microsoft.com/d65411ea-13d5-4932-a757-d897311e9e28">IMalloc::Free</a>



<a href="https://msdn.microsoft.com/8ba500f7-c070-4788-b7fe-58b6a4e6a94c">IMallocSpy</a>



<a href="https://msdn.microsoft.com/b46b0b1e-6144-4bb8-84d5-9db5690b7421">IMallocSpy::PostFree</a>
 

 

