---
UID: NF:objidl.IMallocSpy.PreRealloc
title: IMallocSpy::PreRealloc (objidl.h)
description: Performs operations required before calling IMalloc::Realloc.
helpviewer_keywords: ["IMallocSpy interface [COM]","PreRealloc method","IMallocSpy.PreRealloc","IMallocSpy::PreRealloc","PreRealloc","PreRealloc method [COM]","PreRealloc method [COM]","IMallocSpy interface","_com_imallocspy_prerealloc","com.imallocspy_prerealloc","objidl/IMallocSpy::PreRealloc"]
old-location: com\imallocspy_prerealloc.htm
tech.root: com
ms.assetid: dd4db69c-3369-4aca-bc05-4c3c6850cc09
ms.date: 12/05/2018
ms.keywords: IMallocSpy interface [COM],PreRealloc method, IMallocSpy.PreRealloc, IMallocSpy::PreRealloc, PreRealloc, PreRealloc method [COM], PreRealloc method [COM],IMallocSpy interface, _com_imallocspy_prerealloc, com.imallocspy_prerealloc, objidl/IMallocSpy::PreRealloc
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
 - IMallocSpy::PreRealloc
 - objidl/IMallocSpy::PreRealloc
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
 - IMallocSpy.PreRealloc
---

# IMallocSpy::PreRealloc


## -description

Performs operations required before calling <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-realloc">IMalloc::Realloc</a>.

## -parameters

### -param pRequest [in]

The pointer to the block of memory specified in the call to <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-realloc">IMalloc::Realloc</a>.

### -param cbRequest [in]

The byte count of the block of memory as specified in the original call to <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-realloc">IMalloc::Realloc</a>.

### -param ppNewRequest [out]

Address of pointer variable that receives a pointer to the memory block to be reallocated. This may be different from the pointer in <i>pRequest</i> if the implementation of <b>PreRealloc</b> extends or modifies the reallocation. This is pointer should always be stored by <b>PreRealloc</b>.

### -param fSpyed [in]

Indicates whether the block of memory was allocated while this spy was active.

## -returns

The byte count to be passed to <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-realloc">IMalloc::Realloc</a>.

## -remarks

The <b>PreRealloc</b> implementation may extend and/or modify the allocation to store debug-specific information with the allocation. Thus, the <i>ppNewRequest</i> parameter may differ from <i>pRequest</i>, a pointer to the request specified in the original call to <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-realloc">Realloc</a>.

<b>PreRealloc</b> can force memory allocation failure by returning 0, allowing testing to ensure that the application handles allocation failure gracefully in all cases. In this case, <a href="/windows/desktop/api/objidl/nf-objidl-imallocspy-postrealloc">PostRealloc</a> is not called and <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-realloc">Realloc</a> returns <b>NULL</b>. However, if <b>Realloc</b> encounters a real memory failure and returns <b>NULL</b>, <b>PostRealloc</b> is called. Forcing allocation failure is effective only if <i>cbRequest</i> is not equal to 0.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-imalloc-realloc">IMalloc::Realloc</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a>



<a href="/windows/desktop/api/objidl/nf-objidl-imallocspy-postrealloc">IMallocSpy::PostRealloc</a>