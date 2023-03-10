---
UID: NF:objidl.IMalloc.Alloc
title: IMalloc::Alloc (objidl.h)
description: Allocates a block of memory. (IMalloc.Alloc)
helpviewer_keywords: ["Alloc","Alloc method [COM]","Alloc method [COM]","IMalloc interface","IMalloc interface [COM]","Alloc method","IMalloc.Alloc","IMalloc::Alloc","_com_imalloc_alloc","com.imalloc_alloc","objidl/IMalloc::Alloc"]
old-location: com\imalloc_alloc.htm
tech.root: com
ms.assetid: c9c9bdac-965f-4b18-9338-28a025930480
ms.date: 12/05/2018
ms.keywords: Alloc, Alloc method [COM], Alloc method [COM],IMalloc interface, IMalloc interface [COM],Alloc method, IMalloc.Alloc, IMalloc::Alloc, _com_imalloc_alloc, com.imalloc_alloc, objidl/IMalloc::Alloc
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
 - IMalloc::Alloc
 - objidl/IMalloc::Alloc
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
 - IMalloc.Alloc
---

# IMalloc::Alloc


## -description

Allocates a block of memory.

## -parameters

### -param cb [in]

The size of the memory block to be allocated, in bytes.

## -returns

If the method succeeds, the return value is a pointer to the allocated block of memory. Otherwise, it is <b>NULL</b>.

Applications should always check the return value from this method, even when requesting small amounts of memory, because there is no guarantee the memory will be allocated.

## -remarks

The initial contents of the returned memory block are undefined and there is no guarantee that the block has been initialized, so you should initialize it in your code. The allocated block may be larger than <i>cb</i> bytes because of the space required for alignment and for maintenance information.

If <i>cb</i> is zero, <b>Alloc</b> allocates a zero-length item and returns a valid pointer to that item. If there is insufficient memory available, <b>Alloc</b> returns <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a>
