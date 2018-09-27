---
UID: NF:objidl.IMallocSpy.PreRealloc
title: IMallocSpy::PreRealloc
author: windows-sdk-content
description: Performs operations required before calling IMalloc::Realloc.
old-location: com\imallocspy_prerealloc.htm
tech.root: com
ms.assetid: dd4db69c-3369-4aca-bc05-4c3c6850cc09
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMallocSpy interface [COM],PreRealloc method, IMallocSpy.PreRealloc, IMallocSpy::PreRealloc, PreRealloc, PreRealloc method [COM], PreRealloc method [COM],IMallocSpy interface, _com_imallocspy_prerealloc, com.imallocspy_prerealloc, objidl/IMallocSpy::PreRealloc
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
 - IMallocSpy.PreRealloc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMallocSpy::PreRealloc


## -description


Performs operations required before calling <a href="https://msdn.microsoft.com/37de166a-04a5-4a10-83b3-dd19d0bb48a4">IMalloc::Realloc</a>.


## -parameters




### -param pRequest [in]

The pointer to the block of memory specified in the call to <a href="https://msdn.microsoft.com/37de166a-04a5-4a10-83b3-dd19d0bb48a4">IMalloc::Realloc</a>.


### -param cbRequest [in]

The byte count of the block of memory as specified in the original call to <a href="https://msdn.microsoft.com/37de166a-04a5-4a10-83b3-dd19d0bb48a4">IMalloc::Realloc</a>.


### -param ppNewRequest [out]

Address of pointer variable that receives a pointer to the memory block to be reallocated. This may be different from the pointer in <i>pRequest</i> if the implementation of <b>PreRealloc</b> extends or modifies the reallocation. This is pointer should always be stored by <b>PreRealloc</b>.


### -param fSpyed [in]

Indicates whether the block of memory was allocated while this spy was active.


## -returns



The byte count to be passed to <a href="https://msdn.microsoft.com/37de166a-04a5-4a10-83b3-dd19d0bb48a4">IMalloc::Realloc</a>.




## -remarks



The <b>PreRealloc</b> implementation may extend and/or modify the allocation to store debug-specific information with the allocation. Thus, the <i>ppNewRequest</i> parameter may differ from <i>pRequest</i>, a pointer to the request specified in the original call to <a href="https://msdn.microsoft.com/37de166a-04a5-4a10-83b3-dd19d0bb48a4">Realloc</a>.

<b>PreRealloc</b> can force memory allocation failure by returning 0, allowing testing to ensure that the application handles allocation failure gracefully in all cases. In this case, <a href="https://msdn.microsoft.com/77f86494-f7b3-4c12-bb42-ad74161a1dff">PostRealloc</a> is not called and <a href="https://msdn.microsoft.com/37de166a-04a5-4a10-83b3-dd19d0bb48a4">Realloc</a> returns <b>NULL</b>. However, if <b>Realloc</b> encounters a real memory failure and returns <b>NULL</b>, <b>PostRealloc</b> is called. Forcing allocation failure is effective only if <i>cbRequest</i> is not equal to 0.




## -see-also




<a href="https://msdn.microsoft.com/37de166a-04a5-4a10-83b3-dd19d0bb48a4">IMalloc::Realloc</a>



<a href="https://msdn.microsoft.com/8ba500f7-c070-4788-b7fe-58b6a4e6a94c">IMallocSpy</a>



<a href="https://msdn.microsoft.com/77f86494-f7b3-4c12-bb42-ad74161a1dff">IMallocSpy::PostRealloc</a>
 

 

