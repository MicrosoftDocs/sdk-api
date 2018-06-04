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

# IMallocSpy::PreAlloc


## -description


Performs operations required before calling <a href="https://msdn.microsoft.com/c9c9bdac-965f-4b18-9338-28a025930480">IMalloc::Alloc</a>.


## -parameters




### -param cbRequest [in]

The number of bytes specified in the allocation request the caller is passing to <a href="https://msdn.microsoft.com/c9c9bdac-965f-4b18-9338-28a025930480">Alloc</a>.


## -returns



The number of bytes specified in the call to <a href="https://msdn.microsoft.com/c9c9bdac-965f-4b18-9338-28a025930480">Alloc</a>, which can be greater than or equal to the value of <i>cbRequest</i>.




## -remarks



The <b>PreAlloc</b> implementation may extend and/or modify the allocation to store debug-specific information with the allocation.

<b>PreAlloc</b> can force memory allocation failure by returning 0, allowing testing to ensure that the application handles allocation failure gracefully in all cases. In this case, <a href="https://msdn.microsoft.com/eaf2cb92-afdb-4f1f-a46a-83b6c72db07f">IMallocSpy::PostAlloc</a> is not called and <a href="https://msdn.microsoft.com/c9c9bdac-965f-4b18-9338-28a025930480">Alloc</a> returns <b>NULL</b>. Forcing allocation failure is effective only if <i>cbRequest</i> is not equal to 0. If <b>PreAlloc</b> is forcing failure by returning <b>NULL</b>, <b>PostAlloc</b> is not called. However, <b>Alloc</b> encounters a real memory failure and returns <b>NULL</b>, <b>PostAlloc</b> is called.



The call to <b>PreAlloc</b> through the return from <a href="https://msdn.microsoft.com/eaf2cb92-afdb-4f1f-a46a-83b6c72db07f">PostAlloc</a> is guaranteed to be thread-safe.




## -see-also




<a href="https://msdn.microsoft.com/c9c9bdac-965f-4b18-9338-28a025930480">IMalloc::Alloc</a>



<a href="https://msdn.microsoft.com/8ba500f7-c070-4788-b7fe-58b6a4e6a94c">IMallocSpy</a>



<a href="https://msdn.microsoft.com/eaf2cb92-afdb-4f1f-a46a-83b6c72db07f">IMallocSpy::PostAlloc</a>
 

 

