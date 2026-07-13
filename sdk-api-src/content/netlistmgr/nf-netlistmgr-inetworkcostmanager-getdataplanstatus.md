---
UID: NF:netlistmgr.INetworkCostManager.GetDataPlanStatus
title: INetworkCostManager::GetDataPlanStatus (netlistmgr.h)
description: GetDataPlanStatus retrieves the data plan status for either a machine-wide internet connection , or the first-hop of routing to a specific destination on a connection.
helpviewer_keywords: ["GetDataPlanStatus","GetDataPlanStatus method [Network Awareness]","GetDataPlanStatus method [Network Awareness]","INetworkCostManager interface","INetworkCostManager interface [Network Awareness]","GetDataPlanStatus method","INetworkCostManager.GetDataPlanStatus","INetworkCostManager::GetDataPlanStatus","netlistmgr/INetworkCostManager::GetDataPlanStatus","nla.inetworkcostmanager_getdataplanstatus"]
old-location: nla\inetworkcostmanager_getdataplanstatus.htm
tech.root: nla
ms.assetid: 82B4FF65-5D45-4D79-8F11-EA4CF4760EE2
ms.date: 12/05/2018
ms.keywords: GetDataPlanStatus, GetDataPlanStatus method [Network Awareness], GetDataPlanStatus method [Network Awareness],INetworkCostManager interface, INetworkCostManager interface [Network Awareness],GetDataPlanStatus method, INetworkCostManager.GetDataPlanStatus, INetworkCostManager::GetDataPlanStatus, netlistmgr/INetworkCostManager::GetDataPlanStatus, nla.inetworkcostmanager_getdataplanstatus
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
 - INetworkCostManager::GetDataPlanStatus
 - netlistmgr/INetworkCostManager::GetDataPlanStatus
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
 - INetworkCostManager.GetDataPlanStatus
---

# INetworkCostManager::GetDataPlanStatus


## -description

The <b>GetDataPlanStatus</b> retrieves the data plan status for either a machine-wide internet connection , or the first-hop of routing to a specific destination on a connection. If an IPv4/IPv6 address is not specified, this method returns the data plan status of the connection used for machine-wide Internet connectivity.

## -parameters

### -param pDataPlanStatus [out]

Pointer to an <a href="/windows/desktop/api/netlistmgr/ns-netlistmgr-nlm_dataplan_status">NLM_DATAPLAN_STATUS</a> structure that describes the data plan status associated with a connection used to route to a destination. If <i>destIPAddr</i> specifies a tunnel address, the first available data plan status in the interface stack is returned.

### -param pDestIPAddr [in]

An <a href="/windows/desktop/api/netlistmgr/ns-netlistmgr-nlm_sockaddr">NLM_SOCKADDR</a> structure containing the destination IPv4/IPv6 or tunnel address. If   NULL, this method returns the cost associated with the preferred connection used for machine Internet connectivity.

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
<i>pDataPlanStatus</i> is NULL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
Determining the interface used to route to the destination

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The destination address specified by <i>destIPAddr</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if either an IPv4 or IPv6 stack is not present on the local computer but either an IPv4 or IPv6 address was specified by <i>destIPAddr</i>.

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