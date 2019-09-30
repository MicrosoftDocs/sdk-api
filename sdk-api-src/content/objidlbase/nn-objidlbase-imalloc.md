---
UID: NN:objidlbase.IMalloc
title: IMalloc (objidlbase.h)
author: windows-sdk-content
description: Allocates, frees, and manages memory.
old-location: com\imalloc.htm
tech.root: com
ms.assetid: 047f281e-2665-4d6d-9a0b-918cd3339447
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMalloc, IMalloc interface [COM], IMalloc interface [COM],described, _com_imalloc, com.imalloc, objidlbase/IMalloc
ms.topic: interface
f1_keywords: 
 - "objidlbase/IMalloc"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IMalloc
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMalloc interface


## -description


Allocates, frees, and manages memory.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMalloc</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMalloc</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMalloc</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imalloc-alloc">Alloc</a>
</td>
<td align="left" width="63%">
Allocates a block of memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imalloc-didalloc">DidAlloc</a>
</td>
<td align="left" width="63%">
Determines whether this allocator was used to allocate the specified block of memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imalloc-free">Free</a>
</td>
<td align="left" width="63%">
Frees a previously allocated block of memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imalloc-getsize">GetSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of a previously allocated block of memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imalloc-heapminimize">HeapMinimize</a>
</td>
<td align="left" width="63%">
Minimizes the heap as much as possible by releasing unused memory to the operating system, coalescing adjacent free blocks, and committing free pages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imalloc-realloc">Realloc</a>
</td>
<td align="left" width="63%">
Changes the size of a previously allocated block of memory.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc">CoGetMalloc</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-coregistermallocspy">CoRegisterMallocSpy</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-corevokemallocspy">CoRevokeMallocSpy</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a>
 

 

