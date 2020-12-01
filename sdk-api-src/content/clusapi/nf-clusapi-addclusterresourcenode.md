---
UID: NF:clusapi.AddClusterResourceNode
title: AddClusterResourceNode function (clusapi.h)
description: Adds a node to the list of possible nodes that a resource can run on.
helpviewer_keywords: ["AddClusterResourceNode","AddClusterResourceNode function [Failover Cluster]","PCLUSAPI_ADD_CLUSTER_RESOURCE_NODE","PCLUSAPI_ADD_CLUSTER_RESOURCE_NODE function [Failover Cluster]","_wolf_addclusterresourcenode","clusapi/AddClusterResourceNode","clusapi/PCLUSAPI_ADD_CLUSTER_RESOURCE_NODE","mscs.addclusterresourcenode"]
old-location: mscs\addclusterresourcenode.htm
tech.root: MsCS
ms.assetid: d87f9541-7cc6-4dbb-8f1f-e8e36462b01b
ms.date: 12/05/2018
ms.keywords: AddClusterResourceNode, AddClusterResourceNode function [Failover Cluster], PCLUSAPI_ADD_CLUSTER_RESOURCE_NODE, PCLUSAPI_ADD_CLUSTER_RESOURCE_NODE function [Failover Cluster], _wolf_addclusterresourcenode, clusapi/AddClusterResourceNode, clusapi/PCLUSAPI_ADD_CLUSTER_RESOURCE_NODE, mscs.addclusterresourcenode
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
 - AddClusterResourceNode
 - clusapi/AddClusterResourceNode
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
 - AddClusterResourceNode
---

# AddClusterResourceNode function


## -description

Adds a <a href="/previous-versions/windows/desktop/mscs/nodes">node</a> to the list of possible nodes that a 
    <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> can run on. The 
    <b>PCLUSAPI_ADD_CLUSTER_RESOURCE_NODE</b> type defines a pointer to this function.

## -parameters

### -param hResource [in]

Handle to a resource that will add a node to its possible owners list.

### -param hNode [in]

Handle to the node to be added to the list of potential host nodes belonging to the resource identified by 
      <i>hResource</i>.

## -returns

If the operation succeeds, it returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
       <b>AddClusterResourceNode</b> returns one of the 
       <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

## -remarks

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
    can have additional destructive effects. For information on how LPC and RPC handles are created, see 
    <a href="/previous-versions/windows/desktop/mscs/using-object-handles">Using Object Handles</a> and 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternode">OpenClusterNode</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterresource">OpenClusterResource</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-removeclusterresourcenode">RemoveClusterResourceNode</a>