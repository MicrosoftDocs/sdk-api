---
UID: NF:objidl.IMallocSpy.PostAlloc
title: IMallocSpy::PostAlloc
author: windows-sdk-content
description: Performs operations required after calling IMalloc::Alloc.
old-location: com\imallocspy_postalloc.htm
tech.root: com
ms.assetid: eaf2cb92-afdb-4f1f-a46a-83b6c72db07f
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IMallocSpy interface [COM],PostAlloc method, IMallocSpy.PostAlloc, IMallocSpy::PostAlloc, PostAlloc, PostAlloc method [COM], PostAlloc method [COM],IMallocSpy interface, _com_imallocspy_postalloc, com.imallocspy_postalloc, objidl/IMallocSpy::PostAlloc
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
 - IMallocSpy.PostAlloc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- objidl.h
: 
- IMallocSpy.PostAlloc
: 
---

# IMallocSpy::PostAlloc


## -description


Performs operations required after calling <a href="https://msdn.microsoft.com/c9c9bdac-965f-4b18-9338-28a025930480">IMalloc::Alloc</a>.


## -parameters




### -param pActual [in]

The pointer returned from <a href="https://msdn.microsoft.com/c9c9bdac-965f-4b18-9338-28a025930480">Alloc</a>.


## -returns



This method returns a pointer to the beginning of the block of memory actually allocated. This pointer is also returned to the caller of <a href="https://msdn.microsoft.com/c9c9bdac-965f-4b18-9338-28a025930480">Alloc</a>. If debug information is written at the front of the caller's allocation, this should be a forward offset from <i>pActual</i>. The value is the same as <i>pActual</i> if debug information is appended or if no debug information is attached.




## -remarks



When a spy object implementing <a href="https://msdn.microsoft.com/8ba500f7-c070-4788-b7fe-58b6a4e6a94c">IMallocSpy</a> is registered using the <a href="https://msdn.microsoft.com/28623c1f-e158-4cc5-8c7f-c13d7a65aa76">CoRegisterMallocSpy</a> function, COM calls <b>PostAlloc</b> after any call to <a href="https://msdn.microsoft.com/c9c9bdac-965f-4b18-9338-28a025930480">Alloc</a>. It takes as input a pointer to the allocation done by the call to <b>Alloc</b>, and returns a pointer to the beginning of the total allocation, which could include a forward offset from the other value if <a href="https://msdn.microsoft.com/43d8223b-a3fb-432c-ab4e-009d79ad8658">IMallocSpy::PreAlloc</a> was implemented to attach debug information to the allocation in this way. If not, the same pointer is returned and also becomes the return value to the caller of <b>Alloc</b>.




## -see-also




<a href="https://msdn.microsoft.com/c9c9bdac-965f-4b18-9338-28a025930480">IMalloc::Alloc</a>



<a href="https://msdn.microsoft.com/8ba500f7-c070-4788-b7fe-58b6a4e6a94c">IMallocSpy</a>



<a href="https://msdn.microsoft.com/43d8223b-a3fb-432c-ab4e-009d79ad8658">IMallocSpy::PreAlloc</a>
 

 

