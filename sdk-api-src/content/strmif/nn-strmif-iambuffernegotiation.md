---
UID: NN:strmif.IAMBufferNegotiation
title: IAMBufferNegotiation (strmif.h)
description: The IAMBufferNegotiation interface requests the number of buffers for a filter to create and size of each buffer.
helpviewer_keywords: ["IAMBufferNegotiation","IAMBufferNegotiation interface [DirectShow]","IAMBufferNegotiation interface [DirectShow]","described","IAMBufferNegotiationInterface","dshow.iambuffernegotiation","strmif/IAMBufferNegotiation"]
old-location: dshow\iambuffernegotiation.htm
tech.root: dshow
ms.assetid: 68e98afd-3275-49bb-b165-48ed40026e76
ms.date: 12/05/2018
ms.keywords: IAMBufferNegotiation, IAMBufferNegotiation interface [DirectShow], IAMBufferNegotiation interface [DirectShow],described, IAMBufferNegotiationInterface, dshow.iambuffernegotiation, strmif/IAMBufferNegotiation
f1_keywords:
- strmif/IAMBufferNegotiation
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IAMBufferNegotiation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMBufferNegotiation interface


## -description



The <code>IAMBufferNegotiation</code> interface requests the number of buffers for a filter to create and size of each buffer. This interface can be exposed by any pin that connects using the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imeminputpin">IMemInputPin</a> pin interface, but is typically exposed on the output pins of capture filters.

When two pins connect through <b>IMemInputPin</b>, they agree on an allocator object that is responsible for creating buffers. Normally this process is transparent to the application, but in some situations the application needs more control. If a pin exposes <code>IAMBufferNegotiation</code>, the application can suggest how many buffers to create, the size of the buffers, and other properties. If your application performs preview of captured audio, you can specify a smaller buffer size to reduce latency. Teleconferencing applications should specify a minimal number of buffers.

To use this interface, call the <b>SuggestAllocatorProperties</b> method before the pins connect. After the pins connect, call the <b>GetAllocatorProperties</b> method to determine whether the pin honored the request.

<b>Filter developers</b>: Capture filters should always support this interface when possible.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMBufferNegotiation</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMBufferNegotiation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMBufferNegotiation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iambuffernegotiation-getallocatorproperties">GetAllocatorProperties</a>
</td>
<td align="left" width="63%">
Retrieves the allocator properties that the pin is using.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iambuffernegotiation-suggestallocatorproperties">SuggestAllocatorProperties</a>
</td>
<td align="left" width="63%">
Informs the pin of the application's preferred allocator properties

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/interfaces">Interfaces</a>
 

 

