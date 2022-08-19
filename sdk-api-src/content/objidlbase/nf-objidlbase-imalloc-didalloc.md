---
UID: NF:objidlbase.IMalloc.DidAlloc
title: IMalloc::DidAlloc (objidlbase.h)
description: The IMalloc::DidAlloc (objidlbase.h) method determines whether this allocator was used to allocate the specified block of memory.
helpviewer_keywords: ["DidAlloc","DidAlloc method [COM]","DidAlloc method [COM]","IMalloc interface","IMalloc interface [COM]","DidAlloc method","IMalloc.DidAlloc","IMalloc::DidAlloc","_com_imalloc_didalloc","com.imalloc_didalloc","objidlbase/IMalloc::DidAlloc"]
old-location: com\imalloc_didalloc.htm
tech.root: com
ms.assetid: 085dd7cd-c360-48fa-8713-64dd9057e20d
ms.date: 08/13/2022
ms.keywords: DidAlloc, DidAlloc method [COM], DidAlloc method [COM],IMalloc interface, IMalloc interface [COM],DidAlloc method, IMalloc.DidAlloc, IMalloc::DidAlloc, _com_imalloc_didalloc, com.imalloc_didalloc, objidlbase/IMalloc::DidAlloc
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
 - IMalloc::DidAlloc
 - objidlbase/IMalloc::DidAlloc
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
 - IMalloc.DidAlloc
---

# IMalloc::DidAlloc


## -description

Determines whether this allocator was used to allocate the specified block of memory.

## -parameters

### -param pv [in]

A pointer to the block of memory. If this parameter is a <b>NULL</b> pointer, -1 is returned.

## -returns

This method can return the following values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The block of memory was allocated by this allocator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The block of memory was not allocated by this allocator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
This method cannot determine whether this allocator allocated the block of memory.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a>
