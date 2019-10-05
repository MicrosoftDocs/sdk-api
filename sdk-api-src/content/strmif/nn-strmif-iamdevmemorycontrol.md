---
UID: NN:strmif.IAMDevMemoryControl
title: IAMDevMemoryControl (strmif.h)
author: windows-sdk-content
description: Note  This interface is no longer supported by the AVI Splitter. Note  It was defined to support certain older hardware decoders that required AVI files to be read directly into hardware memory.
old-location: dshow\iamdevmemorycontrol.htm
tech.root: DirectShow
ms.assetid: 9945bffb-6748-4c7d-ba14-91470cf6c651
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMDevMemoryControl, IAMDevMemoryControl interface [DirectShow], IAMDevMemoryControl interface [DirectShow],described, IAMDevMemoryControlInterface, dshow.iamdevmemorycontrol, strmif/IAMDevMemoryControl
ms.topic: interface
f1_keywords: 
 - "strmif/IAMDevMemoryControl"
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
 - IAMDevMemoryControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMDevMemoryControl interface


## -description



<div class="alert"><b>Note</b>  This interface is no longer supported by the AVI Splitter.</div>
<div> </div>
<div class="alert"><b>Note</b>  It was defined to support certain older hardware decoders that required AVI files to be read directly into hardware memory. The interface enables the AVI parser to allocate memory from the downstream filter but still provide its own allocator. There should be no need for any newer devices to support this interface.</div>
<div> </div>
A device memory control object supports <code>IAMDevMemoryControl</code>. This object is aggregated with an <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imemallocator">IMemAllocator</a> object that is used in the connection. Typically, filters will call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamdevmemoryallocator-getdevmemoryobject">IAMDevMemoryAllocator::GetDevMemoryObject</a> method to obtain a pointer to this interface.

Implement this interface with the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamdevmemoryallocator">IAMDevMemoryAllocator</a> interface when pins need to have greater control of memory allocation.

Use this interface to synchronize the completion of writing data to a memory allocator, and to get the device ID of the on-board memory allocator.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMDevMemoryControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMDevMemoryControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMDevMemoryControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamdevmemorycontrol-getdevid">GetDevId</a>
</td>
<td align="left" width="63%">
Retrieves the device ID of the on-board memory allocator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamdevmemorycontrol-querywritesync">QueryWriteSync</a>
</td>
<td align="left" width="63%">
Checks if the memory supported by the allocator requires the use of the <b>WriteSync</b> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamdevmemorycontrol-writesync">WriteSync</a>
</td>
<td align="left" width="63%">
Used to synchronize with the completed write operation by returning when any data being written to the specified allocator region is fully written into the memory.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>
 

 

