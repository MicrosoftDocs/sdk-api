---
UID: NF:clusapi.AddResourceToClusterSharedVolumes
title: AddResourceToClusterSharedVolumes function (clusapi.h)
description: Adds storage to Cluster Shared Volumes.
helpviewer_keywords: ["AddResourceToClusterSharedVolumes","AddResourceToClusterSharedVolumes function [Failover Cluster]","PCLUSAPI_ADD_RESOURCE_TO_CLUSTER_SHARED_VOLUMES","PCLUSAPI_ADD_RESOURCE_TO_CLUSTER_SHARED_VOLUMES function [Failover Cluster]","clusapi/AddResourceToClusterSharedVolumes","clusapi/PCLUSAPI_ADD_RESOURCE_TO_CLUSTER_SHARED_VOLUMES","mscs.addresourcetoclustersharedvolumes"]
old-location: mscs\addresourcetoclustersharedvolumes.htm
tech.root: MsCS
ms.assetid: 87C70280-5030-44b9-B949-7240BCA19C6B
ms.date: 12/05/2018
ms.keywords: AddResourceToClusterSharedVolumes, AddResourceToClusterSharedVolumes function [Failover Cluster], PCLUSAPI_ADD_RESOURCE_TO_CLUSTER_SHARED_VOLUMES, PCLUSAPI_ADD_RESOURCE_TO_CLUSTER_SHARED_VOLUMES function [Failover Cluster], clusapi/AddResourceToClusterSharedVolumes, clusapi/PCLUSAPI_ADD_RESOURCE_TO_CLUSTER_SHARED_VOLUMES, mscs.addresourcetoclustersharedvolumes
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
 - AddResourceToClusterSharedVolumes
 - clusapi/AddResourceToClusterSharedVolumes
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
 - Ext-MS-Win-Cluster-ClusAPI-L1-1-2.dll
api_name:
 - AddResourceToClusterSharedVolumes
---

# AddResourceToClusterSharedVolumes function


## -description

Adds storage to Cluster Shared Volumes. The 
    <b>PCLUSAPI_ADD_RESOURCE_TO_CLUSTER_SHARED_VOLUMES</b> type defines a pointer to this 
    function.

## -parameters

### -param hResource [in]

Handle to the physical disk resource to add to Cluster Shared Volumes.

## -returns

If the operation succeeds, it returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
       <b>AddResourceToClusterSharedVolumes</b> 
       returns one of the <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

## -remarks

The system crash dump path cannot reside on any cluster shared volumes that use BitLocker encryption.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-removeresourcefromclustersharedvolumes">RemoveResourceFromClusterSharedVolumes</a>