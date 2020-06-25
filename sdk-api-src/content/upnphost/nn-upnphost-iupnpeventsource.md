---
UID: NN:upnphost.IUPnPEventSource
title: IUPnPEventSource (upnphost.h)
description: The IUPnPEventSource interface allows the device host to manage event subscriptions for the hosted service.
helpviewer_keywords: ["IUPnPEventSource","IUPnPEventSource interface [UPnP APIs]","IUPnPEventSource interface [UPnP APIs]","described","_upnp_iupnpeventsource","upnp.iupnpeventsource","upnphost/IUPnPEventSource"]
old-location: upnp\iupnpeventsource.htm
tech.root: upnp
ms.assetid: f20dfcaa-b8fe-43c8-b353-067dad4cf2b4
ms.date: 12/05/2018
ms.keywords: IUPnPEventSource, IUPnPEventSource interface [UPnP APIs], IUPnPEventSource interface [UPnP APIs],described, _upnp_iupnpeventsource, upnp.iupnpeventsource, upnphost/IUPnPEventSource
f1_keywords:
- upnphost/IUPnPEventSource
dev_langs:
- c++
req.header: upnphost.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: Upnphost.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Upnphost.dll
api_name:
- IUPnPEventSource
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPEventSource interface


## -description


The 
<b>IUPnPEventSource</b> interface allows the device host to manage event subscriptions for the hosted service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPEventSource</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUPnPEventSource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPEventSource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnphost/nf-upnphost-iupnpeventsource-advise">Advise</a>
</td>
<td align="left" width="63%">
Method that subscribes to a hosted service's events. The hosted device can then send events to the device host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnphost/nf-upnphost-iupnpeventsource-unadvise">Unadvise</a>
</td>
<td align="left" width="63%">
Method that unsubscribes from a hosted service's events. The hosted device may no longer send events to the device host.

</td>
</tr>
</table> 

