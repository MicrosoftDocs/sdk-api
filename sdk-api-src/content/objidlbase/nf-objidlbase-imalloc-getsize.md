---
UID: NF:objidlbase.IMalloc.GetSize
title: IMalloc::GetSize (objidlbase.h)
description: The IMalloc::GetSize (objidlbase.h) method retrieves the size of a previously allocated block of memory.
helpviewer_keywords: ["GetSize","GetSize method [COM]","GetSize method [COM]","IMalloc interface","IMalloc interface [COM]","GetSize method","IMalloc.GetSize","IMalloc::GetSize","_com_imalloc_getsize","com.imalloc_getsize","objidlbase/IMalloc::GetSize"]
old-location: com\imalloc_getsize.htm
tech.root: com
ms.assetid: abf8cb53-7c1b-4dde-9745-30a45ad030b7
ms.date: 08/13/2022
ms.keywords: GetSize, GetSize method [COM], GetSize method [COM],IMalloc interface, IMalloc interface [COM],GetSize method, IMalloc.GetSize, IMalloc::GetSize, _com_imalloc_getsize, com.imalloc_getsize, objidlbase/IMalloc::GetSize
req.header: objidlbase.h
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
 - IMalloc::GetSize
 - objidlbase/IMalloc::GetSize
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
 - IMalloc.GetSize
---

# IMalloc::GetSize


## -description

Retrieves the size of a previously allocated block of memory.

## -parameters

### -param pv [in]

A pointer to the block of memory.

## -returns

The size of the allocated memory block in bytes or, if <i>pv</i> is a <b>NULL</b> pointer, -1.

## -remarks

To get the size in bytes of a memory block, the block must have been previously allocated with <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-alloc">IMalloc::Alloc</a> or <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-realloc">IMalloc::Realloc</a>. The size returned is the actual size of the allocation, which may be greater than the size requested when the allocation was made.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a>
