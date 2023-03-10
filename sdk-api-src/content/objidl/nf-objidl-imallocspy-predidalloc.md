---
UID: NF:objidl.IMallocSpy.PreDidAlloc
title: IMallocSpy::PreDidAlloc (objidl.h)
description: Performs operations required before calling IMalloc::DidAlloc.
helpviewer_keywords: ["IMallocSpy interface [COM]","PreDidAlloc method","IMallocSpy.PreDidAlloc","IMallocSpy::PreDidAlloc","PreDidAlloc","PreDidAlloc method [COM]","PreDidAlloc method [COM]","IMallocSpy interface","_com_imallocspy_predidalloc","com.imallocspy_predidalloc","objidl/IMallocSpy::PreDidAlloc"]
old-location: com\imallocspy_predidalloc.htm
tech.root: com
ms.assetid: f18b6dba-c0fe-40c2-835b-01dff521d27c
ms.date: 12/05/2018
ms.keywords: IMallocSpy interface [COM],PreDidAlloc method, IMallocSpy.PreDidAlloc, IMallocSpy::PreDidAlloc, PreDidAlloc, PreDidAlloc method [COM], PreDidAlloc method [COM],IMallocSpy interface, _com_imallocspy_predidalloc, com.imallocspy_predidalloc, objidl/IMallocSpy::PreDidAlloc
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
 - IMallocSpy::PreDidAlloc
 - objidl/IMallocSpy::PreDidAlloc
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
 - IMallocSpy.PreDidAlloc
---

# IMallocSpy::PreDidAlloc


## -description

Performs operations required before calling <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-didalloc">IMalloc::DidAlloc</a>.

## -parameters

### -param pRequest [in]

The pointer specified in the call to <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-didalloc">DidAlloc</a>.

### -param fSpyed [in]

Indicates whether the allocation was done while this spy was active.

## -returns

The value passed  to <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-didalloc">DidAlloc</a> as the <i>fActual</i> parameter.

## -remarks

When a spy object implementing <a href="/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a> is registered with the <a href="/windows/desktop/api/objbase/nf-objbase-coregistermallocspy">CoRegisterMallocSpy</a> function, COM calls this method immediately before any call to <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-didalloc">IMalloc::DidAlloc</a>. This method is included for completeness and consistency; it is not anticipated that developers will implement significant functionality in this method.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-imalloc-didalloc">IMalloc::DidAlloc</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a>



<a href="/windows/desktop/api/objidl/nf-objidl-imallocspy-postdidalloc">IMallocSpy::PostDidAlloc</a>