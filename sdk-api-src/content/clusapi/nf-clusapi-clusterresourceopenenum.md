---
UID: NF:clusapi.ClusterResourceOpenEnum
title: ClusterResourceOpenEnum function (clusapi.h)
description: Opens an enumerator for iterating through a resource's dependencies and nodes.
helpviewer_keywords: ["CLUSTER_RESOURCE_ENUM_DEPENDS","CLUSTER_RESOURCE_ENUM_NODES","CLUSTER_RESOURCE_ENUM_PROVIDES","ClusterResourceOpenEnum","ClusterResourceOpenEnum function [Failover Cluster]","PCLUSAPI_CLUSTER_RESOURCE_OPEN_ENUM","PCLUSAPI_CLUSTER_RESOURCE_OPEN_ENUM function [Failover Cluster]","_wolf_clusterresourceopenenum","clusapi/ClusterResourceOpenEnum","clusapi/PCLUSAPI_CLUSTER_RESOURCE_OPEN_ENUM","mscs.clusterresourceopenenum"]
old-location: mscs\clusterresourceopenenum.htm
tech.root: MsCS
ms.assetid: f801401f-f49d-41de-b88b-b832330eeccf
ms.date: 12/05/2018
ms.keywords: CLUSTER_RESOURCE_ENUM_DEPENDS, CLUSTER_RESOURCE_ENUM_NODES, CLUSTER_RESOURCE_ENUM_PROVIDES, ClusterResourceOpenEnum, ClusterResourceOpenEnum function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_OPEN_ENUM, PCLUSAPI_CLUSTER_RESOURCE_OPEN_ENUM function [Failover Cluster], _wolf_clusterresourceopenenum, clusapi/ClusterResourceOpenEnum, clusapi/PCLUSAPI_CLUSTER_RESOURCE_OPEN_ENUM, mscs.clusterresourceopenenum
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
 - ClusterResourceOpenEnum
 - clusapi/ClusterResourceOpenEnum
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
 - Ext-MS-Win-Cluster-ClusAPI-L1-1-2.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
 - ClusterResourceOpenEnum
---

# ClusterResourceOpenEnum function


## -description

Opens an enumerator for iterating through a 
    <a href="/previous-versions/windows/desktop/mscs/resources">resource's</a>
<a href="/previous-versions/windows/desktop/mscs/resource-dependencies">dependencies</a> and 
    <a href="/previous-versions/windows/desktop/mscs/nodes">nodes</a>. The <b>PCLUSAPI_CLUSTER_RESOURCE_OPEN_ENUM</b> type defines a pointer to this function.

## -parameters

### -param hResource [in]

A handle to a resource.

### -param dwType [in]

A bitmask that describes the type of <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster objects</a> 
       to be enumerated.


The following values of the 
        <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_enum">CLUSTER_RESOURCE_ENUM</a> enumeration are valid.





#### CLUSTER_RESOURCE_ENUM_DEPENDS (1)

The object is a resource that the resource identified by the <i>hResource</i> parameter 
         directly depends on.



#### CLUSTER_RESOURCE_ENUM_PROVIDES (2)

The object is a resource that depends on the resource identified by <i>hResource</i>.



#### CLUSTER_RESOURCE_ENUM_NODES (4)

The object is a node that can host the resource identified by <i>hResource</i>.

## -returns

If the operation succeeds, the function returns an enumeration handle.

If the operation fails, the function returns <b>NULL</b>. For more information about the 
       error, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

Do not call <b>ClusterResourceOpenEnum</b> from 
     any resource DLL entry point function. 
     <b>ClusterResourceOpenEnum</b> can safely be called 
     from a worker thread. For more information, see 
     <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.


#### Examples

See <a href="/previous-versions/windows/desktop/mscs/enumerating-objects">Enumerating Objects</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-management-functions">Cluster Resource Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecloseenum">ClusterResourceCloseEnum</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceenum">ClusterResourceEnum</a>