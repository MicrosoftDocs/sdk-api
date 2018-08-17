---
UID: NC:clusapi.PCLUSAPI_CREATE_CLUSTER_RESOURCE
title: PCLUSAPI_CREATE_CLUSTER_RESOURCE
author: windows-sdk-content
description: Creates a resource in a cluster.
old-location: mscs\createclusterresource.htm
old-project: mscs
ms.assetid: c9fe8fa8-57d7-4866-8113-694dc44dae22
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: CLUSTER_RESOURCE_DEFAULT_MONITOR, CLUSTER_RESOURCE_SEPARATE_MONITOR, PCLUSAPI_CREATE_CLUSTER_RESOURCE, PCLUSAPI_CREATE_CLUSTER_RESOURCE callback, PCLUSAPI_CREATE_CLUSTER_RESOURCE callback function [Failover Cluster], _wolf_createclusterresource, clusapi/PCLUSAPI_CREATE_CLUSTER_RESOURCE, mscs.createclusterresource
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
 - PCLUSAPI_CREATE_CLUSTER_RESOURCE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CREATE_CLUSTER_RESOURCE callback function


## -description


Creates a <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a> in a 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369114(v=VS.85).aspx">cluster</a>. The <b>PCLUSAPI_CREATE_CLUSTER_RESOURCE</b> type defines a pointer to this function.


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
      <a href="https://msdn.microsoft.com/en-us/library/Bb309165(v=VS.85).aspx">CLUSTER_RESOURCE_CREATE_FLAGS</a> 
      enumeration.



#### CLUSTER_RESOURCE_DEFAULT_MONITOR (0)

The <a href="https://msdn.microsoft.com/en-us/library/Aa369163(v=VS.85).aspx">Cluster service</a> determines the 
        <a href="https://msdn.microsoft.com/en-us/library/Aa372266(v=VS.85).aspx">Resource Monitor</a> to which the new resource will be 
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
    <a href="https://msdn.microsoft.com/en-us/library/Aa369588(v=VS.85).aspx">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb309165(v=VS.85).aspx">CLUSTER_RESOURCE_CREATE_FLAGS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa372262(v=VS.85).aspx">Cluster Resource Management Functions</a>



<a href="https://msdn.microsoft.com/d6a8425c-c926-46d8-b13a-c293f8ed30a8">DeleteClusterResource</a>



<a href="https://msdn.microsoft.com/0c7ef9d9-d32b-448e-9e07-6befb9b3e338">OpenClusterGroup</a>
 

 

