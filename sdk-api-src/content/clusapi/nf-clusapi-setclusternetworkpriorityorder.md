---
UID: NF:clusapi.SetClusterNetworkPriorityOrder
title: SetClusterNetworkPriorityOrder function (clusapi.h)
description: Sets the priority order for the set of networks used for internal communication between cluster nodes.
helpviewer_keywords: ["PCLUSAPI_SET_CLUSTER_NETWORK_PRIORITY_ORDER","PCLUSAPI_SET_CLUSTER_NETWORK_PRIORITY_ORDER function [Failover Cluster]","SetClusterNetworkPriorityOrder","SetClusterNetworkPriorityOrder function [Failover Cluster]","_wolf_setclusternetworkpriorityorder","clusapi/PCLUSAPI_SET_CLUSTER_NETWORK_PRIORITY_ORDER","clusapi/SetClusterNetworkPriorityOrder","mscs.setclusternetworkpriorityorder"]
old-location: mscs\setclusternetworkpriorityorder.htm
tech.root: MsCS
ms.assetid: 538e5024-6c51-4b11-a5ff-9df6aa7a4606
ms.date: 12/05/2018
ms.keywords: PCLUSAPI_SET_CLUSTER_NETWORK_PRIORITY_ORDER, PCLUSAPI_SET_CLUSTER_NETWORK_PRIORITY_ORDER function [Failover Cluster], SetClusterNetworkPriorityOrder, SetClusterNetworkPriorityOrder function [Failover Cluster], _wolf_setclusternetworkpriorityorder, clusapi/PCLUSAPI_SET_CLUSTER_NETWORK_PRIORITY_ORDER, clusapi/SetClusterNetworkPriorityOrder, mscs.setclusternetworkpriorityorder
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 Enterprise, Windows Server 2003 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetClusterNetworkPriorityOrder
 - clusapi/SetClusterNetworkPriorityOrder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - SetClusterNetworkPriorityOrder
---

# SetClusterNetworkPriorityOrder function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008 and this function does nothing and returns 
    <b>ERROR_CALL_NOT_IMPLEMENTED</b>.]

Sets the priority order for the set of <a href="/previous-versions/windows/desktop/mscs/networks">networks</a> used for 
    internal communication between cluster <a href="/previous-versions/windows/desktop/mscs/nodes">nodes</a>. The <b>PCLUSAPI_SET_CLUSTER_NETWORK_PRIORITY_ORDER</b> type defines a pointer to this function.

## -parameters

### -param hCluster [in]

Handle to the <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> to be affected.

### -param NetworkCount [in]

Number of items in the list specified by the <i>NetworkList</i> parameter.

### -param NetworkList [in]

Prioritized array of handles to network objects. The first handle in the array has the highest priority. The 
       list must contain only those networks that are used for internal communication between nodes in the cluster, 
       and there can be no duplicates.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b> (0).

If the operation fails, the function returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following are possible error 
       codes.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
<dt>87 (0x57)</dt>
</dl>
</td>
<td width="60%">
There was a duplicate network in <i>NetworkList</i>.

</td>
</tr>
</table>

## -remarks

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
     can have additional destructive effects. For information on how LPC and RPC handles are created, see 
     <a href="/previous-versions/windows/desktop/mscs/using-object-handles">Using Object Handles</a> and 
     <a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterenum">ClusterEnum</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternetwork">OpenClusterNetwork</a>