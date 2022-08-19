---
UID: NF:objidl.IMalloc.Realloc
title: IMalloc::Realloc (objidl.h)
description: The IMalloc::Realloc method (objidl.h) changes the size of a previously allocated block of memory. 
helpviewer_keywords: ["IMalloc interface [COM]","Realloc method","IMalloc.Realloc","IMalloc::Realloc","Realloc","Realloc method [COM]","Realloc method [COM]","IMalloc interface","_com_imalloc_realloc","com.imalloc_realloc","objidlbase/IMalloc::Realloc"]
old-location: com\imalloc_realloc.htm
tech.root: com
ms.assetid: 37de166a-04a5-4a10-83b3-dd19d0bb48a4
ms.date: 08/12/2022
ms.keywords: IMalloc interface [COM],Realloc method, IMalloc.Realloc, IMalloc::Realloc, Realloc, Realloc method [COM], Realloc method [COM],IMalloc interface, _com_imalloc_realloc, com.imalloc_realloc, objidlbase/IMalloc::Realloc
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
 - IMalloc::Realloc
 - objidl/IMalloc::Realloc
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
 - IMalloc.Realloc
---

# IMalloc::Realloc


## -description

Changes the size of a previously allocated block of memory.

## -parameters

### -param pv [in]

A pointer to the block of memory to be reallocated. This parameter can be <b>NULL</b>, as discussed in the Remarks section below.

### -param cb [in]

The size of the memory block to be reallocated, in bytes. This parameter can be 0, as discussed in the Remarks section below.

## -returns

If the method succeeds, the return value is a pointer to the reallocated block of memory. Otherwise, it is <b>NULL</b>.

## -remarks

This method reallocates a block of memory, but does not guarantee that its contents are initialized. Therefore, the caller is responsible for subsequently initializing the memory. The allocated block may be larger than <i>cb</i> bytes because of the space required for alignment and for maintenance information.

The <i>pv</i> argument points to the beginning of the block. If <i>pv</i> is <b>NULL</b>, <b>Realloc</b> allocates a new memory block in the same way that <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-alloc">IMalloc::Alloc</a> does. If <i>pv</i> is not <b>NULL</b>, it should be a pointer returned by a prior call to <b>Alloc</b>.

The <i>cb</i> argument specifies the size of the new block, in bytes. The contents of the block are unchanged up to the shorter of the new and old sizes, although the new block can be in a different location. Because the new block can be in a different memory location, the pointer returned by <b>Realloc</b> is not guaranteed to be the pointer passed through the <i>pv</i> argument. If <i>pv</i> is not <b>NULL</b> and <i>cb</i> is zero, the memory pointed to by <i>pv</i> is freed.

<b>Realloc</b> returns a void pointer to the reallocated (and possibly moved) block of memory. The return value is <b>NULL</b> if the size is zero and the buffer argument is not <b>NULL</b>, or if there is not enough memory available to expand the block to the specified size. In the first case, the original block is freed; in the second, the original block is unchanged.

The storage space pointed to by the return value is guaranteed to be suitably aligned for storage of any type of object. To get a pointer to a type other than <b>void</b>, use a type cast on the return value.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a>
