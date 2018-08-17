---
UID: NC:clusapi.PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM
title: PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM
author: windows-sdk-content
description: Opens an enumerator for iterating through a group's resources and/or the nodes that are included in its list of preferred owners.
old-location: mscs\clustergroupopenenum.htm
old-project: mscs
ms.assetid: d8f9eff0-1784-4b55-8603-c262d5c23f6c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CLUSTER_GROUP_ENUM_ALL, CLUSTER_GROUP_ENUM_CONTAINS, CLUSTER_GROUP_ENUM_NODES, PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM, PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM callback, PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM callback function [Failover Cluster], _wolf_clustergroupopenenum, clusapi/PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM, mscs.clustergroupopenenum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: clusapi.h
req.include-header: 
req.redist: 
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
 - PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM callback function


## -description


Opens an enumerator for iterating through a 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369645(v=VS.85).aspx">group's</a> <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resources</a> 
    and/or the <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">nodes</a> that are included in its list of preferred 
    owners. The <b>PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM</b> type defines a pointer to this function.


## -parameters




### -param hGroup [in]

A handle to the <a href="https://msdn.microsoft.com/en-us/library/Aa369645(v=VS.85).aspx">group</a> to be enumerated.


### -param dwType [in]

A bitmask that describes the <a href="https://msdn.microsoft.com/en-us/library/Aa369115(v=VS.85).aspx">cluster objects</a> to be 
       enumerated. The following are valid values of the 
       <a href="https://msdn.microsoft.com/en-us/library/Bb309149(v=VS.85).aspx">CLUSTER_GROUP_ENUM</a> enumeration.



#### CLUSTER_GROUP_ENUM_CONTAINS (1)

Enumerates the resources in the group.



#### CLUSTER_GROUP_ENUM_NODES (2)

Enumerates the nodes in the preferred owners list of the group.



#### CLUSTER_GROUP_ENUM_ALL (3)

Enumerates the resources in the group and the preferred owners of the group.


## -returns



If the operation succeeds, 
       <i>ClusterGroupOpenEnum</i> returns a handle to an 
       enumerator that can be passed to the 
       <a href="https://msdn.microsoft.com/fffcae88-8df0-487f-9f6d-bc3560283ef1">ClusterGroupEnum</a> function.

If the operation fails, the function returns <b>NULL</b>. For more information about the 
       error, call the function <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Do not call <i>ClusterGroupOpenEnum</i> from any 
     resource DLL entry point function. 
     <i>ClusterGroupOpenEnum</i> can safely be called from a 
     worker thread. For more information, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa369588(v=VS.85).aspx">Function Calls to Avoid in Resource DLLs</a>.


#### Examples

See <a href="https://msdn.microsoft.com/en-us/library/Aa369563(v=VS.85).aspx">Enumerating Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9bdab6b9-a54d-4166-988c-effdeb2ab254">ClusterGroupCloseEnum</a>



<a href="https://msdn.microsoft.com/fffcae88-8df0-487f-9f6d-bc3560283ef1">ClusterGroupEnum</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369686(v=VS.85).aspx">Group Management Functions</a>



<a href="https://msdn.microsoft.com/0c7ef9d9-d32b-448e-9e07-6befb9b3e338">OpenClusterGroup</a>
 

 

