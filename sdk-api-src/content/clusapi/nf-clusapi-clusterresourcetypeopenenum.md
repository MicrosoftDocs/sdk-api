---
UID: NF:clusapi.ClusterResourceTypeOpenEnum
title: ClusterResourceTypeOpenEnum function (clusapi.h)
description: Opens an enumerator for iterating through a resource type's possible owner nodes or resources.
helpviewer_keywords: ["CLUSTER_RESOURCE_TYPE_ENUM_ALL","CLUSTER_RESOURCE_TYPE_ENUM_NODES","CLUSTER_RESOURCE_TYPE_ENUM_RESOURCES","ClusterResourceTypeOpenEnum","ClusterResourceTypeOpenEnum function [Failover Cluster]","PCLUSAPI_CLUSTER_RESOURCE_TYPE_OPEN_ENUM","PCLUSAPI_CLUSTER_RESOURCE_TYPE_OPEN_ENUM function [Failover Cluster]","_wolf_clusterresourcetypeopenenum","clusapi/ClusterResourceTypeOpenEnum","clusapi/PCLUSAPI_CLUSTER_RESOURCE_TYPE_OPEN_ENUM","mscs.clusterresourcetypeopenenum"]
old-location: mscs\clusterresourcetypeopenenum.htm
tech.root: MsCS
ms.assetid: fa05875a-26c7-401d-ae81-1d204bfd7df1
ms.date: 12/05/2018
ms.keywords: CLUSTER_RESOURCE_TYPE_ENUM_ALL, CLUSTER_RESOURCE_TYPE_ENUM_NODES, CLUSTER_RESOURCE_TYPE_ENUM_RESOURCES, ClusterResourceTypeOpenEnum, ClusterResourceTypeOpenEnum function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_TYPE_OPEN_ENUM, PCLUSAPI_CLUSTER_RESOURCE_TYPE_OPEN_ENUM function [Failover Cluster], _wolf_clusterresourcetypeopenenum, clusapi/ClusterResourceTypeOpenEnum, clusapi/PCLUSAPI_CLUSTER_RESOURCE_TYPE_OPEN_ENUM, mscs.clusterresourcetypeopenenum
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
 - ClusterResourceTypeOpenEnum
 - clusapi/ClusterResourceTypeOpenEnum
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
 - ClusterResourceTypeOpenEnum
---

# ClusterResourceTypeOpenEnum function


## -description

Opens an enumerator for iterating through a <a href="/previous-versions/windows/desktop/mscs/resource-types">resource type's</a> 
    possible owner <a href="/previous-versions/windows/desktop/mscs/nodes">nodes</a> or resources. The <b>PCLUSAPI_CLUSTER_RESOURCE_TYPE_OPEN_ENUM</b> type defines a pointer to this function.

## -parameters

### -param hCluster [in]

<a href="/previous-versions/windows/desktop/mscs/c-gly">Cluster</a> handle.

### -param lpszResourceTypeName [in]

A null-terminated Unicode string containing the name of the resource type.

### -param dwType [in]

Bitmask describing the type of <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster objects</a> to be 
       enumerated. The following values of the <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_type_enum">CLUSTER_RESOURCE_TYPE_ENUM</a> enumeration are valid.



#### CLUSTER_RESOURCE_TYPE_ENUM_NODES (1)

The object is a node that can be a possible owner of the resource type.



#### CLUSTER_RESOURCE_TYPE_ENUM_RESOURCES (2)

The object is a resource that is an instance of the resource type.



#### CLUSTER_RESOURCE_TYPE_ENUM_ALL (3)

Enumerate both nodes and resources.

## -returns

If the operation succeeds, the function returns an enumeration handle which can be used in subsequent calls 
       to <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypeenum">ClusterResourceTypeEnum</a>.

If the operation fails, the function returns <b>NULL</b>. For more information about the 
      error, call the function <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_type_enum">CLUSTER_RESOURCE_TYPE_ENUM</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypecloseenum">ClusterResourceTypeCloseEnum</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypeenum">ClusterResourceTypeEnum</a>



<a href="/previous-versions/windows/desktop/mscs/resource-type-management-functions">Resource Type Management Functions</a>