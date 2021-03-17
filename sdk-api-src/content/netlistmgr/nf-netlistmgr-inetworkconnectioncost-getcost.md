---
UID: NF:netlistmgr.INetworkConnectionCost.GetCost
title: INetworkConnectionCost::GetCost (netlistmgr.h)
description: GetCost method retrieves the network cost associated with a connection.
helpviewer_keywords: ["GetCost","GetCost method [Network Awareness]","GetCost method [Network Awareness]","INetworkConnectionCost interface","INetworkConnectionCost interface [Network Awareness]","GetCost method","INetworkConnectionCost.GetCost","INetworkConnectionCost::GetCost","netlistmgr/INetworkConnectionCost::GetCost","nla.inetworkconnectioncost_getcost"]
old-location: nla\inetworkconnectioncost_getcost.htm
tech.root: nla
ms.assetid: 66D5FC1A-054C-406E-BEC3-CA62EA09CDF1
ms.date: 12/05/2018
ms.keywords: GetCost, GetCost method [Network Awareness], GetCost method [Network Awareness],INetworkConnectionCost interface, INetworkConnectionCost interface [Network Awareness],GetCost method, INetworkConnectionCost.GetCost, INetworkConnectionCost::GetCost, netlistmgr/INetworkConnectionCost::GetCost, nla.inetworkconnectioncost_getcost
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetworkConnectionCost::GetCost
 - netlistmgr/INetworkConnectionCost::GetCost
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
 - INetworkConnectionCost.GetCost
---

# INetworkConnectionCost::GetCost


## -description

The <b>GetCost</b> method retrieves the network cost associated with a connection.

## -parameters

### -param pCost [out]

A DWORD value that represents the network cost of the connection. The lowest 16 bits represent the cost level and the highest 16 bits represent the cost flags. Possible values are defined by the <a href="/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_connection_cost">NLM_CONNECTION_COST</a> enumeration.

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

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworkconnectioncost">INetworkConnectionCost</a>