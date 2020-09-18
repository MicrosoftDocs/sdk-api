---
UID: NF:clusapi.CreateClusterResourceType
title: CreateClusterResourceType function (clusapi.h)
description: Creates a resource type in a cluster.
helpviewer_keywords: ["CreateClusterResourceType","CreateClusterResourceType function [Failover Cluster]","PCLUSAPI_CREATE_CLUSTER_RESOURCE_TYPE","PCLUSAPI_CREATE_CLUSTER_RESOURCE_TYPE function [Failover Cluster]","_wolf_createclusterresourcetype","clusapi/CreateClusterResourceType","clusapi/PCLUSAPI_CREATE_CLUSTER_RESOURCE_TYPE","mscs.createclusterresourcetype"]
old-location: mscs\createclusterresourcetype.htm
tech.root: MsCS
ms.assetid: 19b8e8cf-898c-4df5-959c-e3789b082a76
ms.date: 12/05/2018
ms.keywords: CreateClusterResourceType, CreateClusterResourceType function [Failover Cluster], PCLUSAPI_CREATE_CLUSTER_RESOURCE_TYPE, PCLUSAPI_CREATE_CLUSTER_RESOURCE_TYPE function [Failover Cluster], _wolf_createclusterresourcetype, clusapi/CreateClusterResourceType, clusapi/PCLUSAPI_CREATE_CLUSTER_RESOURCE_TYPE, mscs.createclusterresourcetype
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
 - CreateClusterResourceType
 - clusapi/CreateClusterResourceType
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
 - CreateClusterResourceType
---

# CreateClusterResourceType function


## -description

Creates a <a href="/previous-versions/windows/desktop/mscs/resource-types">resource type</a> in a <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>. The <b>PCLUSAPI_CREATE_CLUSTER_RESOURCE_TYPE</b> type defines a pointer to this function.

## -parameters

### -param hCluster [in]

Handle to the cluster to receive the new resource type.

### -param lpszResourceTypeName [in]

Pointer to a null-terminated Unicode string containing the name of the new resource type. The specified name must be unique within the cluster.

### -param lpszDisplayName [in]

Pointer to the  <a href="/previous-versions/windows/desktop/mscs/display-names">display name</a> for the new resource type. While the content of <i>lpszResourceTypeName</i> should uniquely identify the resource type on all clusters, the content of <i>lpszDisplayName</i> should be a localized friendly name for the resource suitable for displaying to administrators.

### -param lpszResourceTypeDll [in]

Pointer to the fully qualified name of the  <a href="/previous-versions/windows/desktop/mscs/resource-dlls">resource DLL</a> for the new resource type or the path name relative to the Cluster directory.

### -param dwLooksAlivePollInterval [in]

Default millisecond value to be used as the poll interval needed by the new resource type's  <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-plooks_alive_routine">LooksAlive</a> function. The <i>dwLooksAlivePollInterval</i> parameter is used to set the resource type's  <a href="/previous-versions/windows/desktop/mscs/resource-types-looksalivepollinterval">LooksAlivePollInterval</a> property.

### -param dwIsAlivePollInterval [in]

Default millisecond value to be used as the poll interval needed by the new resource type's  <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pis_alive_routine">IsAlive</a> function. The <i>dwIsAlivePollInterval</i> parameter is used to set the resource type's  <a href="/previous-versions/windows/desktop/mscs/resource-types-isalivepollinterval">IsAlivePollInterval</a> property.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

The  <b>CreateClusterResourceType</b> function only defines the resource type in the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> and registers the resource type with the  <a href="/previous-versions/windows/desktop/mscs/cluster-service">Cluster service</a>. To complete the process of installing a new resource type in a cluster, developers must install the resource DLLs and  <a href="/previous-versions/windows/desktop/mscs/cluster-administrator">Cluster Administrator</a> extension DLLs for the new types on each  <a href="/previous-versions/windows/desktop/mscs/nodes">node</a> in the cluster. Also, if Cluster Administrator will be used on systems that are not member nodes, the extension DLLs must also be installed on those systems.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-deleteclusterresourcetype">DeleteClusterResourceType</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pis_alive_routine">IsAlive</a>



<a href="/previous-versions/windows/desktop/mscs/resource-types-isalivepollinterval">IsAlivePollInterval</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-plooks_alive_routine">LooksAlive</a>



<a href="/previous-versions/windows/desktop/mscs/resource-types-looksalivepollinterval">LooksAlivePollInterval</a>