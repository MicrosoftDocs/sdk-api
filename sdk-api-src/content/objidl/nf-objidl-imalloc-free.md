---
UID: NF:objidl.IMalloc.Free
title: IMalloc::Free (objidl.h)
description: Frees a previously allocated block of memory.
old-location: com\imalloc_free.htm
tech.root: com
ms.assetid: d65411ea-13d5-4932-a757-d897311e9e28
ms.date: 12/05/2018
ms.keywords: Free, Free method [COM], Free method [COM],IMalloc interface, IMalloc interface [COM],Free method, IMalloc.Free, IMalloc::Free, _com_imalloc_free, com.imalloc_free, objidlbase/IMalloc::Free
ms.topic: method
f1_keywords:
- objidl/IMalloc.Free
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- objidlbase.h
api_name:
- IMalloc.Free
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMalloc::Free


## -description


Frees a previously allocated block of memory.


## -parameters




### -param pv [in]

A pointer to the memory block to be freed. If this parameter is <b>NULL</b>, this method has no effect.


## -returns



This method does not return a value.




## -remarks



This method frees a block of memory previously allocated through a call to <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imalloc-alloc">IMalloc::Alloc</a> or <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imalloc-realloc">IMalloc::Realloc</a>. The number of bytes freed equals the number of bytes that were allocated. After the call, the block of memory pointed to by <i>pv</i> is invalid and can no longer be used.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a>
 

 

