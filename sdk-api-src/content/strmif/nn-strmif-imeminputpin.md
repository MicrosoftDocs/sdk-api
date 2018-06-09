---
UID: NN:strmif.IMemInputPin
title: IMemInputPin
author: windows-sdk-content
description: The IMemInputPin interface delivers media data to an input pin.
old-location: dshow\imeminputpin.htm
old-project: DirectShow
ms.assetid: a4407c6f-6bb5-4274-920b-8bf7d76268bc
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMemInputPin, IMemInputPin interface [DirectShow], IMemInputPin interface [DirectShow],described, IMemInputPinInterface, dshow.imeminputpin, strmif/IMemInputPin
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
 - IMemInputPin
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMemInputPin interface


## -description



The <code>IMemInputPin</code> interface delivers media data to an input pin. Input pins expose this interface if they use the <a href="https://msdn.microsoft.com/77a161c4-706c-4270-a343-9e16c03cd590">IMemAllocator</a> interface to allocate buffers. When an output pin connects to an input pin, the output pin uses this interface to negotiate allocator requirements and deliver samples to the input pin.

Applications typically do not use this interface.

<b>Filter developers: </b>The <a href="https://msdn.microsoft.com/5a2b7f09-8c8b-45da-a4b7-afeb8d5548c1">CBaseInputPin</a> class implements this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMemInputPin</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMemInputPin</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ab49028e-ae27-4d4e-a5f1-a086ade25c5e">GetAllocator</a>
</td>
<td align="left" width="63%">
Retrieves the memory allocator proposed by this pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61e6ea4f-70cd-43d8-bbb7-76e041ee0eeb">GetAllocatorRequirements</a>
</td>
<td align="left" width="63%">
Retrieves allocator properties that are requested by the input pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dbc9c0ce-3e9c-4402-9d3e-1c7295e94ad9">NotifyAllocator</a>
</td>
<td align="left" width="63%">
Specifies an allocator for the connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7cc1e57a-a18a-4ea4-9669-0be3fb140d40">Receive</a>
</td>
<td align="left" width="63%">
Receives the next media sample in the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc047cad-e250-41f7-856d-26fc077f87a1">ReceiveCanBlock</a>
</td>
<td align="left" width="63%">
Determines whether calls to the <a href="https://msdn.microsoft.com/7cc1e57a-a18a-4ea4-9669-0be3fb140d40">Receive</a> method might block.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf90a6e8-0758-4cee-887d-3ac9f7aa764d">ReceiveMultiple</a>
</td>
<td align="left" width="63%">
Receives multiple samples in the stream.

</td>
</tr>
</table> 

