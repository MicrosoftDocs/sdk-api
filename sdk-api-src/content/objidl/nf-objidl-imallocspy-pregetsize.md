---
UID: NF:objidl.IMallocSpy.PreGetSize
title: IMallocSpy::PreGetSize method
author: windows-driver-content
description: Performs operations required before calling IMalloc::GetSize.
old-location: com\imallocspy_pregetsize.htm
old-project: com
ms.assetid: 7bebc327-490e-4a41-8043-5d7211e645f5
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IMallocSpy, IMallocSpy interface [COM], PreGetSize method, IMallocSpy::PreGetSize, PreGetSize method [COM], PreGetSize method [COM], IMallocSpy interface, PreGetSize,IMallocSpy.PreGetSize, _com_imallocspy_pregetsize, com.imallocspy_pregetsize, objidl/IMallocSpy::PreGetSize
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
-	IMallocSpy.PreGetSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMallocSpy::PreGetSize method


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
 

 

