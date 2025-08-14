---
UID: NF:clusapi.GetClusterNodeState
title: GetClusterNodeState function (clusapi.h)
description: Returns the current state of a node.
helpviewer_keywords: ["GetClusterNodeState","GetClusterNodeState function [Failover Cluster]","PCLUSAPI_GET_CLUSTER_NODE_STATE","PCLUSAPI_GET_CLUSTER_NODE_STATE function [Failover Cluster]","_wolf_getclusternodestate","clusapi/GetClusterNodeState","clusapi/PCLUSAPI_GET_CLUSTER_NODE_STATE","mscs.getclusternodestate"]
old-location: mscs\getclusternodestate.htm
tech.root: MsCS
ms.assetid: 94c83582-3d99-4a20-ad58-1af4e8190781
ms.date: 12/05/2018
ms.keywords: GetClusterNodeState, GetClusterNodeState function [Failover Cluster], PCLUSAPI_GET_CLUSTER_NODE_STATE, PCLUSAPI_GET_CLUSTER_NODE_STATE function [Failover Cluster], _wolf_getclusternodestate, clusapi/GetClusterNodeState, clusapi/PCLUSAPI_GET_CLUSTER_NODE_STATE, mscs.getclusternodestate
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
 - GetClusterNodeState
 - clusapi/GetClusterNodeState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-clusapi-l1-1-6.dll
 - ext-ms-win-cluster-clusapi-l1-1-5.dll
 - ext-ms-win-cluster-clusapi-l1-1-4.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
 - GetClusterNodeState
---

# GetClusterNodeState function


## -description

Returns the 
    current state of a <a href="/previous-versions/windows/desktop/mscs/nodes">node</a>. The <b>PCLUSAPI_GET_CLUSTER_NODE_STATE</b> type defines a pointer to this function.

## -parameters

### -param hNode [in]

Handle to the node for which state information should be returned.

## -returns

<b>GetClusterNodeState</b> returns the current state 
       of the node, which is represented by one of the following values.


The returned values are from the 
       <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_node_state">CLUSTER_NODE_STATE</a> enumeration.



<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterNodeUp</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The node is physically plugged in, turned on, booted, and capable of executing programs.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterNodeDown</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The node is turned off or not operational.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterNodeJoining</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The node is in the process of joining a 
        <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterNodePaused</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The node is running but not participating in cluster operations.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ClusterNodeStateUnknown</b></dt>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
The operation was not successful. For more information about the error, call the function 
        <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

</td>
</tr>
</table>

## -remarks

The <b>ClusterNodeDown</b> state only indicates that a node is inactive; it does not 
    specify the reason for the inactivity. A node can be in the <b>ClusterNodeDown</b> state for 
    the following reasons:

<ul>
<li>The node is not running.</li>
<li>The <a href="/previous-versions/windows/desktop/mscs/cluster-service">Cluster service</a> on the node is not 
      running.</li>
<li>The node cannot communicate with the node controlling the 
      <a href="/previous-versions/windows/desktop/mscs/quorum-resource">quorum resource</a>.</li>
<li>The node is inactive for any other reason.</li>
</ul>
When a node is operating as an active member of a cluster but cannot host any resources or groups, it is in 
    the <b>ClusterNodePaused</b> state (see the 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-pauseclusternode">PauseClusterNode</a> function). Nodes that are undergoing 
    maintenance are typically placed in this state.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_node_state">CLUSTER_NODE_STATE</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternode">OpenClusterNode</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-pauseclusternode">PauseClusterNode</a>