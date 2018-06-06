---
UID: NN:strmif.IAMDevMemoryAllocator
title: IAMDevMemoryAllocator
author: windows-sdk-content
description: Note  This interface is no longer supported by the AVI Splitter. Note  This interface was defined to support older hardware decoders that required AVI files to be read into directly hardware memory.
old-location: dshow\iamdevmemoryallocator.htm
old-project: DirectShow
ms.assetid: bab1e582-928a-408b-a9c5-8e9827e9928b
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IAMDevMemoryAllocator, IAMDevMemoryAllocator interface [DirectShow], IAMDevMemoryAllocator interface [DirectShow],described, IAMDevMemoryAllocatorInterface, dshow.iamdevmemoryallocator, strmif/IAMDevMemoryAllocator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmif.h
api_name:
 - IAMDevMemoryAllocator
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMDevMemoryAllocator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMDevMemoryAllocator</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/de5f7755-fd96-4016-9cab-b98721080e14">Alloc</a>
</td>
<td align="left" width="63%">
Allocates a memory buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d51be809-4a97-4098-9ef3-8ed6603f26c0">CheckMemory</a>
</td>
<td align="left" width="63%">
Tests whether the particular device of the allocator allocated a memory pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d86d3016-bca0-4a0b-946b-f50c49266c67">Free</a>
</td>
<td align="left" width="63%">
Frees the previously allocated memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7ca361a-1ce6-449f-9d81-fbfe39f0f9f0">GetDevMemoryObject</a>
</td>
<td align="left" width="63%">
Retrieves an <b>IUnknown</b> interface pointer to a device memory control object that can be aggregated with a custom allocator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451309">GetInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about the memory capabilities.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5b798477-9b36-4f59-b9cc-2938b5e4009f">Deprecated Interfaces</a>
 

 

