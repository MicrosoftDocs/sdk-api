---
UID: NN:strmif.IPin
title: IPin
author: windows-sdk-content
description: This interface is exposed by all input and output pins.The filter graph manager uses this interface to connect pins and perform flushing operations.
old-location: dshow\ipin.htm
tech.root: DirectShow
ms.assetid: ad0ead4e-9f8e-4935-b220-306d665e50f4
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IPin, IPin interface [DirectShow], IPin interface [DirectShow],described, IPinInterface, dshow.ipin, strmif/IPin
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IPin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPin interface


## -description



This interface is exposed by all input and output pins.

The filter graph manager uses this interface to connect pins and perform flushing operations. Applications can use this interface to query the pin for information. Applications should never call <code>IPin</code> methods that change a pin's state, such as <a href="https://msdn.microsoft.com/1b02ee67-5dc5-44c1-bea5-2eab46ebd0f6">Connect</a>, <a href="https://msdn.microsoft.com/46e1e99c-848b-4936-b6bf-4ef1703a1f42">Disconnect</a>, <a href="https://msdn.microsoft.com/15563666-5f35-46a0-ad12-215979c9d9c1">BeginFlush</a>, or <a href="https://msdn.microsoft.com/42b201b6-1fbf-4a01-aed7-23a9e66c11ea">EndFlush</a>. To connect pins, an application must use the methods in <a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder</a>.

<b>Filter developers: </b>The <a href="https://msdn.microsoft.com/23b9a0e2-24fe-4ff9-b2bb-97630c237de9">CBasePin</a>, <a href="https://msdn.microsoft.com/5a2b7f09-8c8b-45da-a4b7-afeb8d5548c1">CBaseInputPin</a>, and <a href="https://msdn.microsoft.com/5279c8aa-6ec0-4a89-a1b3-6904d7b69a93">CBaseOutputPin</a> classes implement this interface. Other base classes derive from these three classes.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPin</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPin</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/15563666-5f35-46a0-ad12-215979c9d9c1">BeginFlush</a>
</td>
<td align="left" width="63%">
Begins a flush operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b02ee67-5dc5-44c1-bea5-2eab46ebd0f6">Connect</a>
</td>
<td align="left" width="63%">
Connects the pin to another pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/970c814f-2309-481e-9e8e-9bd32b83fdc7">ConnectedTo</a>
</td>
<td align="left" width="63%">
Retrieves the pin connected to this pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f372bfa7-b0ba-43f9-ba86-cbca5d1de515">ConnectionMediaType</a>
</td>
<td align="left" width="63%">
Gets the media type for the current pin connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46e1e99c-848b-4936-b6bf-4ef1703a1f42">Disconnect</a>
</td>
<td align="left" width="63%">
Breaks the current pin connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42b201b6-1fbf-4a01-aed7-23a9e66c11ea">EndFlush</a>
</td>
<td align="left" width="63%">
Ends a flush operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0cca250-9603-4d58-8af5-5b272730e5fa">EndOfStream</a>
</td>
<td align="left" width="63%">
Notifies the pin that no additional data is expected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/288be4db-5236-40e5-bd92-d95b1bfb86fa">EnumMediaTypes</a>
</td>
<td align="left" width="63%">
Enumerates the pin's preferred media types.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70c4bda0-3efa-4f85-b71e-174c4c80830c">NewSegment</a>
</td>
<td align="left" width="63%">
Notifies the pin that media samples received after this call are grouped as a segment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed11eeef-464b-4a75-958b-2bc6dbc7af04">QueryAccept</a>
</td>
<td align="left" width="63%">
Determines whether the pin accepts a specified media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc36b5d6-bcca-403d-b840-ceabbf159f5d">QueryDirection</a>
</td>
<td align="left" width="63%">
Gets the direction of the pin (input or output).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4fb2713-549d-4c0d-9768-386bcffd696f">QueryId</a>
</td>
<td align="left" width="63%">
Gets the pin identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0289b89-9220-402c-858c-09076e2ab6b6">QueryInternalConnections</a>
</td>
<td align="left" width="63%">
Retrieves the pins that are connected internally to this pin (within the filter).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a7c85ce-46f1-4928-9e2a-3a4bd96dc771">QueryPinInfo</a>
</td>
<td align="left" width="63%">
Gets information about the pin, such as the name, the owning filter, and the direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2013e95-88bc-4f4a-87af-2b13c120ec46">ReceiveConnection</a>
</td>
<td align="left" width="63%">
Accepts a connection from another pin.

</td>
</tr>
</table> 

