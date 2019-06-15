---
UID: NN:strmif.IMemInputPin
title: IMemInputPin (strmif.h)
author: windows-sdk-content
description: The IMemInputPin interface delivers media data to an input pin.
old-location: dshow\imeminputpin.htm
tech.root: DirectShow
ms.assetid: a4407c6f-6bb5-4274-920b-8bf7d76268bc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMemInputPin, IMemInputPin interface [DirectShow], IMemInputPin interface [DirectShow],described, IMemInputPinInterface, dshow.imeminputpin, strmif/IMemInputPin
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
 - IMemInputPin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMemInputPin interface


## -description



The <code>IMemInputPin</code> interface delivers media data to an input pin. Input pins expose this interface if they use the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imemallocator">IMemAllocator</a> interface to allocate buffers. When an output pin connects to an input pin, the output pin uses this interface to negotiate allocator requirements and deliver samples to the input pin.

Applications typically do not use this interface.

<b>Filter developers: </b>The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/cbaseinputpin">CBaseInputPin</a> class implements this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMemInputPin</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMemInputPin</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMemInputPin</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imeminputpin-getallocator">GetAllocator</a>
</td>
<td align="left" width="63%">
Retrieves the memory allocator proposed by this pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imeminputpin-getallocatorrequirements">GetAllocatorRequirements</a>
</td>
<td align="left" width="63%">
Retrieves allocator properties that are requested by the input pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imeminputpin-notifyallocator">NotifyAllocator</a>
</td>
<td align="left" width="63%">
Specifies an allocator for the connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imeminputpin-receive">Receive</a>
</td>
<td align="left" width="63%">
Receives the next media sample in the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imeminputpin-receivecanblock">ReceiveCanBlock</a>
</td>
<td align="left" width="63%">
Determines whether calls to the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imeminputpin-receive">Receive</a> method might block.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imeminputpin-receivemultiple">ReceiveMultiple</a>
</td>
<td align="left" width="63%">
Receives multiple samples in the stream.

</td>
</tr>
</table> 

