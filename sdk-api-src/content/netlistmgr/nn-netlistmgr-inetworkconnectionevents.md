---
UID: NN:netlistmgr.INetworkConnectionEvents
title: INetworkConnectionEvents (netlistmgr.h)
author: windows-sdk-content
description: The INetworkConnectionEvents interface is a message sink interface that a client implements to get network connection-related events. Applications that are interested in lower-level events (such as authentication changes) must implement this interface.
old-location: nla\inetworkconnectionevents.htm
tech.root: nla
ms.assetid: 339f23ee-583d-4623-ad43-00b4fd4395ad
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: INetworkConnectionEvents, INetworkConnectionEvents interface [Network Awareness], INetworkConnectionEvents interface [Network Awareness],described, netlistmgr/INetworkConnectionEvents, nla.inetworkconnectionevents
ms.topic: interface
req.header: netlistmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Netlistmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Netlistmgr.h
api_name:
 - INetworkConnectionEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetworkConnectionEvents interface


## -description


The <b>INetworkConnectionEvents</b> interface is a message sink interface that a client implements to get network connection-related events. Applications that are interested in lower-level events (such as authentication changes) must implement this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetworkConnectionEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INetworkConnectionEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetworkConnectionEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b245a6e-918c-41de-b33e-87723491e900">NetworkConnectionConnectivityChanged</a>
</td>
<td align="left" width="63%">
Notifies a client when connectivity change events occur on a network connection level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38c6a422-9291-4136-ac81-b634040138b3">NetworkConnectionPropertyChange</a>
</td>
<td align="left" width="63%">
Notifies a client when property change events related to a specific network connection occur.

</td>
</tr>
</table> 

