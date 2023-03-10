---
UID: NF:objidl.IMallocSpy.PostDidAlloc
title: IMallocSpy::PostDidAlloc (objidl.h)
description: Performs operations required after calling IMalloc::DidAlloc.
helpviewer_keywords: ["IMallocSpy interface [COM]","PostDidAlloc method","IMallocSpy.PostDidAlloc","IMallocSpy::PostDidAlloc","PostDidAlloc","PostDidAlloc method [COM]","PostDidAlloc method [COM]","IMallocSpy interface","_com_imallocspy_postdidalloc","com.imallocspy_postdidalloc","objidl/IMallocSpy::PostDidAlloc"]
old-location: com\imallocspy_postdidalloc.htm
tech.root: com
ms.assetid: 820ff316-9edd-4894-8461-fc532d439348
ms.date: 12/05/2018
ms.keywords: IMallocSpy interface [COM],PostDidAlloc method, IMallocSpy.PostDidAlloc, IMallocSpy::PostDidAlloc, PostDidAlloc, PostDidAlloc method [COM], PostDidAlloc method [COM],IMallocSpy interface, _com_imallocspy_postdidalloc, com.imallocspy_postdidalloc, objidl/IMallocSpy::PostDidAlloc
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
 - IMallocSpy::PostDidAlloc
 - objidl/IMallocSpy::PostDidAlloc
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
 - IMallocSpy.PostDidAlloc
---

# IMallocSpy::PostDidAlloc


## -description

Performs operations required after calling <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-didalloc">IMalloc::DidAlloc</a>.

## -parameters

### -param pRequest [in]

The pointer specified in the call to <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-didalloc">DidAlloc</a>.

### -param fSpyed [in]

Indicates whether the allocation was done while this spy was active.

### -param fActual [in]

The value returned by <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-didalloc">DidAlloc</a>.

## -returns

The value returned to the caller of <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-didalloc">DidAlloc</a>.

## -remarks

When a spy object implementing <a href="/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a> is registered using the <a href="/windows/desktop/api/objbase/nf-objbase-coregistermallocspy">CoRegisterMallocSpy</a> function, COM calls this method immediately after any call to <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-didalloc">DidAlloc</a>. This method is included for completeness and consistency; it is not anticipated that developers will implement significant functionality in this method.

For convenience, <i>pRequest</i>, the original pointer passed in the call to <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-didalloc">DidAlloc</a>, is passed to <b>PostDidAlloc</b>. In addition, the parameter <i>fActual</i> is a Boolean value that indicates whether this value was actually passed to <b>DidAlloc</b>. If not, it would indicate that <a href="/windows/desktop/api/objidl/nf-objidl-imallocspy-predidalloc">IMallocSpy::PreDidAlloc</a> was implemented to alter this pointer for some debugging purpose.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-imalloc-didalloc">IMalloc::DidAlloc</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a>



<a href="/windows/desktop/api/objidl/nf-objidl-imallocspy-predidalloc">IMallocSpy::PreDidAlloc</a>