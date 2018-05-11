---
UID: NC:clusapi.PCLUSAPI_CREATE_CLUSTER_RESOURCE
title: PCLUSAPI_CREATE_CLUSTER_RESOURCE
author: windows-driver-content
description: Creates a resource in a cluster.
old-location: mscs\createclusterresource.htm
old-project: MsCS
ms.assetid: c9fe8fa8-57d7-4866-8113-694dc44dae22
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: CLUSTER_RESOURCE_DEFAULT_MONITOR, CLUSTER_RESOURCE_SEPARATE_MONITOR, PCLUSAPI_CREATE_CLUSTER_RESOURCE, PCLUSAPI_CREATE_CLUSTER_RESOURCE callback, PCLUSAPI_CREATE_CLUSTER_RESOURCE callback function [Failover Cluster], _wolf_createclusterresource, clusapi/PCLUSAPI_CREATE_CLUSTER_RESOURCE, mscs.createclusterresource
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_CREATE_CLUSTER_RESOURCE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CREATE_CLUSTER_RESOURCE callback function


## -description


Creates a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> in a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>. The <b>PCLUSAPI_CREATE_CLUSTER_RESOURCE</b> type defines a pointer to this function.


## -parameters




### -param hGroup [in]

Handle to the <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a> that should receive the resource.


### -param lpszResourceName [in]

Pointer to a null-terminated Unicode string containing the name of the new resource. The specified name 
      must be unique within the cluster.


### -param lpszResourceType [in]

Pointer to the type of new resource. The specified type must be installed in the cluster.


### -param dwFlags [in]

Bitmask describing how the resource should be added to the cluster. The <i>dwFlags</i> 
      parameter can be set to one of the following values enumerated from the 
      <a href="https://msdn.microsoft.com/16f5ab58-2507-431a-98f9-bd00a24485ba">CLUSTER_RESOURCE_CREATE_FLAGS</a> 
      enumeration.



#### CLUSTER_RESOURCE_DEFAULT_MONITOR (0)

The <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a> determines the 
        <a href="https://msdn.microsoft.com/caebb47f-c2c5-463e-a957-d9eefc7fc33d">Resource Monitor</a> to which the new resource will be 
        assigned.



#### CLUSTER_RESOURCE_SEPARATE_MONITOR (1)

Causes the Cluster service to create a separate Resource Monitor dedicated exclusively to the new 
        resource.


## -returns



If the operation succeeds, the function returns a resource handle.

If the operation fails, the function returns <b>NULL</b>. For more information about the 
       error, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Do not call <i>CreateClusterResource</i> from a 
    resource DLL. For more information, see 
    <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/16f5ab58-2507-431a-98f9-bd00a24485ba">CLUSTER_RESOURCE_CREATE_FLAGS</a>



<a href="https://msdn.microsoft.com/d1f7360d-f592-49fb-b3b4-60d93afd7c6f">Cluster Resource Management Functions</a>



<a href="https://msdn.microsoft.com/d6a8425c-c926-46d8-b13a-c293f8ed30a8">DeleteClusterResource</a>



<a href="https://msdn.microsoft.com/0c7ef9d9-d32b-448e-9e07-6befb9b3e338">OpenClusterGroup</a>
 

 

