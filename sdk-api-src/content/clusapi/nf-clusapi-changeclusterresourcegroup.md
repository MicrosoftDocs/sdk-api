---
UID: NF:clusapi.ChangeClusterResourceGroup
title: ChangeClusterResourceGroup function (clusapi.h)
description: Moves a resource from one group to another.
helpviewer_keywords: ["ChangeClusterResourceGroup","ChangeClusterResourceGroup function [Failover Cluster]","PCLUSAPI_CHANGE_CLUSTER_RESOURCE_GROUP","PCLUSAPI_CHANGE_CLUSTER_RESOURCE_GROUP function [Failover Cluster]","_wolf_changeclusterresourcegroup","clusapi/ChangeClusterResourceGroup","clusapi/PCLUSAPI_CHANGE_CLUSTER_RESOURCE_GROUP","mscs.changeclusterresourcegroup"]
old-location: mscs\changeclusterresourcegroup.htm
tech.root: MsCS
ms.assetid: 99720615-ad5d-4d9a-a6ae-8ba1cd2499f2
ms.date: 12/05/2018
ms.keywords: ChangeClusterResourceGroup, ChangeClusterResourceGroup function [Failover Cluster], PCLUSAPI_CHANGE_CLUSTER_RESOURCE_GROUP, PCLUSAPI_CHANGE_CLUSTER_RESOURCE_GROUP function [Failover Cluster], _wolf_changeclusterresourcegroup, clusapi/ChangeClusterResourceGroup, clusapi/PCLUSAPI_CHANGE_CLUSTER_RESOURCE_GROUP, mscs.changeclusterresourcegroup
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
 - ChangeClusterResourceGroup
 - clusapi/ChangeClusterResourceGroup
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
 - ChangeClusterResourceGroup
---

# ChangeClusterResourceGroup function


## -description

Moves a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> from one 
    <a href="/previous-versions/windows/desktop/mscs/groups">group</a> to another. The 
    <b>PCLUSAPI_CHANGE_CLUSTER_RESOURCE_GROUP</b> type defines a pointer to this function.

## -parameters

### -param hResource [in]

Handle of the resource to be moved.

### -param hGroup [in]

Handle of the group that should receive the resource identified by 
      <i>hResource</i>.

## -returns

If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, it returns one of the 
       <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

## -remarks

With the <b>ChangeClusterResourceGroup</b> 
    function, both the group that a resource currently belongs to and its new group must be owned by the same 
    <a href="/previous-versions/windows/desktop/mscs/nodes">node</a> regardless of the resource's state.

Do not call <b>ChangeClusterResourceGroup</b> 
    from a resource DLL. For more information, see 
    <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>. 
    If the resource identified by <i>hResource</i> has 
    <a href="/previous-versions/windows/desktop/mscs/resource-dependencies">dependencies</a>, all of the resources in its dependency 
    tree are moved to the group identified by <i>hGroup</i>. For example, in the situation shown 
    in the following diagram, changing resource B to group 2 will move the entire dependency tree (resources A, X, and 
    Y) .

:::image type="content" source="./images/resmove.png" border="false" alt-text="Diagram showing the tree of dependencies between resources in a Cluster Resource Group, before and after a resource is moved to another group.":::

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
    can have additional destructive effects. For information on how LPC and RPC handles are created, see 
    <a href="/previous-versions/windows/desktop/mscs/using-object-handles">Using Object Handles</a> and 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclustergroup">OpenClusterGroup</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterresource">OpenClusterResource</a>