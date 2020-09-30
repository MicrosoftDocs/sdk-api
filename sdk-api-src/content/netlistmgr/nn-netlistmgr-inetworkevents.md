---
UID: NN:netlistmgr.INetworkEvents
title: INetworkEvents (netlistmgr.h)
description: INetworkEvents is a notification sink interface that a client implements to get network related events. These APIs are all callback functions that are called automatically when the respective events are raised.
helpviewer_keywords: ["INetworkEvents","INetworkEvents interface [Network Awareness]","INetworkEvents interface [Network Awareness]","described","netlistmgr/INetworkEvents","nla.inetworkevents"]
old-location: nla\inetworkevents.htm
tech.root: nla
ms.assetid: 75cc6efb-dd1b-40b6-84fe-5ba7c244cd72
ms.date: 12/05/2018
ms.keywords: INetworkEvents, INetworkEvents interface [Network Awareness], INetworkEvents interface [Network Awareness],described, netlistmgr/INetworkEvents, nla.inetworkevents
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetworkEvents
 - netlistmgr/INetworkEvents
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Netlistmgr.h
api_name:
 - INetworkEvents
---

# INetworkEvents interface


## -description

<b>INetworkEvents</b> is a notification sink interface that a client implements to get network related events. These APIs are all callback functions that are called automatically when the respective events are raised.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetworkEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INetworkEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetworkEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworkevents-networkadded">NetworkAdded</a>
</td>
<td align="left" width="63%">
Called when a new network is added.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworkevents-networkconnectivitychanged">NetworkConnectivityChanged</a>
</td>
<td align="left" width="63%">
Called when network connectivity related changes occur. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworkevents-networkdeleted">NetworkDeleted</a>
</td>
<td align="left" width="63%">
Called when a network is deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworkevents-networkpropertychanged">NetworkPropertyChanged</a>
</td>
<td align="left" width="63%">
Called when a network property change is detected.

</td>
</tr>
</table>