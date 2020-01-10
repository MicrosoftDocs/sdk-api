---
UID: NN:strmif.IAMDevMemoryAllocator
title: IAMDevMemoryAllocator (strmif.h)
description: Note  This interface is no longer supported by the AVI Splitter. Note  This interface was defined to support older hardware decoders that required AVI files to be read into directly hardware memory.
old-location: dshow\iamdevmemoryallocator.htm
tech.root: DirectShow
ms.assetid: bab1e582-928a-408b-a9c5-8e9827e9928b
ms.date: 12/05/2018
ms.keywords: IAMDevMemoryAllocator, IAMDevMemoryAllocator interface [DirectShow], IAMDevMemoryAllocator interface [DirectShow],described, IAMDevMemoryAllocatorInterface, dshow.iamdevmemoryallocator, strmif/IAMDevMemoryAllocator
f1_keywords:
- strmif/IAMDevMemoryAllocator
dev_langs:
- c++
req.header: strmif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
- strmif.h
api_name:
- IAMDevMemoryAllocator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMDevMemoryAllocator interface


## -description



<div class="alert"><b>Note</b>  This interface is no longer supported by the AVI Splitter.</div>
<div> </div>
<div class="alert"><b>Note</b>  This interface was defined to support older hardware decoders that required AVI files to be read into directly hardware memory. The interface enables the AVI parser to allocate memory from the downstream filter but still provide its own allocator.</div>
<div> </div>
Implement this interface when your pin must support the creation of on-board memory allocators. Source filters that are aware of on-board memory and need to create their own allocators should query for this interface, request an amount of memory and then create an allocator (aggregating the device memory control object). Source filters that don't need to create their own allocator could just use the allocator of the downstream pin (which also aggregates the device memory control object). The hardware-based filter can confirm the usage of its on-board memory by calling methods on the aggregated allocator.

Use this interface when applications need to control the memory of codecs with on-board memory.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMDevMemoryAllocator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMDevMemoryAllocator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMDevMemoryAllocator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamdevmemoryallocator-alloc">Alloc</a>
</td>
<td align="left" width="63%">
Allocates a memory buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamdevmemoryallocator-checkmemory">CheckMemory</a>
</td>
<td align="left" width="63%">
Tests whether the particular device of the allocator allocated a memory pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamdevmemoryallocator-free">Free</a>
</td>
<td align="left" width="63%">
Frees the previously allocated memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamdevmemoryallocator-getdevmemoryobject">GetDevMemoryObject</a>
</td>
<td align="left" width="63%">
Retrieves an <b>IUnknown</b> interface pointer to a device memory control object that can be aggregated with a custom allocator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamdevmemoryallocator-getinfo">GetInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about the memory capabilities.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>
 

 

