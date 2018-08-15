---
UID: NN:netlistmgr.INetworkEvents
title: INetworkEvents
author: windows-sdk-content
description: INetworkEvents is a notification sink interface that a client implements to get network related events. These APIs are all callback functions that are called automatically when the respective events are raised.
old-location: nla\inetworkevents.htm
old-project: nla
ms.assetid: 75cc6efb-dd1b-40b6-84fe-5ba7c244cd72
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: INetworkEvents, INetworkEvents interface [Network Awareness], INetworkEvents interface [Network Awareness],described, netlistmgr/INetworkEvents, nla.inetworkevents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: netlistmgr.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: NLM_NETWORK_PROPERTY_CHANGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Netlistmgr.h
api_name:
 - INetworkEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetworkEvents interface


## -description


<b>INetworkEvents</b> is a notification sink interface that a client implements to get network related events. These APIs are all callback functions that are called automatically when the respective events are raised.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetworkEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INetworkEvents</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/2fda364e-ad6a-447a-ba0c-25e5d52ef5c5">NetworkAdded</a>
</td>
<td align="left" width="63%">
Called when a new network is added.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/adaf3abe-9a8c-45af-bcc7-bcc516ed75ff">NetworkConnectivityChanged</a>
</td>
<td align="left" width="63%">
Called when network connectivity related changes occur. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae54cc29-6da8-405d-92f9-654239150dd0">NetworkDeleted</a>
</td>
<td align="left" width="63%">
Called when a network is deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a84f49ee-9efd-450e-a6e6-3f140330a9d0">NetworkPropertyChanged</a>
</td>
<td align="left" width="63%">
Called when a network property change is detected.

</td>
</tr>
</table> 

