---
UID: NF:clusapi.RemoveClusterResourceNode
title: RemoveClusterResourceNode function (clusapi.h)
description: Removes a node from the list of nodes that can host a resource.
helpviewer_keywords: ["PCLUSAPI_REMOVE_CLUSTER_RESOURCE_NODE","PCLUSAPI_REMOVE_CLUSTER_RESOURCE_NODE function [Failover Cluster]","RemoveClusterResourceNode","RemoveClusterResourceNode function [Failover Cluster]","_wolf_removeclusterresourcenode","clusapi/PCLUSAPI_REMOVE_CLUSTER_RESOURCE_NODE","clusapi/RemoveClusterResourceNode","mscs.removeclusterresourcenode"]
old-location: mscs\removeclusterresourcenode.htm
tech.root: MsCS
ms.assetid: 1a5b59b9-5c19-4920-b150-b0b404629fb3
ms.date: 12/05/2018
ms.keywords: PCLUSAPI_REMOVE_CLUSTER_RESOURCE_NODE, PCLUSAPI_REMOVE_CLUSTER_RESOURCE_NODE function [Failover Cluster], RemoveClusterResourceNode, RemoveClusterResourceNode function [Failover Cluster], _wolf_removeclusterresourcenode, clusapi/PCLUSAPI_REMOVE_CLUSTER_RESOURCE_NODE, clusapi/RemoveClusterResourceNode, mscs.removeclusterresourcenode
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
 - RemoveClusterResourceNode
 - clusapi/RemoveClusterResourceNode
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
 - RemoveClusterResourceNode
---

# RemoveClusterResourceNode function


## -description

Removes a  <a href="/previous-versions/windows/desktop/mscs/nodes">node</a> from the list of nodes that can host a  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>. The <b>PCLUSAPI_REMOVE_CLUSTER_RESOURCE_NODE</b> type defines a pointer to this function.

## -parameters

### -param hResource [in]

Handle to the target resource.

### -param hNode [in]

Handle to the node that should be removed from the list of potential host nodes belonging to the resource identified by <i>hResource</i>.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

Do not call  <b>RemoveClusterResourceNode</b> from a resource DLL. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and can have additional destructive effects. For information on how LPC and RPC handles are created, see  <a href="/previous-versions/windows/desktop/mscs/using-object-handles">Using Object Handles</a> and  <a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-addclusterresourcenode">AddClusterResourceNode</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternode">OpenClusterNode</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterresource">OpenClusterResource</a>