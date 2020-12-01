---
UID: NF:clusapi.DeleteClusterResourceType
title: DeleteClusterResourceType function (clusapi.h)
description: Removes a resource type from a cluster.
helpviewer_keywords: ["DeleteClusterResourceType","DeleteClusterResourceType function [Failover Cluster]","PCLUSAPI_DELETE_CLUSTER_RESOURCE_TYPE","PCLUSAPI_DELETE_CLUSTER_RESOURCE_TYPE function [Failover Cluster]","_wolf_deleteclusterresourcetype","clusapi/DeleteClusterResourceType","clusapi/PCLUSAPI_DELETE_CLUSTER_RESOURCE_TYPE","mscs.deleteclusterresourcetype"]
old-location: mscs\deleteclusterresourcetype.htm
tech.root: MsCS
ms.assetid: 39615efe-e0fe-4e7b-b6f0-ba4a79d841a8
ms.date: 12/05/2018
ms.keywords: DeleteClusterResourceType, DeleteClusterResourceType function [Failover Cluster], PCLUSAPI_DELETE_CLUSTER_RESOURCE_TYPE, PCLUSAPI_DELETE_CLUSTER_RESOURCE_TYPE function [Failover Cluster], _wolf_deleteclusterresourcetype, clusapi/DeleteClusterResourceType, clusapi/PCLUSAPI_DELETE_CLUSTER_RESOURCE_TYPE, mscs.deleteclusterresourcetype
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
 - DeleteClusterResourceType
 - clusapi/DeleteClusterResourceType
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
 - DeleteClusterResourceType
---

# DeleteClusterResourceType function


## -description

Removes a  <a href="/previous-versions/windows/desktop/mscs/resource-types">resource type</a> from a <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>. The <b>PCLUSAPI_DELETE_CLUSTER_RESOURCE_TYPE</b> type defines a pointer to this function.

## -parameters

### -param hCluster [in]

Handle to the cluster containing the resource type to be removed.

### -param lpszResourceTypeName [in]

Pointer to a null-terminated Unicode string containing the name of the resource type to be removed.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

The  <b>DeleteClusterResourceType</b> function only removes the resource type with the name pointed to by <i>lpszResourceTypeName</i> from the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> and then unregisters it with the  <a href="/previous-versions/windows/desktop/mscs/cluster-service">Cluster service</a>. The caller must delete the  <a href="/previous-versions/windows/desktop/mscs/resource-dlls">resource DLL</a> for the resource type from each  <a href="/previous-versions/windows/desktop/mscs/nodes">node</a> in the cluster.

The caller must also delete any  <a href="/previous-versions/windows/desktop/mscs/resources">resources</a> of this type before calling  <b>DeleteClusterResourceType</b> to delete the type. If any resources of the specified type still exist when  <b>DeleteClusterResourceType</b> is called, the function fails.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-createclusterresourcetype">CreateClusterResourceType</a>