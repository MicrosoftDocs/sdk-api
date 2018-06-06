---
UID: NF:netlistmgr.INetworkConnectionCost.GetDataPlanStatus
title: INetworkConnectionCost::GetDataPlanStatus
author: windows-sdk-content
description: GetDataPlanStatus method retrieves the status of the data plan associated with a connection.
old-location: nla\inetworkconnectioncost_getdataplanstatus.htm
old-project: NLA
ms.assetid: 861ED7D2-569A-4B62-BAB6-CA649CA9B524
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetDataPlanStatus, GetDataPlanStatus method [Network Awareness], GetDataPlanStatus method [Network Awareness],INetworkConnectionCost interface, INetworkConnectionCost interface [Network Awareness],GetDataPlanStatus method, INetworkConnectionCost.GetDataPlanStatus, INetworkConnectionCost::GetDataPlanStatus, netlistmgr/INetworkConnectionCost::GetDataPlanStatus, nla.inetworkconnectioncost_getdataplanstatus
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
 - INetworkConnectionCost.GetDataPlanStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetworkConnectionCost::GetDataPlanStatus


## -description


The <b>GetDataPlanStatus</b> method retrieves the status of the data plan associated with a connection.


## -parameters




### -param pDataPlanStatus [out]

Pointer to an <a href="https://msdn.microsoft.com/49774150-FD7E-4541-95DF-C848247A6A9C">NLM_DATAPLAN_STATUS</a> structure that describes the status of the data plan associated with the connection. The caller supplies the memory of this structure.


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




<a href="https://msdn.microsoft.com/D04A5C34-6E5D-4F5B-B54D-3FDF7A936D9E">INetworkConnectionCost</a>
 

 

