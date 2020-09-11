---
UID: NN:strmif.IMemAllocator
title: IMemAllocator (strmif.h)
description: The IMemAllocator interface allocates media samples, for moving data between pins.This interface is used by pins that share allocators, when the input pin exposes the IMemInputPin interface.
helpviewer_keywords: ["IMemAllocator","IMemAllocator interface [DirectShow]","IMemAllocator interface [DirectShow]","described","IMemAllocatorInterface","dshow.imemallocator","strmif/IMemAllocator"]
old-location: dshow\imemallocator.htm
tech.root: dshow
ms.assetid: 77a161c4-706c-4270-a343-9e16c03cd590
ms.date: 12/05/2018
ms.keywords: IMemAllocator, IMemAllocator interface [DirectShow], IMemAllocator interface [DirectShow],described, IMemAllocatorInterface, dshow.imemallocator, strmif/IMemAllocator
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMemAllocator
 - strmif/IMemAllocator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMemAllocator
---

# IMemAllocator interface


## -description

The <code>IMemAllocator</code> interface allocates media samples, for moving data between pins.

This interface is used by pins that share allocators, when the input pin exposes the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imeminputpin">IMemInputPin</a> interface. The pins negotiate which pin will provide the allocator. The allocator is used to allocate memory buffers, retrieve empty buffers, and release buffers. Not every filter creates its own allocator, so one allocator might be used by several filters. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/how-filters-connect">How Filters Connect</a>.

Applications typically do not use this interface.

To use an allocator, perform the following steps:

<ol>
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imemallocator-setproperties">IMemAllocator::SetProperties</a> method to specify the buffer requirements, including the number of buffers and the size of each buffer.</li>
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imemallocator-commit">IMemAllocator::Commit</a> method to allocate the buffers.</li>
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imemallocator-getbuffer">IMemAllocator::GetBuffer</a> method to retrieve media samples. This method blocks until the next sample becomes available.</li>
<li>When you are done with each sample, call the <b>IUnknown::Release</b> method on the sample. The sample is not deleted when its reference count reaches zero. Instead, the sample returns to the allocator's free list.</li>
<li>When you are done using the allocator, call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imemallocator-decommit">IMemAllocator::Decommit</a> method to release the memory for the buffers.</li>
</ol>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMemAllocator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMemAllocator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMemAllocator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imemallocator-commit">Commit</a>
</td>
<td align="left" width="63%">
Allocates the buffer memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imemallocator-decommit">Decommit</a>
</td>
<td align="left" width="63%">
Releases the buffer memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imemallocator-getbuffer">GetBuffer</a>
</td>
<td align="left" width="63%">
Retrieves a media sample that contains an empty buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imemallocator-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Retrieves the number of buffers that the allocator will create, and the buffer properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imemallocator-releasebuffer">ReleaseBuffer</a>
</td>
<td align="left" width="63%">
Releases a media sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imemallocator-setproperties">SetProperties</a>
</td>
<td align="left" width="63%">
Specifies the number of buffers to allocate and the size of each buffer.

</td>
</tr>
</table>

