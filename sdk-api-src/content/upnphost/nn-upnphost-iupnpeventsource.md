---
UID: NN:upnphost.IUPnPEventSource
title: IUPnPEventSource
author: windows-sdk-content
description: The IUPnPEventSource interface allows the device host to manage event subscriptions for the hosted service.
old-location: upnp\iupnpeventsource.htm
old-project: upnp
ms.assetid: f20dfcaa-b8fe-43c8-b353-067dad4cf2b4
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IUPnPEventSource, IUPnPEventSource interface [UPnP APIs], IUPnPEventSource interface [UPnP APIs],described, _upnp_iupnpeventsource, upnp.iupnpeventsource, upnphost/IUPnPEventSource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnphost.dll
api_name:
 - IUPnPEventSource
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnphost.dll
req.irql: 
req.product: Windows UI
---

# IUPnPEventSource interface


## -description


The 
<b>IUPnPEventSource</b> interface allows the device host to manage event subscriptions for the hosted service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPEventSource</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUPnPEventSource</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ec68f4ff-7549-4d48-b347-0320bc55329c">Advise</a>
</td>
<td align="left" width="63%">
Method that subscribes to a hosted service's events. The hosted device can then send events to the device host.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ae9c53f-eb82-4396-ba85-c95e252911c8">Unadvise</a>
</td>
<td align="left" width="63%">
Method that unsubscribes from a hosted service's events. The hosted device may no longer send events to the device host.

</td>
</tr>
</table> 

