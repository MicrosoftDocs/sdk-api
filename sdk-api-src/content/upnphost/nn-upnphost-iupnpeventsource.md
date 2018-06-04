---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

