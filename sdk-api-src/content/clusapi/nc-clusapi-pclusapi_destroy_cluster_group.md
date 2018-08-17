---
UID: NC:clusapi.PCLUSAPI_DESTROY_CLUSTER_GROUP
title: PCLUSAPI_DESTROY_CLUSTER_GROUP
author: windows-sdk-content
description: Deletes the specified group from a cluster.
old-location: mscs\destroyclustergroup.htm
old-project: mscs
ms.assetid: ac293d5b-edc8-4c5f-9b05-9e2349bf1453
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PCLUSAPI_DESTROY_CLUSTER_GROUP, PCLUSAPI_DESTROY_CLUSTER_GROUP callback, PCLUSAPI_DESTROY_CLUSTER_GROUP callback function [Failover Cluster], clusapi/PCLUSAPI_DESTROY_CLUSTER_GROUP, mscs.destroyclustergroup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
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
 - PCLUSAPI_DESTROY_CLUSTER_GROUP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_DESTROY_CLUSTER_GROUP callback function


## -description


Deletes the specified <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a> from a 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369114(v=VS.85).aspx">cluster</a>. Unlike 
    <a href="https://msdn.microsoft.com/a0a8461c-8919-4620-83a2-bb8e5d03b0c4">DeleteClusterGroup</a> the group can contain resources 
    and it can be online. The <b>PCLUSAPI_DESTROY_CLUSTER_GROUP</b> type defines a pointer to this function.


## -parameters




### -param hGroup [in]

This parameter takes a handle to the cluster group to be destroyed.


## -returns



This function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>. If the 
       operation completes successfully the function returns <b>ERROR_SUCCESS</b> (0). Any other 
       returned system error code would indicate that the 
       operation failed.




## -remarks



The <b>PCLUSAPI_DESTROY_CLUSTER_GROUP</b> type defines a pointer to this function.

<i>DestroyClusterGroup</i> does not close the group 
     handle specified by the <i>hGroup</i> parameter. To avoid memory leaks, be sure to close this handle with 
     the <a href="https://msdn.microsoft.com/5bbacf45-2e1a-402a-8592-c8f60034c4ad">CloseClusterGroup</a> function.

Do not call <i>DestroyClusterGroup</i> from a resource 
     DLL. For more information, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa369588(v=VS.85).aspx">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/5bbacf45-2e1a-402a-8592-c8f60034c4ad">CloseClusterGroup</a>



<a href="https://msdn.microsoft.com/a0a8461c-8919-4620-83a2-bb8e5d03b0c4">DeleteClusterGroup</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369686(v=VS.85).aspx">Group Management Functions</a>
 

 

