---
UID: NF:clusapi.GetClusterNetworkState
title: GetClusterNetworkState function (clusapi.h)
description: Current state of a network.
helpviewer_keywords: ["GetClusterNetworkState","GetClusterNetworkState function [Failover Cluster]","PCLUSAPI_GET_CLUSTER_NETWORK_STATE","PCLUSAPI_GET_CLUSTER_NETWORK_STATE function [Failover Cluster]","_wolf_getclusternetworkstate","clusapi/GetClusterNetworkState","clusapi/PCLUSAPI_GET_CLUSTER_NETWORK_STATE","mscs.getclusternetworkstate"]
old-location: mscs\getclusternetworkstate.htm
tech.root: MsCS
ms.assetid: 7fdbc0cf-fa7b-4b48-bd3c-46f174fc514a
ms.date: 12/05/2018
ms.keywords: GetClusterNetworkState, GetClusterNetworkState function [Failover Cluster], PCLUSAPI_GET_CLUSTER_NETWORK_STATE, PCLUSAPI_GET_CLUSTER_NETWORK_STATE function [Failover Cluster], _wolf_getclusternetworkstate, clusapi/GetClusterNetworkState, clusapi/PCLUSAPI_GET_CLUSTER_NETWORK_STATE, mscs.getclusternetworkstate
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
 - GetClusterNetworkState
 - clusapi/GetClusterNetworkState
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
 - GetClusterNetworkState
---

# GetClusterNetworkState function


## -description

Returns 
    the current state of a <a href="/previous-versions/windows/desktop/mscs/networks">network</a>. The <b>PCLUSAPI_GET_CLUSTER_NETWORK_STATE</b> type defines a pointer to this function.

## -parameters

### -param hNetwork [in]

Handle to the network for which state information should be returned.

## -returns

<b>GetClusterNetworkState</b> returns the current 
       state of the network, which is represented by one of the following values enumerated by the 
       <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_network_state">CLUSTER_NETWORK_STATE</a> enumeration.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterNetworkUnavailable</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
All of the network interfaces on the network are unavailable, which means that the nodes that own the 
        network interfaces are down.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterNetworkDown</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The network is not operational; none of the <a href="/previous-versions/windows/desktop/mscs/nodes">nodes</a> on the 
        network can communicate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterNetworkPartitioned</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The network is operational, but two or more nodes on the network cannot communicate. Typically a 
        path-specific problem has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterNetworkUp</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The network is operational; all of the nodes in the cluster can communicate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterNetworkStateUnknown</b></dt>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
The operation was not successful. For more information about the error, call the function 
        <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_network_state">CLUSTER_NETWORK_STATE</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternetwork">OpenClusterNetwork</a>