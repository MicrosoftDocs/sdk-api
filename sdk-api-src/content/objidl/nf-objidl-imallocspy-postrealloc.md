---
UID: NF:objidl.IMallocSpy.PostRealloc
title: IMallocSpy::PostRealloc
author: windows-sdk-content
description: Performs operations required after calling IMalloc::Realloc.
old-location: com\imallocspy_postrealloc.htm
tech.root: com
ms.assetid: 77f86494-f7b3-4c12-bb42-ad74161a1dff
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: IMallocSpy interface [COM],PostRealloc method, IMallocSpy.PostRealloc, IMallocSpy::PostRealloc, PostRealloc, PostRealloc method [COM], PostRealloc method [COM],IMallocSpy interface, _com_imallocspy_postrealloc, com.imallocspy_postrealloc, objidl/IMallocSpy::PostRealloc
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
 - IMallocSpy.PostRealloc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMallocSpy::PostRealloc


## -description


Performs operations required after calling <a href="https://msdn.microsoft.com/37de166a-04a5-4a10-83b3-dd19d0bb48a4">IMalloc::Realloc</a>.


## -parameters




### -param pActual [in]

The pointer specified in the call to <a href="https://msdn.microsoft.com/37de166a-04a5-4a10-83b3-dd19d0bb48a4">Realloc</a>.


### -param fSpyed [in]

Indicates whether the block of memory was allocated while the current spy was active.


## -returns



The method returns a pointer to the beginning of the block actually allocated. This pointer is also returned to the caller of <a href="https://msdn.microsoft.com/37de166a-04a5-4a10-83b3-dd19d0bb48a4">IMalloc::Realloc</a>. If debug information is written at the front of the caller's allocation, it should be a forward offset from <i>pActual</i>. The value should be the same as <i>pActual</i> if debug information is appended or if no debug information is attached.




## -remarks



If memory is successfully reallocated while the spy is active, <i>fSpyed</i> will be <b>TRUE</b> in subsequent calls to <a href="https://msdn.microsoft.com/8ba500f7-c070-4788-b7fe-58b6a4e6a94c">IMallocSpy</a> methods that track the reallocated memory, even if <i>fSpyed</i> was previously <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/37de166a-04a5-4a10-83b3-dd19d0bb48a4">IMalloc::Realloc</a>



<a href="https://msdn.microsoft.com/8ba500f7-c070-4788-b7fe-58b6a4e6a94c">IMallocSpy</a>



<a href="https://msdn.microsoft.com/dd4db69c-3369-4aca-bc05-4c3c6850cc09">IMallocSpy::PreRealloc</a>
 

 

