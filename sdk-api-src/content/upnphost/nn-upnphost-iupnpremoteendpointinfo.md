---
UID: NN:upnphost.IUPnPRemoteEndpointInfo
title: IUPnPRemoteEndpointInfo
author: windows-driver-content
description: The IUPnPRemoteEndpointInfo interface allows a hosted device to obtain information about a requester (that is, a control point) and the request.
old-location: upnp\iupnpremoteendpointinfo.htm
old-project: UPnP
ms.assetid: 32e246cd-50eb-4221-8166-a7cd8ed42d69
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: IUPnPRemoteEndpointInfo, IUPnPRemoteEndpointInfo interface [UPnP APIs], IUPnPRemoteEndpointInfo interface [UPnP APIs],described, upnp.iupnpremoteendpointinfo, upnphost/IUPnPRemoteEndpointInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: upnphost.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Upnphost.dll
api_name:
-	IUPnPRemoteEndpointInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnphost.dll
req.irql: 
req.product: Windows UI
---

# IUPnPRemoteEndpointInfo interface


## -description


The <b>IUPnPRemoteEndpointInfo</b> interface allows a hosted device to obtain information about a requester (that is,  a control point) and the request.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPRemoteEndpointInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUPnPRemoteEndpointInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPRemoteEndpointInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/efbb0671-cb32-41e1-8405-1d145c247673">GetDwordValue</a>
</td>
<td align="left" width="63%">
Gets a 4-byte value that provides information about either a request or requester.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597612">GetGuidValue</a>
</td>
<td align="left" width="63%">
Currently not supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597621">GetStringValue</a>
</td>
<td align="left" width="63%">
Gets a string that provides information about either a request or requester.

</td>
</tr>
</table> 

