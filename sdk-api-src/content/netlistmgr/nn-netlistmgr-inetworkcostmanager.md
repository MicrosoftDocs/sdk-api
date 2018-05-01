---
UID: NN:netlistmgr.INetworkCostManager
title: INetworkCostManager
author: windows-driver-content
description: Use this interface to query for machine-wide cost and data plan status information associated with either a connection used for machine-wide Internet connectivity, or the first-hop of routing to a specific destination on a connection.
old-location: nla\inetworkcostmanager.htm
old-project: NLA
ms.assetid: A6316E94-398D-4D87-B631-6BEF416895EE
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: INetworkCostManager, INetworkCostManager interface [Network Awareness], INetworkCostManager interface [Network Awareness], described, netlistmgr/INetworkCostManager, nla.inetworkcostmanager
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: NLM_NETWORK_PROPERTY_CHANGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Netlistmgr.h
api_name:
-	INetworkCostManager
-	INetworkCostManager.GetCost
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# INetworkCostManager interface


## -description


Use this interface to query for machine-wide cost and data plan status information associated with either a connection used for machine-wide Internet connectivity, or the first-hop of routing to a specific destination on a connection. Additionally, this interface enables applications to specify destination IP addresses  to receive cost or data plan status change notifications for.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetworkCostManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INetworkCostManager</b> also has these types of members:
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




<a href="https://msdn.microsoft.com/A8F4194E-6E9A-4173-8F88-FC2923B11CF0">INetworkCostManagerEvents</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

