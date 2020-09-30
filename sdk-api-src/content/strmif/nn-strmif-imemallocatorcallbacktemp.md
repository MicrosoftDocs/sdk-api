---
UID: NN:strmif.IMemAllocatorCallbackTemp
title: IMemAllocatorCallbackTemp (strmif.h)
description: The IMemAllocatorCallbackTemp interface enables a filter to receive a callback notification from an allocator whenever a sample is returned to the allocator's free list.The use of this interface is deprecated.
helpviewer_keywords: ["IMemAllocatorCallbackTemp","IMemAllocatorCallbackTemp interface [DirectShow]","IMemAllocatorCallbackTemp interface [DirectShow]","described","IMemAllocatorCallbackTempInterface","dshow.imemallocatorcallbacktemp","strmif/IMemAllocatorCallbackTemp"]
old-location: dshow\imemallocatorcallbacktemp.htm
tech.root: dshow
ms.assetid: 6213faaa-86ff-46e7-80da-a043cae40805
ms.date: 12/05/2018
ms.keywords: IMemAllocatorCallbackTemp, IMemAllocatorCallbackTemp interface [DirectShow], IMemAllocatorCallbackTemp interface [DirectShow],described, IMemAllocatorCallbackTempInterface, dshow.imemallocatorcallbacktemp, strmif/IMemAllocatorCallbackTemp
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
 - IMemAllocatorCallbackTemp
 - strmif/IMemAllocatorCallbackTemp
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
 - IMemAllocatorCallbackTemp
---

# IMemAllocatorCallbackTemp interface


## -description

The <code>IMemAllocatorCallbackTemp</code> interface enables a filter to receive a callback notification from an allocator whenever a sample is returned to the allocator's free list.

The use of this interface is deprecated.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMemAllocatorCallbackTemp</b> interface inherits from <a href="/windows/desktop/api/strmif/nn-strmif-imemallocator">IMemAllocator</a>. <b>IMemAllocatorCallbackTemp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMemAllocatorCallbackTemp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount">GetFreeCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of free media samples.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/strmif/nf-strmif-imemallocatorcallbacktemp-setnotify">SetNotify</a>
</td>
<td align="left" width="63%">
Sets or removes a callback on the allocator.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-imemallocator">IMemAllocator</a>