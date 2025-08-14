---
UID: NF:clusapi.CreateClusterResource
title: CreateClusterResource function (clusapi.h)
description: Creates a resource in a cluster.
helpviewer_keywords: ["CLUSTER_RESOURCE_DEFAULT_MONITOR","CLUSTER_RESOURCE_SEPARATE_MONITOR","CreateClusterResource","CreateClusterResource function [Failover Cluster]","PCLUSAPI_CREATE_CLUSTER_RESOURCE","PCLUSAPI_CREATE_CLUSTER_RESOURCE function [Failover Cluster]","_wolf_createclusterresource","clusapi/CreateClusterResource","clusapi/PCLUSAPI_CREATE_CLUSTER_RESOURCE","mscs.createclusterresource"]
old-location: mscs\createclusterresource.htm
tech.root: MsCS
ms.assetid: c9fe8fa8-57d7-4866-8113-694dc44dae22
ms.date: 12/05/2018
ms.keywords: CLUSTER_RESOURCE_DEFAULT_MONITOR, CLUSTER_RESOURCE_SEPARATE_MONITOR, CreateClusterResource, CreateClusterResource function [Failover Cluster], PCLUSAPI_CREATE_CLUSTER_RESOURCE, PCLUSAPI_CREATE_CLUSTER_RESOURCE function [Failover Cluster], _wolf_createclusterresource, clusapi/CreateClusterResource, clusapi/PCLUSAPI_CREATE_CLUSTER_RESOURCE, mscs.createclusterresource
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
 - CreateClusterResource
 - clusapi/CreateClusterResource
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
 - CreateClusterResource
---

# CreateClusterResource function


## -description

Creates a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> in a 
    <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>. The <b>PCLUSAPI_CREATE_CLUSTER_RESOURCE</b> type defines a pointer to this function.

## -parameters

### -param hGroup [in]

Handle to the <a href="/previous-versions/windows/desktop/mscs/groups">group</a> that should receive the resource.

### -param lpszResourceName [in]

Pointer to a null-terminated Unicode string containing the name of the new resource. The specified name 
      must be unique within the cluster.

### -param lpszResourceType [in]

Pointer to the type of new resource. The specified type must be installed in the cluster.

### -param dwFlags [in]

Bitmask describing how the resource should be added to the cluster. The <i>dwFlags</i> 
      parameter can be set to one of the following values enumerated from the 
      <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_create_flags">CLUSTER_RESOURCE_CREATE_FLAGS</a> 
      enumeration.



#### CLUSTER_RESOURCE_DEFAULT_MONITOR (0)

The <a href="/previous-versions/windows/desktop/mscs/cluster-service">Cluster service</a> determines the 
        <a href="/previous-versions/windows/desktop/mscs/resource-monitor">Resource Monitor</a> to which the new resource will be 
        assigned.



#### CLUSTER_RESOURCE_SEPARATE_MONITOR (1)

Causes the Cluster service to create a separate Resource Monitor dedicated exclusively to the new 
        resource.

## -returns

If the operation succeeds, the function returns a resource handle.

If the operation fails, the function returns <b>NULL</b>. For more information about the 
       error, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Do not call <b>CreateClusterResource</b> from a 
    resource DLL. For more information, see 
    <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_create_flags">CLUSTER_RESOURCE_CREATE_FLAGS</a>



<a href="/previous-versions/windows/desktop/mscs/resource-management-functions">Cluster Resource Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-deleteclusterresource">DeleteClusterResource</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclustergroup">OpenClusterGroup</a>