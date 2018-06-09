---
UID: NN:strmif.IMemAllocator
title: IMemAllocator
author: windows-sdk-content
description: The IMemAllocator interface allocates media samples, for moving data between pins.This interface is used by pins that share allocators, when the input pin exposes the IMemInputPin interface.
old-location: dshow\imemallocator.htm
old-project: DirectShow
ms.assetid: 77a161c4-706c-4270-a343-9e16c03cd590
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMemAllocator, IMemAllocator interface [DirectShow], IMemAllocator interface [DirectShow],described, IMemAllocatorInterface, dshow.imemallocator, strmif/IMemAllocator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
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
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMemAllocator interface


## -description



The <code>IMemAllocator</code> interface allocates media samples, for moving data between pins.

This interface is used by pins that share allocators, when the input pin exposes the <a href="https://msdn.microsoft.com/a4407c6f-6bb5-4274-920b-8bf7d76268bc">IMemInputPin</a> interface. The pins negotiate which pin will provide the allocator. The allocator is used to allocate memory buffers, retrieve empty buffers, and release buffers. Not every filter creates its own allocator, so one allocator might be used by several filters. For more information, see <a href="https://msdn.microsoft.com/6a126dd5-00fa-4ea6-b00a-09b7e1246874">How Filters Connect</a>.

Applications typically do not use this interface.

To use an allocator, perform the following steps:

<ol>
<li>Call the <a href="https://msdn.microsoft.com/c68f2e2f-c70f-447d-804b-dfdfe8ae8a52">IMemAllocator::SetProperties</a> method to specify the buffer requirements, including the number of buffers and the size of each buffer.</li>
<li>Call the <a href="https://msdn.microsoft.com/34db4c1f-5642-4495-a572-9a78b1ee7b7e">IMemAllocator::Commit</a> method to allocate the buffers.</li>
<li>Call the <a href="https://msdn.microsoft.com/a5d015c8-ef15-4bac-906f-5d064fbff11f">IMemAllocator::GetBuffer</a> method to retrieve media samples. This method blocks until the next sample becomes available.</li>
<li>When you are done with each sample, call the <b>IUnknown::Release</b> method on the sample. The sample is not deleted when its reference count reaches zero. Instead, the sample returns to the allocator's free list.</li>
<li>When you are done using the allocator, call the <a href="https://msdn.microsoft.com/2c1211c1-e047-4240-b85a-9be0a9290d31">IMemAllocator::Decommit</a> method to release the memory for the buffers.</li>
</ol>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMemAllocator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMemAllocator</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439717">Commit</a>
</td>
<td align="left" width="63%">
Allocates the buffer memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c1211c1-e047-4240-b85a-9be0a9290d31">Decommit</a>
</td>
<td align="left" width="63%">
Releases the buffer memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983413">GetBuffer</a>
</td>
<td align="left" width="63%">
Retrieves a media sample that contains an empty buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991811">GetProperties</a>
</td>
<td align="left" width="63%">
Retrieves the number of buffers that the allocator will create, and the buffer properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96e02a28-af92-41a7-8251-c4ab15190651">ReleaseBuffer</a>
</td>
<td align="left" width="63%">
Releases a media sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991815">SetProperties</a>
</td>
<td align="left" width="63%">
Specifies the number of buffers to allocate and the size of each buffer.

</td>
</tr>
</table> 

