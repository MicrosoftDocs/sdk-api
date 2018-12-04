---
UID: NF:objidl.IMallocSpy.PreFree
title: IMallocSpy::PreFree
author: windows-sdk-content
description: Performs operations required before calling IMalloc::Free. This method ensures that the pointer passed to Free points to the beginning of the actual allocation.
old-location: com\imallocspy_prefree.htm
tech.root: com
ms.assetid: 528eedac-e8cc-4dc7-8287-c023ebefb72c
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IMallocSpy interface [COM],PreFree method, IMallocSpy.PreFree, IMallocSpy::PreFree, PreFree, PreFree method [COM], PreFree method [COM],IMallocSpy interface, _com_imallocspy_prefree, com.imallocspy_prefree, objidl/IMallocSpy::PreFree
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
 - IMallocSpy.PreFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

