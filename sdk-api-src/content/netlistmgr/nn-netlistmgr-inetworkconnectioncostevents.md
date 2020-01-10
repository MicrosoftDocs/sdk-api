---
UID: NN:netlistmgr.INetworkConnectionCostEvents
title: INetworkConnectionCostEvents (netlistmgr.h)
description: This interface to notify an application of cost and data plan status change events for a connection.
old-location: nla\inetworkconnectioncostevents.htm
tech.root: nla
ms.assetid: ABFE73E5-CB9E-4077-81D2-DD0FB39F4EC5
ms.date: 12/05/2018
ms.keywords: INetworkConnectionCostEvents, INetworkConnectionCostEvents interface [Network Awareness], INetworkConnectionCostEvents interface [Network Awareness],described, netlistmgr/INetworkConnectionCostEvents, nla.inetworkconnectioncostevents
f1_keywords:
- netlistmgr/INetworkConnectionCostEvents
dev_langs:
- c++
req.header: netlistmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
- INetworkConnectionCostEvents
- INetworkConnectionCostEvents.ConnectionCostChanged
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetworkConnectionCostEvents interface


## -description


Use this interface to notify an application of cost and data plan status change events for a connection. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetworkConnectionCostEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INetworkConnectionCostEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetworkConnectionCostEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>ConnectionCostChanged</b></td>
<td align="left" width="63%">
Indicates a network cost change.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworkconnectioncostevents-connectiondataplanstatuschanged">ConnectionDataPlanStatusChanged</a>
</td>
<td align="left" width="63%">
Indicates a data plan status change.

</td>
</tr>
</table> 

