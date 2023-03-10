---
UID: NF:objidl.IMallocSpy.PostAlloc
title: IMallocSpy::PostAlloc (objidl.h)
description: Performs operations required after calling IMalloc::Alloc.
helpviewer_keywords: ["IMallocSpy interface [COM]","PostAlloc method","IMallocSpy.PostAlloc","IMallocSpy::PostAlloc","PostAlloc","PostAlloc method [COM]","PostAlloc method [COM]","IMallocSpy interface","_com_imallocspy_postalloc","com.imallocspy_postalloc","objidl/IMallocSpy::PostAlloc"]
old-location: com\imallocspy_postalloc.htm
tech.root: com
ms.assetid: eaf2cb92-afdb-4f1f-a46a-83b6c72db07f
ms.date: 12/05/2018
ms.keywords: IMallocSpy interface [COM],PostAlloc method, IMallocSpy.PostAlloc, IMallocSpy::PostAlloc, PostAlloc, PostAlloc method [COM], PostAlloc method [COM],IMallocSpy interface, _com_imallocspy_postalloc, com.imallocspy_postalloc, objidl/IMallocSpy::PostAlloc
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
 - IMallocSpy::PostAlloc
 - objidl/IMallocSpy::PostAlloc
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
 - IMallocSpy.PostAlloc
---

# IMallocSpy::PostAlloc


## -description

Performs operations required after calling <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-alloc">IMalloc::Alloc</a>.

## -parameters

### -param pActual [in]

The pointer returned from <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-alloc">Alloc</a>.

## -returns

This method returns a pointer to the beginning of the block of memory actually allocated. This pointer is also returned to the caller of <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-alloc">Alloc</a>. If debug information is written at the front of the caller's allocation, this should be a forward offset from <i>pActual</i>. The value is the same as <i>pActual</i> if debug information is appended or if no debug information is attached.

## -remarks

When a spy object implementing <a href="/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a> is registered using the <a href="/windows/desktop/api/objbase/nf-objbase-coregistermallocspy">CoRegisterMallocSpy</a> function, COM calls <b>PostAlloc</b> after any call to <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-alloc">Alloc</a>. It takes as input a pointer to the allocation done by the call to <b>Alloc</b>, and returns a pointer to the beginning of the total allocation, which could include a forward offset from the other value if <a href="/windows/desktop/api/objidl/nf-objidl-imallocspy-prealloc">IMallocSpy::PreAlloc</a> was implemented to attach debug information to the allocation in this way. If not, the same pointer is returned and also becomes the return value to the caller of <b>Alloc</b>.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-imalloc-alloc">IMalloc::Alloc</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a>



<a href="/windows/desktop/api/objidl/nf-objidl-imallocspy-prealloc">IMallocSpy::PreAlloc</a>