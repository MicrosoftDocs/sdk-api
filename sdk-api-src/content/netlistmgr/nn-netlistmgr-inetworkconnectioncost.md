---
UID: NN:netlistmgr.INetworkConnectionCost
title: INetworkConnectionCost (netlistmgr.h)
description: To query current network cost and data plan status associated with a connection.helpviewer_keywords: ["INetworkConnectionCost","INetworkConnectionCost interface [Network Awareness]","INetworkConnectionCost interface [Network Awareness]","described","netlistmgr/INetworkConnectionCost","nla.inetworkconnectcost"]
old-location: nla\inetworkconnectcost.htm
tech.root: nla
ms.assetid: D04A5C34-6E5D-4F5B-B54D-3FDF7A936D9E
ms.date: 12/05/2018
ms.keywords: INetworkConnectionCost, INetworkConnectionCost interface [Network Awareness], INetworkConnectionCost interface [Network Awareness],described, netlistmgr/INetworkConnectionCost, nla.inetworkconnectcost
f1_keywords:
- netlistmgr/INetworkConnectionCost
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
- INetworkConnectionCost
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetworkConnectionCost interface


## -description


Use this interface to query current network cost and data plan status associated with a connection. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetworkConnectionCost</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INetworkConnectionCost</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetworkConnectionCost</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworkconnectioncost-getcost">GetCost</a>
</td>
<td align="left" width="63%">
 Retrieves the network cost associated with a connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworkconnectioncost-getdataplanstatus">GetDataPlanStatus</a>
</td>
<td align="left" width="63%">
Retrieves the status of the data plan associated with a connection.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

