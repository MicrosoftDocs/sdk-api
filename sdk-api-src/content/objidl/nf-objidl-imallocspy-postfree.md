---
UID: NF:objidl.IMallocSpy.PostFree
title: IMallocSpy::PostFree (objidl.h)
author: windows-sdk-content
description: Performs operations required after calling IMalloc::Free.
old-location: com\imallocspy_postfree.htm
tech.root: com
ms.assetid: b46b0b1e-6144-4bb8-84d5-9db5690b7421
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMallocSpy interface [COM],PostFree method, IMallocSpy.PostFree, IMallocSpy::PostFree, PostFree, PostFree method [COM], PostFree method [COM],IMallocSpy interface, _com_imallocspy_postfree, com.imallocspy_postfree, objidl/IMallocSpy::PostFree
ms.topic: method
f1_keywords: ["objidl/IMallocSpy.PostFree"]
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
 - IMallocSpy.PostFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMallocSpy::PostFree


## -description


Performs operations required after calling <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imalloc-free">IMalloc::Free</a>.


## -parameters




### -param fSpyed [in]

Indicates whether the block of memory to be freed was allocated while the current spy was active.


## -returns



This method does not return a value.




## -remarks



When a spy object implementing <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a> is registered using <a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-coregistermallocspy">CoRegisterMallocSpy</a> function, COM calls this method immediately after any call to <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imalloc-free">IMalloc::Free</a>. This method is included for completeness and consistencyâ€”it is not anticipated that developers will implement significant functionality in this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imalloc-free">IMalloc::Free</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imallocspy-prefree">IMallocSpy::PreFree</a>
 

 

