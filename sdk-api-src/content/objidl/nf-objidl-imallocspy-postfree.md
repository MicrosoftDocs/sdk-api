---
UID: NF:objidl.IMallocSpy.PostFree
title: IMallocSpy::PostFree (objidl.h)
description: Performs operations required after calling IMalloc::Free.
helpviewer_keywords: ["IMallocSpy interface [COM]","PostFree method","IMallocSpy.PostFree","IMallocSpy::PostFree","PostFree","PostFree method [COM]","PostFree method [COM]","IMallocSpy interface","_com_imallocspy_postfree","com.imallocspy_postfree","objidl/IMallocSpy::PostFree"]
old-location: com\imallocspy_postfree.htm
tech.root: com
ms.assetid: b46b0b1e-6144-4bb8-84d5-9db5690b7421
ms.date: 12/05/2018
ms.keywords: IMallocSpy interface [COM],PostFree method, IMallocSpy.PostFree, IMallocSpy::PostFree, PostFree, PostFree method [COM], PostFree method [COM],IMallocSpy interface, _com_imallocspy_postfree, com.imallocspy_postfree, objidl/IMallocSpy::PostFree
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
 - IMallocSpy::PostFree
 - objidl/IMallocSpy::PostFree
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
 - IMallocSpy.PostFree
---

# IMallocSpy::PostFree


## -description

Performs operations required after calling <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-free">IMalloc::Free</a>.

## -parameters

### -param fSpyed [in]

Indicates whether the block of memory to be freed was allocated while the current spy was active.

## -remarks

When a spy object implementing <a href="/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a> is registered using <a href="/windows/desktop/api/objbase/nf-objbase-coregistermallocspy">CoRegisterMallocSpy</a> function, COM calls this method immediately after any call to <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-free">IMalloc::Free</a>. This method is included for completeness and consistency; it is not anticipated that developers will implement significant functionality in this method.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-imalloc-free">IMalloc::Free</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a>



<a href="/windows/desktop/api/objidl/nf-objidl-imallocspy-prefree">IMallocSpy::PreFree</a>