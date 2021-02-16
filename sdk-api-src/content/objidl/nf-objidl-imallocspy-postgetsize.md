---
UID: NF:objidl.IMallocSpy.PostGetSize
title: IMallocSpy::PostGetSize (objidl.h)
description: Performs operations required after calling IMalloc::GetSize.
helpviewer_keywords: ["IMallocSpy interface [COM]","PostGetSize method","IMallocSpy.PostGetSize","IMallocSpy::PostGetSize","PostGetSize","PostGetSize method [COM]","PostGetSize method [COM]","IMallocSpy interface","_com_imallocspy_postgetsize","com.imallocspy_postgetsize","objidl/IMallocSpy::PostGetSize"]
old-location: com\imallocspy_postgetsize.htm
tech.root: com
ms.assetid: ac619736-a434-46c0-9874-0cb646fdecae
ms.date: 12/05/2018
ms.keywords: IMallocSpy interface [COM],PostGetSize method, IMallocSpy.PostGetSize, IMallocSpy::PostGetSize, PostGetSize, PostGetSize method [COM], PostGetSize method [COM],IMallocSpy interface, _com_imallocspy_postgetsize, com.imallocspy_postgetsize, objidl/IMallocSpy::PostGetSize
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
 - IMallocSpy::PostGetSize
 - objidl/IMallocSpy::PostGetSize
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
 - IMallocSpy.PostGetSize
---

# IMallocSpy::PostGetSize


## -description

Performs operations required after calling <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-getsize">IMalloc::GetSize</a>.

## -parameters

### -param cbActual [in]

The number of bytes in the allocation, as returned by <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-getsize">GetSize</a>.

### -param fSpyed [in]

Indicates whether the block of memory was allocated while the current spy was active.

## -returns

The value returned by <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-getsize">IMalloc::GetSize</a>, which is the size of the allocated block of memory, in bytes.

## -remarks

The size determined by <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-getsize">GetSize</a> is the value returned by the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapsize">HeapSize</a> function. This is the size originally requested. For example, a memory allocation request of 27 bytes returns an allocation of 32 bytes and <b>GetSize</b> returns 27.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-imalloc-getsize">IMalloc::GetSize</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a>



<a href="/windows/desktop/api/objidl/nf-objidl-imallocspy-pregetsize">IMallocSpy::PreGetSize</a>