---
UID: NN:netlistmgr.INetworkCostManagerEvents
title: INetworkCostManagerEvents (netlistmgr.h)
description: This interface to notify an application of machine-wide cost and data plan related events.
helpviewer_keywords: ["INetworkCostManagerEvents","INetworkCostManagerEvents interface [Network Awareness]","INetworkCostManagerEvents interface [Network Awareness]","described","netlistmgr/INetworkCostManagerEvents","nla.inetworkcostmanagerevents"]
old-location: nla\inetworkcostmanagerevents.htm
tech.root: nla
ms.assetid: A8F4194E-6E9A-4173-8F88-FC2923B11CF0
ms.date: 12/05/2018
ms.keywords: INetworkCostManagerEvents, INetworkCostManagerEvents interface [Network Awareness], INetworkCostManagerEvents interface [Network Awareness],described, netlistmgr/INetworkCostManagerEvents, nla.inetworkcostmanagerevents
f1_keywords:
- netlistmgr/INetworkCostManagerEvents
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Netlistmgr.h
api_name:
- INetworkCostManagerEvents
- INetworkCostManagerEvents.CostChanged
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetworkCostManagerEvents interface


## -description


Use this interface to notify an application of machine-wide cost and data plan related events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetworkCostManagerEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INetworkCostManagerEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetworkCostManagerEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>CostChanged</b></td>
<td align="left" width="63%">
Indicates a cost change for either machine-wide Internet connectivity, or the first-hop of routing to a specific destination on a connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworkcostmanagerevents-dataplanstatuschanged">DataPlanStatusChanged</a>
</td>
<td align="left" width="63%">
Indicates a change to the status of a data plan associated with a connection used for either machine-wide Internet connectivity, or the first-hop of routing to a specific destination on a connection.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

