---
UID: NF:objidl.IMallocSpy.PreFree
title: IMallocSpy::PreFree (objidl.h)
description: Performs operations required before calling IMalloc::Free. This method ensures that the pointer passed to Free points to the beginning of the actual allocation.
helpviewer_keywords: ["IMallocSpy interface [COM]","PreFree method","IMallocSpy.PreFree","IMallocSpy::PreFree","PreFree","PreFree method [COM]","PreFree method [COM]","IMallocSpy interface","_com_imallocspy_prefree","com.imallocspy_prefree","objidl/IMallocSpy::PreFree"]
old-location: com\imallocspy_prefree.htm
tech.root: com
ms.assetid: 528eedac-e8cc-4dc7-8287-c023ebefb72c
ms.date: 12/05/2018
ms.keywords: IMallocSpy interface [COM],PreFree method, IMallocSpy.PreFree, IMallocSpy::PreFree, PreFree, PreFree method [COM], PreFree method [COM],IMallocSpy interface, _com_imallocspy_prefree, com.imallocspy_prefree, objidl/IMallocSpy::PreFree
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
 - IMallocSpy::PreFree
 - objidl/IMallocSpy::PreFree
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
 - IMallocSpy.PreFree
---

# IMallocSpy::PreFree


## -description

Performs operations required before calling <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-free">IMalloc::Free</a>. This method ensures that the pointer passed to <b>Free</b> points to the beginning of the actual allocation.

## -parameters

### -param pRequest [in]

A pointer to the block of memory that the caller is passing to <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-free">Free</a>.

### -param fSpyed [in]

Indicates whether the block of memory to be freed was allocated while the current spy was active.

## -returns

The value to be passed  to <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-free">IMalloc::Free</a>.

## -remarks

If <a href="/windows/desktop/api/objidl/nf-objidl-imallocspy-prealloc">IMallocSpy::PreAlloc</a> modified the original allocation request passed to <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-alloc">IMalloc::Alloc</a> (or <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-realloc">IMalloc::Realloc</a>), <b>PreFree</b> must supply a pointer to the actual allocation, which COM will pass to <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-free">IMalloc::Free</a>. For example, if the <b>PreAlloc</b>/<a href="/windows/desktop/api/objidl/nf-objidl-imallocspy-postalloc">PostAlloc</a> pair attached a header used to store debug information to the beginning of the caller's allocation, <b>PreFree</b> must return a pointer to the beginning of this header so that all of the block that was allocated can be freed.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-imalloc-free">IMalloc::Free</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a>



<a href="/windows/desktop/api/objidl/nf-objidl-imallocspy-postfree">IMallocSpy::PostFree</a>