---
UID: NF:objidl.IMallocSpy.PreAlloc
title: IMallocSpy::PreAlloc (objidl.h)
description: Performs operations required before calling IMalloc::Alloc.
helpviewer_keywords: ["IMallocSpy interface [COM]","PreAlloc method","IMallocSpy.PreAlloc","IMallocSpy::PreAlloc","PreAlloc","PreAlloc method [COM]","PreAlloc method [COM]","IMallocSpy interface","_com_imallocspy_prealloc","com.imallocspy_prealloc","objidl/IMallocSpy::PreAlloc"]
old-location: com\imallocspy_prealloc.htm
tech.root: com
ms.assetid: 43d8223b-a3fb-432c-ab4e-009d79ad8658
ms.date: 12/05/2018
ms.keywords: IMallocSpy interface [COM],PreAlloc method, IMallocSpy.PreAlloc, IMallocSpy::PreAlloc, PreAlloc, PreAlloc method [COM], PreAlloc method [COM],IMallocSpy interface, _com_imallocspy_prealloc, com.imallocspy_prealloc, objidl/IMallocSpy::PreAlloc
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
 - IMallocSpy::PreAlloc
 - objidl/IMallocSpy::PreAlloc
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
 - IMallocSpy.PreAlloc
---

# IMallocSpy::PreAlloc


## -description

Performs operations required before calling <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-alloc">IMalloc::Alloc</a>.

## -parameters

### -param cbRequest [in]

The number of bytes specified in the allocation request the caller is passing to <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-alloc">Alloc</a>.

## -returns

The number of bytes specified in the call to <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-alloc">Alloc</a>, which can be greater than or equal to the value of <i>cbRequest</i>.

## -remarks

The <b>PreAlloc</b> implementation may extend and/or modify the allocation to store debug-specific information with the allocation.

<b>PreAlloc</b> can force memory allocation failure by returning 0, allowing testing to ensure that the application handles allocation failure gracefully in all cases. In this case, <a href="/windows/desktop/api/objidl/nf-objidl-imallocspy-postalloc">IMallocSpy::PostAlloc</a> is not called and <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-alloc">Alloc</a> returns <b>NULL</b>. Forcing allocation failure is effective only if <i>cbRequest</i> is not equal to 0. If <b>PreAlloc</b> is forcing failure by returning <b>NULL</b>, <b>PostAlloc</b> is not called. However, <b>Alloc</b> encounters a real memory failure and returns <b>NULL</b>, <b>PostAlloc</b> is called.



The call to <b>PreAlloc</b> through the return from <a href="/windows/desktop/api/objidl/nf-objidl-imallocspy-postalloc">PostAlloc</a> is guaranteed to be thread-safe.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-imalloc-alloc">IMalloc::Alloc</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a>



<a href="/windows/desktop/api/objidl/nf-objidl-imallocspy-postalloc">IMallocSpy::PostAlloc</a>