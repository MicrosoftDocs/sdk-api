---
UID: NF:clusapi.MoveClusterGroup
title: MoveClusterGroup function (clusapi.h)
description: Moves a group and all of its resources from one node to another.
helpviewer_keywords: ["MoveClusterGroup","MoveClusterGroup function [Failover Cluster]","PCLUSAPI_MOVE_CLUSTER_GROUP","PCLUSAPI_MOVE_CLUSTER_GROUP function [Failover Cluster]","_wolf_moveclustergroup","clusapi/MoveClusterGroup","clusapi/PCLUSAPI_MOVE_CLUSTER_GROUP","mscs.moveclustergroup"]
old-location: mscs\moveclustergroup.htm
tech.root: MsCS
ms.assetid: 32408600-5118-47fb-890b-9c31faef2299
ms.date: 12/05/2018
ms.keywords: MoveClusterGroup, MoveClusterGroup function [Failover Cluster], PCLUSAPI_MOVE_CLUSTER_GROUP, PCLUSAPI_MOVE_CLUSTER_GROUP function [Failover Cluster], _wolf_moveclustergroup, clusapi/MoveClusterGroup, clusapi/PCLUSAPI_MOVE_CLUSTER_GROUP, mscs.moveclustergroup
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
 - MoveClusterGroup
 - clusapi/MoveClusterGroup
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
 - MoveClusterGroup
---

# MoveClusterGroup function


## -description

Moves a  <a href="/previous-versions/windows/desktop/mscs/groups">group</a> and all of its  <a href="/previous-versions/windows/desktop/mscs/resources">resources</a> from one  <a href="/previous-versions/windows/desktop/mscs/nodes">node</a> to another. The <b>PCLUSAPI_MOVE_CLUSTER_GROUP</b> type defines a pointer to this function.

## -parameters

### -param hGroup [in]

Handle to the group to be moved.

### -param hDestinationNode [in, optional]

Handle to the node where the moved group should be brought back online or <b>NULL</b>.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following is one of the possible error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_IO_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The reassignment of ownership of the group is in progress.

</td>
</tr>
</table>

## -remarks

The return value from the  <b>MoveClusterGroup</b> function does not imply anything about the state of the group or any of its resources. The return value only indicates whether the change of ownership was successful. After returning from  <b>MoveClusterGroup</b>, the cluster always attempts to return the group to the state it was before the move.

If you want your application to ensure a particular state for a resource or a group after a move:

<ol>
<li>Check the state prior to the move. The cluster will attempt to restore that state after the move.</li>
<li>Poll for the state after the move and adjust as necessary. Or create a notification port (see  <a href="/previous-versions/windows/desktop/mscs/receiving-cluster-events">Receiving Cluster Events</a>) and wait for a <b>CLUSTER_CHANGE_GROUP_STATE</b> event.</li>
</ol>
When <i>hDestinationNode</i> is set to <b>NULL</b>,  <b>MoveClusterGroup</b> attempts to move the group to the best possible node. If there is no node available that can accept the group, the function fails.  <b>MoveClusterGroup</b> also fails if  <b>MoveClusterGroup</b> determines that the group cannot be brought online on the node identified by the <i>hDestinationNode</i> parameter.

Do not call  <b>MoveClusterGroup</b> from a resource DLL. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and can have additional destructive effects. For information on how LPC and RPC handles are created, see  <a href="/previous-versions/windows/desktop/mscs/using-object-handles">Using Object Handles</a> and  <a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclustergroup">OpenClusterGroup</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternode">OpenClusterNode</a>