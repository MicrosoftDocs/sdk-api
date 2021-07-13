---
UID: NF:objidl.IMallocSpy.PostHeapMinimize
title: IMallocSpy::PostHeapMinimize (objidl.h)
description: Performs operations required after calling IMalloc::HeapMinimize.
helpviewer_keywords: ["IMallocSpy interface [COM]","PostHeapMinimize method","IMallocSpy.PostHeapMinimize","IMallocSpy::PostHeapMinimize","PostHeapMinimize","PostHeapMinimize method [COM]","PostHeapMinimize method [COM]","IMallocSpy interface","_com_imallocspy_postheapminimize","com.imallocspy_postheapminimize","objidl/IMallocSpy::PostHeapMinimize"]
old-location: com\imallocspy_postheapminimize.htm
tech.root: com
ms.assetid: 9d51c34e-6ed1-493d-8999-e67c4a60f6b6
ms.date: 12/05/2018
ms.keywords: IMallocSpy interface [COM],PostHeapMinimize method, IMallocSpy.PostHeapMinimize, IMallocSpy::PostHeapMinimize, PostHeapMinimize, PostHeapMinimize method [COM], PostHeapMinimize method [COM],IMallocSpy interface, _com_imallocspy_postheapminimize, com.imallocspy_postheapminimize, objidl/IMallocSpy::PostHeapMinimize
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMallocSpy::PostHeapMinimize
 - objidl/IMallocSpy::PostHeapMinimize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IMallocSpy.PostHeapMinimize
---

# IMallocSpy::PostHeapMinimize


## -description

Performs operations required after calling <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-heapminimize">IMalloc::HeapMinimize</a>.



## -remarks

When a spy object implementing <a href="/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a> is registered using the <a href="/windows/desktop/api/objbase/nf-objbase-coregistermallocspy">CoRegisterMallocSpy</a> function, COM calls this method immediately after any call to <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-free">IMalloc::Free</a>. This method is included for completeness and consistency; it is not anticipated that developers will implement significant functionality in this method.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-imalloc-heapminimize">IMalloc::HeapMinimize</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a>



<a href="/windows/desktop/api/objidl/nf-objidl-imallocspy-preheapminimize">IMallocSpy::PreHeapMinimize</a>
