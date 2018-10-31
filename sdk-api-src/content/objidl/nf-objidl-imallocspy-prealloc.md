---
UID: NF:objidl.IMallocSpy.PreAlloc
title: IMallocSpy::PreAlloc
author: windows-sdk-content
description: Performs operations required before calling IMalloc::Alloc.
old-location: com\imallocspy_prealloc.htm
tech.root: com
ms.assetid: 43d8223b-a3fb-432c-ab4e-009d79ad8658
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IMallocSpy interface [COM],PreAlloc method, IMallocSpy.PreAlloc, IMallocSpy::PreAlloc, PreAlloc, PreAlloc method [COM], PreAlloc method [COM],IMallocSpy interface, _com_imallocspy_prealloc, com.imallocspy_prealloc, objidl/IMallocSpy::PreAlloc
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
 - IMallocSpy.PreAlloc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

