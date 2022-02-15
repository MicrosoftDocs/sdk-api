---
UID: NF:netlistmgr.INetworkCostManager.GetCost
title: INetworkCostManager::GetCost (netlistmgr.h)
description: GetCost method retrieves the current cost of either a machine-wide internet connection, or the first-hop of routing to a specific destination on a connection.
helpviewer_keywords: ["GetCost","GetCost method [Network Awareness]","GetCost method [Network Awareness]","INetworkCostManager interface","INetworkCostManager interface [Network Awareness]","GetCost method","INetworkCostManager.GetCost","INetworkCostManager::GetCost","netlistmgr/INetworkCostManager::GetCost","nla.inetworkcostmanager_getcost"]
old-location: nla\inetworkcostmanager_getcost.htm
tech.root: nla
ms.assetid: F0690CD5-0BC9-4042-9A38-17B48761034F
ms.date: 12/05/2018
ms.keywords: GetCost, GetCost method [Network Awareness], GetCost method [Network Awareness],INetworkCostManager interface, INetworkCostManager interface [Network Awareness],GetCost method, INetworkCostManager.GetCost, INetworkCostManager::GetCost, netlistmgr/INetworkCostManager::GetCost, nla.inetworkcostmanager_getcost
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
 - INetworkCostManager::GetCost
 - netlistmgr/INetworkCostManager::GetCost
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
 - INetworkCostManager.GetCost
---

# INetworkCostManager::GetCost


## -description

The  <b>GetCost</b> method retrieves the current cost of either a machine-wide internet connection, or the first-hop of routing to a specific destination on a connection. If <i>destIPaddr</i> is NULL, this method instead returns the cost of the network used for machine-wide Internet connectivity.

## -parameters

### -param pCost [out]

A DWORD value that indicates the cost of the connection. The lowest 16 bits represent the cost level, and the highest 16 bits represent the flags. Possible values are defined by the <a href="/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_connection_cost">NLM_CONNECTION_COST</a> enumeration.

### -param pDestIPAddr [in]

An <a href="/windows/desktop/api/netlistmgr/ns-netlistmgr-nlm_sockaddr">NLM_SOCKADDR</a> structure containing the destination IPv4/IPv6 address. If  NULL, this method will instead return the cost associated with the preferred connection used for machine Internet connectivity.

## -returns

Returns S_OK on success, otherwise an HRESULT error code is returned.

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
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
Currently determining the interface used to route to the destination

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The destination IPv4/IPv6 address specified by <i>destIPAddr</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if either an IPv4 or IPv6 stack is not present on the local computer but  either an IPv4 or IPv6 address was specified by <i>destIPAddr</i>.

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

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworkcostmanager">INetworkCostManager</a>



<a href="/windows/desktop/api/netlistmgr/ns-netlistmgr-nlm_sockaddr">NLM_SOCKADDR</a>