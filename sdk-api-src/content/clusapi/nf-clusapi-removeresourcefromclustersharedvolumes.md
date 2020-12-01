---
UID: NF:clusapi.RemoveResourceFromClusterSharedVolumes
title: RemoveResourceFromClusterSharedVolumes function (clusapi.h)
description: Removes storage from Cluster Shared Volumes.
helpviewer_keywords: ["PCLUSAPI_REMOVE_RESOURCE_FROM_CLUSTER_SHARED_VOLUMES","PCLUSAPI_REMOVE_RESOURCE_FROM_CLUSTER_SHARED_VOLUMES function [Failover Cluster]","RemoveResourceFromClusterSharedVolumes","RemoveResourceFromClusterSharedVolumes function [Failover Cluster]","clusapi/PCLUSAPI_REMOVE_RESOURCE_FROM_CLUSTER_SHARED_VOLUMES","clusapi/RemoveResourceFromClusterSharedVolumes","mscs.removeresourcefromclustersharedvolumes"]
old-location: mscs\removeresourcefromclustersharedvolumes.htm
tech.root: MsCS
ms.assetid: 696CBC0D-C1F6-4f1a-94D1-71F77B102258
ms.date: 12/05/2018
ms.keywords: PCLUSAPI_REMOVE_RESOURCE_FROM_CLUSTER_SHARED_VOLUMES, PCLUSAPI_REMOVE_RESOURCE_FROM_CLUSTER_SHARED_VOLUMES function [Failover Cluster], RemoveResourceFromClusterSharedVolumes, RemoveResourceFromClusterSharedVolumes function [Failover Cluster], clusapi/PCLUSAPI_REMOVE_RESOURCE_FROM_CLUSTER_SHARED_VOLUMES, clusapi/RemoveResourceFromClusterSharedVolumes, mscs.removeresourcefromclustersharedvolumes
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
 - RemoveResourceFromClusterSharedVolumes
 - clusapi/RemoveResourceFromClusterSharedVolumes
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
 - RemoveResourceFromClusterSharedVolumes
---

# RemoveResourceFromClusterSharedVolumes function


## -description

Removes storage from Cluster Shared Volumes. The 
    <b>PCLUSAPI_REMOVE_RESOURCE_FROM_CLUSTER_SHARED_VOLUMES</b> type defines a pointer to this 
    function.

## -parameters

### -param hResource [in]

Handle to the physical disk resource to remove from Cluster Shared Volumes.

## -returns

If the operation succeeds, it returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
       <b>RemoveResourceFromClusterSharedVolumes</b> 
       returns one of the <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-addresourcetoclustersharedvolumes">AddResourceToClusterSharedVolumes</a>