---
UID: NC:clusapi.PCLUSAPI_ADD_RESOURCE_TO_CLUSTER_SHARED_VOLUMES
title: PCLUSAPI_ADD_RESOURCE_TO_CLUSTER_SHARED_VOLUMES
author: windows-sdk-content
description: Adds storage to Cluster Shared Volumes.
old-location: mscs\addresourcetoclustersharedvolumes.htm
old-project: mscs
ms.assetid: 87C70280-5030-44b9-B949-7240BCA19C6B
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PCLUSAPI_ADD_RESOURCE_TO_CLUSTER_SHARED_VOLUMES, PCLUSAPI_ADD_RESOURCE_TO_CLUSTER_SHARED_VOLUMES callback, PCLUSAPI_ADD_RESOURCE_TO_CLUSTER_SHARED_VOLUMES callback function [Failover Cluster], clusapi/PCLUSAPI_ADD_RESOURCE_TO_CLUSTER_SHARED_VOLUMES, mscs.addresourcetoclustersharedvolumes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ClusAPI.h
api_name:
 - PCLUSAPI_ADD_RESOURCE_TO_CLUSTER_SHARED_VOLUMES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_ADD_RESOURCE_TO_CLUSTER_SHARED_VOLUMES callback function


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
       <i>AddResourceToClusterSharedVolumes</i> 
       returns one of the <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error codes</a>.




## -remarks



The system crash dump path cannot reside on any cluster shared volumes that use BitLocker encryption.




## -see-also




<a href="https://msdn.microsoft.com/696CBC0D-C1F6-4f1a-94D1-71F77B102258">RemoveResourceFromClusterSharedVolumes</a>
 

 

