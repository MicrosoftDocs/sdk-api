---
UID: NF:clusapi.RemoveResourceFromClusterSharedVolumes
title: RemoveResourceFromClusterSharedVolumes function (clusapi.h)
author: windows-sdk-content
description: Removes storage from Cluster Shared Volumes.
old-location: mscs\removeresourcefromclustersharedvolumes.htm
tech.root: MsCS
ms.assetid: 696CBC0D-C1F6-4f1a-94D1-71F77B102258
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PCLUSAPI_REMOVE_RESOURCE_FROM_CLUSTER_SHARED_VOLUMES, PCLUSAPI_REMOVE_RESOURCE_FROM_CLUSTER_SHARED_VOLUMES function [Failover Cluster], RemoveResourceFromClusterSharedVolumes, RemoveResourceFromClusterSharedVolumes function [Failover Cluster], clusapi/PCLUSAPI_REMOVE_RESOURCE_FROM_CLUSTER_SHARED_VOLUMES, clusapi/RemoveResourceFromClusterSharedVolumes, mscs.removeresourcefromclustersharedvolumes
ms.topic: function
f1_keywords: 
 - "clusapi/RemoveResourceFromClusterSharedVolumes"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - RemoveResourceFromClusterSharedVolumes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
       returns one of the <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-addresourcetoclustersharedvolumes">AddResourceToClusterSharedVolumes</a>
 

 

