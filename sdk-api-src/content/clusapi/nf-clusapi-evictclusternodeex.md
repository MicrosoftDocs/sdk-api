---
UID: NF:clusapi.EvictClusterNodeEx
title: EvictClusterNodeEx function (clusapi.h)
description: Evicts a node from the cluster and initiates cleanup operations on the node.
helpviewer_keywords: ["EvictClusterNodeEx","EvictClusterNodeEx function [Failover Cluster]","PCLUSAPI_EVICT_CLUSTER_NODE_EX","PCLUSAPI_EVICT_CLUSTER_NODE_EX function [Failover Cluster]","_wolf_evictclusternodeex","clusapi/EvictClusterNodeEx","clusapi/PCLUSAPI_EVICT_CLUSTER_NODE_EX","mscs.evictclusternodeex"]
old-location: mscs\evictclusternodeex.htm
tech.root: MsCS
ms.assetid: 7f7ba010-265e-40d5-a429-a776d164fa07
ms.date: 12/05/2018
ms.keywords: EvictClusterNodeEx, EvictClusterNodeEx function [Failover Cluster], PCLUSAPI_EVICT_CLUSTER_NODE_EX, PCLUSAPI_EVICT_CLUSTER_NODE_EX function [Failover Cluster], _wolf_evictclusternodeex, clusapi/EvictClusterNodeEx, clusapi/PCLUSAPI_EVICT_CLUSTER_NODE_EX, mscs.evictclusternodeex
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
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
 - EvictClusterNodeEx
 - clusapi/EvictClusterNodeEx
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
 - EvictClusterNodeEx
---

# EvictClusterNodeEx function


## -description

Evicts a 
    <a href="/previous-versions/windows/desktop/mscs/nodes">node</a> from the 
    <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> and initiates cleanup operations on the node. The <b>PCLUSAPI_EVICT_CLUSTER_NODE_EX</b> type defines a pointer to this function.

## -parameters

### -param hNode [in]

Handle to the node to remove from the cluster.

### -param dwTimeOut [in]

Specifies the number of milliseconds for the function to wait for cleanup operations to occur. The function 
      will return when the cleanup is complete or when the specified time elapses, whichever is sooner.

### -param phrCleanupStatus [out]

Pointer to an <b>HRESULT</b>   that describes the results of the cleanup operation.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
      <a href="/windows/desktop/Debug/system-error-codes">system error code</a>, including the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CLUSTER_EVICT_WITHOUT_CLEANUP</b></dt>
</dl>
</td>
<td width="60%">
The node was evicted but the cleanup operation returned a value other than S_OK.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-evictclusternode">EvictClusterNode</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternode">OpenClusterNode</a>