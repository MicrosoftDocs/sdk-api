---
UID: NF:clusapi.EvictClusterNode
title: EvictClusterNode function (clusapi.h)
description: Deletes a node from the cluster database.
helpviewer_keywords: ["EvictClusterNode","EvictClusterNode function [Failover Cluster]","PCLUSAPI_EVICT_CLUSTER_NODE","PCLUSAPI_EVICT_CLUSTER_NODE function [Failover Cluster]","_wolf_evictclusternode","clusapi/EvictClusterNode","clusapi/PCLUSAPI_EVICT_CLUSTER_NODE","mscs.evictclusternode"]
old-location: mscs\evictclusternode.htm
tech.root: MsCS
ms.assetid: 0353b640-5fa6-4e83-a7e5-1b4bd2ca16d9
ms.date: 12/05/2018
ms.keywords: EvictClusterNode, EvictClusterNode function [Failover Cluster], PCLUSAPI_EVICT_CLUSTER_NODE, PCLUSAPI_EVICT_CLUSTER_NODE function [Failover Cluster], _wolf_evictclusternode, clusapi/EvictClusterNode, clusapi/PCLUSAPI_EVICT_CLUSTER_NODE, mscs.evictclusternode
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
 - EvictClusterNode
 - clusapi/EvictClusterNode
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
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - EvictClusterNode
---

# EvictClusterNode function


## -description

Deletes a  <a href="/previous-versions/windows/desktop/mscs/nodes">node</a> from the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a>. The <b>PCLUSAPI_EVICT_CLUSTER_NODE</b> type defines a pointer to this function.

## -parameters

### -param hNode [in]

Handle to the node to delete.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

To reinstate an evicted node, you must first remove the  <a href="/previous-versions/windows/desktop/mscs/cluster-service">Cluster service</a> from the node and then reinstall it. During installation, choose the <b>Join an Existing Cluster</b> option.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternode">OpenClusterNode</a>