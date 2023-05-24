---
UID: NF:objidl.IMalloc.Free
title: IMalloc::Free (objidl.h)
description: The IMalloc::Free method (objidl.h) frees a previously allocated block of memory.
helpviewer_keywords: ["Free","Free method [COM]","Free method [COM]","IMalloc interface","IMalloc interface [COM]","Free method","IMalloc.Free","IMalloc::Free","_com_imalloc_free","com.imalloc_free","objidlbase/IMalloc::Free"]
old-location: com\imalloc_free.htm
tech.root: com
ms.assetid: d65411ea-13d5-4932-a757-d897311e9e28
ms.date: 08/12/2022
ms.keywords: Free, Free method [COM], Free method [COM],IMalloc interface, IMalloc interface [COM],Free method, IMalloc.Free, IMalloc::Free, _com_imalloc_free, com.imalloc_free, objidlbase/IMalloc::Free
req.header: objidl.h
req.include-header: ObjIdl.h
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
 - IMalloc::Free
 - objidl/IMalloc::Free
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IMalloc.Free
---

# IMalloc::Free


## -description

Frees a previously allocated block of memory.

## -parameters

### -param pv [in]

A pointer to the memory block to be freed. If this parameter is <b>NULL</b>, this method has no effect.

## -remarks

This method frees a block of memory previously allocated through a call to <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-alloc">IMalloc::Alloc</a> or <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-realloc">IMalloc::Realloc</a>. The number of bytes freed equals the number of bytes that were allocated. After the call, the block of memory pointed to by <i>pv</i> is invalid and can no longer be used.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a>
