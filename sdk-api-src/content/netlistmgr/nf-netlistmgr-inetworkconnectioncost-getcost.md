---
UID: NF:netlistmgr.INetworkConnectionCost.GetCost
title: INetworkConnectionCost::GetCost
author: windows-sdk-content
description: GetCost method retrieves the network cost associated with a connection.
old-location: nla\inetworkconnectioncost_getcost.htm
old-project: NLA
ms.assetid: 66D5FC1A-054C-406E-BEC3-CA62EA09CDF1
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetCost, GetCost method [Network Awareness], GetCost method [Network Awareness],INetworkConnectionCost interface, INetworkConnectionCost interface [Network Awareness],GetCost method, INetworkConnectionCost.GetCost, INetworkConnectionCost::GetCost, netlistmgr/INetworkConnectionCost::GetCost, nla.inetworkconnectioncost_getcost
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - INetworkConnectionCost.GetCost
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetworkConnectionCost::GetCost


## -description


The <b>GetCost</b> method retrieves the network cost associated with a connection.


## -parameters




### -param pCost [out]

A DWORD value that represents the network cost of the connection. The lowest 16 bits represent the cost level and the highest 16 bits represent the cost flags. Possible values are defined by the <a href="https://msdn.microsoft.com/93541814-A1C3-4C24-BB99-CEE4895F34F8">NLM_CONNECTION_COST</a> enumeration.


## -returns



Returns S_OK on success. Otherwise an HRESULT error code is returned. Possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pCost</i> is NULL

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NO_NETWORK)</b></dt>
</dl>
</td>
<td width="60%">
Network connectivity is currently unavailable.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/D04A5C34-6E5D-4F5B-B54D-3FDF7A936D9E">INetworkConnectionCost</a>
 

 

