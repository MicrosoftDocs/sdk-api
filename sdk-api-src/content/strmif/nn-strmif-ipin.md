---
UID: NN:strmif.IPin
title: IPin (strmif.h)
description: This interface is exposed by all input and output pins.The filter graph manager uses this interface to connect pins and perform flushing operations.
helpviewer_keywords: ["IPin","IPin interface [DirectShow]","IPin interface [DirectShow]","described","IPinInterface","dshow.ipin","strmif/IPin"]
old-location: dshow\ipin.htm
tech.root: DirectShow
ms.assetid: ad0ead4e-9f8e-4935-b220-306d665e50f4
ms.date: 12/05/2018
ms.keywords: IPin, IPin interface [DirectShow], IPin interface [DirectShow],described, IPinInterface, dshow.ipin, strmif/IPin
f1_keywords:
- strmif/IPin
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
- IPin
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPin interface


## -description



This interface is exposed by all input and output pins.

The filter graph manager uses this interface to connect pins and perform flushing operations. Applications can use this interface to query the pin for information. Applications should never call <code>IPin</code> methods that change a pin's state, such as <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-connect">Connect</a>, <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-disconnect">Disconnect</a>, <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-beginflush">BeginFlush</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-endflush">EndFlush</a>. To connect pins, an application must use the methods in <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a>.

<b>Filter developers: </b>The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/cbasepin">CBasePin</a>, <a href="https://docs.microsoft.com/windows/desktop/DirectShow/cbaseinputpin">CBaseInputPin</a>, and <a href="https://docs.microsoft.com/windows/desktop/DirectShow/cbaseoutputpin">CBaseOutputPin</a> classes implement this interface. Other base classes derive from these three classes.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPin</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPin</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPin</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-beginflush">BeginFlush</a>
</td>
<td align="left" width="63%">
Begins a flush operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-connect">Connect</a>
</td>
<td align="left" width="63%">
Connects the pin to another pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-connectedto">ConnectedTo</a>
</td>
<td align="left" width="63%">
Retrieves the pin connected to this pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-connectionmediatype">ConnectionMediaType</a>
</td>
<td align="left" width="63%">
Gets the media type for the current pin connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-disconnect">Disconnect</a>
</td>
<td align="left" width="63%">
Breaks the current pin connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-endflush">EndFlush</a>
</td>
<td align="left" width="63%">
Ends a flush operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-endofstream">EndOfStream</a>
</td>
<td align="left" width="63%">
Notifies the pin that no additional data is expected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-enummediatypes">EnumMediaTypes</a>
</td>
<td align="left" width="63%">
Enumerates the pin's preferred media types.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-newsegment">NewSegment</a>
</td>
<td align="left" width="63%">
Notifies the pin that media samples received after this call are grouped as a segment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-queryaccept">QueryAccept</a>
</td>
<td align="left" width="63%">
Determines whether the pin accepts a specified media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-querydirection">QueryDirection</a>
</td>
<td align="left" width="63%">
Gets the direction of the pin (input or output).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-queryid">QueryId</a>
</td>
<td align="left" width="63%">
Gets the pin identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-queryinternalconnections">QueryInternalConnections</a>
</td>
<td align="left" width="63%">
Retrieves the pins that are connected internally to this pin (within the filter).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-querypininfo">QueryPinInfo</a>
</td>
<td align="left" width="63%">
Gets information about the pin, such as the name, the owning filter, and the direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-receiveconnection">ReceiveConnection</a>
</td>
<td align="left" width="63%">
Accepts a connection from another pin.

</td>
</tr>
</table> 

