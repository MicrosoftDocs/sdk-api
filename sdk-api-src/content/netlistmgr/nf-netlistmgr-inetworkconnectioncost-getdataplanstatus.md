---
UID: NF:netlistmgr.INetworkConnectionCost.GetDataPlanStatus
title: INetworkConnectionCost::GetDataPlanStatus (netlistmgr.h)
description: GetDataPlanStatus method retrieves the status of the data plan associated with a connection.
helpviewer_keywords: ["GetDataPlanStatus","GetDataPlanStatus method [Network Awareness]","GetDataPlanStatus method [Network Awareness]","INetworkConnectionCost interface","INetworkConnectionCost interface [Network Awareness]","GetDataPlanStatus method","INetworkConnectionCost.GetDataPlanStatus","INetworkConnectionCost::GetDataPlanStatus","netlistmgr/INetworkConnectionCost::GetDataPlanStatus","nla.inetworkconnectioncost_getdataplanstatus"]
old-location: nla\inetworkconnectioncost_getdataplanstatus.htm
tech.root: nla
ms.assetid: 861ED7D2-569A-4B62-BAB6-CA649CA9B524
ms.date: 12/05/2018
ms.keywords: GetDataPlanStatus, GetDataPlanStatus method [Network Awareness], GetDataPlanStatus method [Network Awareness],INetworkConnectionCost interface, INetworkConnectionCost interface [Network Awareness],GetDataPlanStatus method, INetworkConnectionCost.GetDataPlanStatus, INetworkConnectionCost::GetDataPlanStatus, netlistmgr/INetworkConnectionCost::GetDataPlanStatus, nla.inetworkconnectioncost_getdataplanstatus
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
 - INetworkConnectionCost::GetDataPlanStatus
 - netlistmgr/INetworkConnectionCost::GetDataPlanStatus
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
 - INetworkConnectionCost.GetDataPlanStatus
---

# INetworkConnectionCost::GetDataPlanStatus


## -description

The <b>GetDataPlanStatus</b> method retrieves the status of the data plan associated with a connection.

## -parameters

### -param pDataPlanStatus [out]

Pointer to an <a href="/windows/desktop/api/netlistmgr/ns-netlistmgr-nlm_dataplan_status">NLM_DATAPLAN_STATUS</a> structure that describes the status of the data plan associated with the connection. The caller supplies the memory of this structure.

## -returns

Returns S_OK on success. Otherwise, an HRESULT error code is returned. Possible values include:

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