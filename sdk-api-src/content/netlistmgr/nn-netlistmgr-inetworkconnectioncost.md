---
UID: NN:netlistmgr.INetworkConnectionCost
title: INetworkConnectionCost
author: windows-sdk-content
description: To query current network cost and data plan status associated with a connection.
old-location: nla\inetworkconnectcost.htm
old-project: NLA
ms.assetid: D04A5C34-6E5D-4F5B-B54D-3FDF7A936D9E
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: INetworkConnectionCost, INetworkConnectionCost interface [Network Awareness], INetworkConnectionCost interface [Network Awareness],described, netlistmgr/INetworkConnectionCost, nla.inetworkconnectcost
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - INetworkConnectionCost
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetworkConnectionCost interface


## -description


Use this interface to query current network cost and data plan status associated with a connection. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetworkConnectionCost</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INetworkConnectionCost</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/66D5FC1A-054C-406E-BEC3-CA62EA09CDF1">GetCost</a>
</td>
<td align="left" width="63%">
 Retrieves the network cost associated with a connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/861ED7D2-569A-4B62-BAB6-CA649CA9B524">GetDataPlanStatus</a>
</td>
<td align="left" width="63%">
Retrieves the status of the data plan associated with a connection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

