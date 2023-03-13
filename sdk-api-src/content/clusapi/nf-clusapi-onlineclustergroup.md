---
UID: NF:clusapi.OnlineClusterGroup
title: OnlineClusterGroup function (clusapi.h)
description: Brings a group online. (OnlineClusterGroup)
helpviewer_keywords: ["OnlineClusterGroup","OnlineClusterGroup function [Failover Cluster]","PCLUSAPI_ONLINE_CLUSTER_GROUP","PCLUSAPI_ONLINE_CLUSTER_GROUP function [Failover Cluster]","_wolf_onlineclustergroup","clusapi/OnlineClusterGroup","clusapi/PCLUSAPI_ONLINE_CLUSTER_GROUP","mscs.onlineclustergroup"]
old-location: mscs\onlineclustergroup.htm
tech.root: MsCS
ms.assetid: 33b4f435-f394-41fc-846f-8e9206c76aa1
ms.date: 12/05/2018
ms.keywords: OnlineClusterGroup, OnlineClusterGroup function [Failover Cluster], PCLUSAPI_ONLINE_CLUSTER_GROUP, PCLUSAPI_ONLINE_CLUSTER_GROUP function [Failover Cluster], _wolf_onlineclustergroup, clusapi/OnlineClusterGroup, clusapi/PCLUSAPI_ONLINE_CLUSTER_GROUP, mscs.onlineclustergroup
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
 - OnlineClusterGroup
 - clusapi/OnlineClusterGroup
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
 - OnlineClusterGroup
---

# OnlineClusterGroup function


## -description

Brings a  <a href="/previous-versions/windows/desktop/mscs/groups">group</a> online. The <b>PCLUSAPI_ONLINE_CLUSTER_GROUP</b> type defines a pointer to this function.

## -parameters

### -param hGroup [in]

Handle to the group to be brought online.

### -param hDestinationNode [in, optional]

Handle to the  <a href="/previous-versions/windows/desktop/mscs/nodes">node</a> where the group identified by <i>hGroup</i> should be brought online or <b>NULL</b>.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following are possible error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_HOST_NODE_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
A suitable host node was not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_IO_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The operation is in progress.

</td>
</tr>
</table>

## -remarks

If the group cannot be brought online on the node identified by the <i>hDestinationNode</i> parameter, the  <b>OnlineClusterGroup</b> function fails.

If the <i>hDestinationNode</i> parameter is set to <b>NULL</b>,  <b>OnlineClusterGroup</b> brings the group online on the current node.

Do not call  <b>OnlineClusterGroup</b> from a resource DLL. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and can have additional destructive effects. For information on how LPC and RPC handles are created, see  <a href="/previous-versions/windows/desktop/mscs/using-object-handles">Using Object Handles</a> and  <a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-offlineclustergroup">OfflineClusterGroup</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclustergroup">OpenClusterGroup</a>
