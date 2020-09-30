---
UID: NN:netlistmgr.INetworkCostManager
title: INetworkCostManager (netlistmgr.h)
description: Use this interface to query for machine-wide cost and data plan status information associated with either a connection used for machine-wide Internet connectivity, or the first-hop of routing to a specific destination on a connection.
helpviewer_keywords: ["INetworkCostManager","INetworkCostManager interface [Network Awareness]","INetworkCostManager interface [Network Awareness]","described","netlistmgr/INetworkCostManager","nla.inetworkcostmanager"]
old-location: nla\inetworkcostmanager.htm
tech.root: nla
ms.assetid: A6316E94-398D-4D87-B631-6BEF416895EE
ms.date: 12/05/2018
ms.keywords: INetworkCostManager, INetworkCostManager interface [Network Awareness], INetworkCostManager interface [Network Awareness],described, netlistmgr/INetworkCostManager, nla.inetworkcostmanager
req.header: netlistmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
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
 - INetworkCostManager
 - netlistmgr/INetworkCostManager
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
 - INetworkCostManager
 - INetworkCostManager.GetCost
---

# INetworkCostManager interface


## -description

Use this interface to query for machine-wide cost and data plan status information associated with either a connection used for machine-wide Internet connectivity, or the first-hop of routing to a specific destination on a connection. Additionally, this interface enables applications to specify destination IP addresses  to receive cost or data plan status change notifications for.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetworkCostManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INetworkCostManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetworkCostManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>GetCost</b></td>
<td align="left" width="63%">
Retrieves the current cost of either a machine-wide internet connection, or the first-hop of routing to a specific destination on a connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="nla.getdataplanstatus">GetDataPlanStatus</a>
</td>
<td align="left" width="63%">
Retrieves the data plan status for either a machine-wide internet connection , or the first-hop of routing to a specific destination on a connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="nla.setdestinationaddresses">SetDestinationAddresses</a>
</td>
<td align="left" width="63%">
Registers specified destination IP addresses to receive cost or data plan status change notifications.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworkcostmanagerevents">INetworkCostManagerEvents</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>