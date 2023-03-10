---
UID: NF:objidl.IMallocSpy.PreGetSize
title: IMallocSpy::PreGetSize (objidl.h)
description: Performs operations required before calling IMalloc::GetSize.
helpviewer_keywords: ["IMallocSpy interface [COM]","PreGetSize method","IMallocSpy.PreGetSize","IMallocSpy::PreGetSize","PreGetSize","PreGetSize method [COM]","PreGetSize method [COM]","IMallocSpy interface","_com_imallocspy_pregetsize","com.imallocspy_pregetsize","objidl/IMallocSpy::PreGetSize"]
old-location: com\imallocspy_pregetsize.htm
tech.root: com
ms.assetid: 7bebc327-490e-4a41-8043-5d7211e645f5
ms.date: 12/05/2018
ms.keywords: IMallocSpy interface [COM],PreGetSize method, IMallocSpy.PreGetSize, IMallocSpy::PreGetSize, PreGetSize, PreGetSize method [COM], PreGetSize method [COM],IMallocSpy interface, _com_imallocspy_pregetsize, com.imallocspy_pregetsize, objidl/IMallocSpy::PreGetSize
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
 - IMallocSpy::PreGetSize
 - objidl/IMallocSpy::PreGetSize
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
 - IMallocSpy.PreGetSize
---

# IMallocSpy::PreGetSize


## -description

Performs operations required before calling <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-getsize">IMalloc::GetSize</a>.

## -parameters

### -param pRequest [in]

The pointer that the caller is passing to <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-getsize">GetSize</a>.

### -param fSpyed [in]

Indicates whether the block of memory was allocated while the current spy was active.

## -returns

A pointer to the actual allocation for which the size is to be determined.

## -remarks

The <b>PreGetSize</b> method receives as its <i>pRequest</i> parameter the pointer the caller is passing to <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-getsize">IMalloc::GetSize</a>. It must then return a pointer to the actual allocation, which may have altered <i>pRequest</i> in the implementation of either the <a href="/windows/desktop/api/objidl/nf-objidl-imallocspy-prealloc">PreAlloc</a> or the <a href="/windows/desktop/api/objidl/nf-objidl-imallocspy-prerealloc">PreRealloc</a> method of <a href="/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a>. The pointer to the true allocation is then passed to <b>GetSize</b> as its <i>pv</i> parameter.


<a href="/windows/desktop/api/objidl/nf-objidl-imalloc-getsize">IMalloc::GetSize</a> then returns the size determined, and COM passes this value to <a href="/windows/desktop/api/objidl/nf-objidl-imallocspy-postgetsize">IMallocSpy::PostGetSize</a> in <i>cbActual</i>.

The size determined by <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-getsize">GetSize</a> is the value returned by the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapsize">HeapSize</a> function. This is the size originally requested. For example, a memory allocation request of 27 bytes returns an allocation of 32 bytes and <b>GetSize</b> returns 27.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-imalloc-getsize">IMalloc::GetSize</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a>



<a href="/windows/desktop/api/objidl/nf-objidl-imallocspy-postgetsize">IMallocSpy::PostGetSize</a>