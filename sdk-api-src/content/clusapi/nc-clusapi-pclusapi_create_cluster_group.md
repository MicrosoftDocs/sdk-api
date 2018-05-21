---
UID: NC:clusapi.PCLUSAPI_CREATE_CLUSTER_GROUP
title: PCLUSAPI_CREATE_CLUSTER_GROUP
author: windows-driver-content
description: Adds a group to a cluster and returns a handle to the newly added group.
old-location: mscs\createclustergroup.htm
old-project: MsCS
ms.assetid: 7011640e-87d0-4f2b-971c-9e86c77db13e
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: PCLUSAPI_CREATE_CLUSTER_GROUP, PCLUSAPI_CREATE_CLUSTER_GROUP callback, PCLUSAPI_CREATE_CLUSTER_GROUP callback function [Failover Cluster], _wolf_createclustergroup, clusapi/PCLUSAPI_CREATE_CLUSTER_GROUP, mscs.createclustergroup
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
-	PCLUSAPI_CREATE_CLUSTER_GROUP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CREATE_CLUSTER_GROUP callback function


## -description


Adds a  <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a> to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> and returns a handle to the newly added group. The <b>PCLUSAPI_CREATE_CLUSTER_GROUP</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to the target cluster.


### -param lpszGroupName [in]

Pointer to a null-terminated Unicode string containing the name of the group to be added to the cluster identified by <i>hCluster</i>. If there is not a group by this name,  <i>CreateClusterGroup</i> creates it.


## -returns



If the operation succeeds, 
the function returns a group handle.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Do not call  <i>CreateClusterGroup</i> from a resource DLL. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.

The <i>CreateClusterGroup</i> function calls the <a href="https://msdn.microsoft.com/D24A2622-758D-4344-8872-F0D8E4EE80CC">CreateClusterGroupEx</a> function with a <b>NULL</b> CLUSTER_CREATE_GROUP_INFO. The new group is created with a group type of ClusGroupTypeUnknown.


#### Examples

See  <a href="https://msdn.microsoft.com/c6309c0e-fe81-4946-a333-efc5d2a7cb48">Creating Groups</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0c7ef9d9-d32b-448e-9e07-6befb9b3e338">OpenClusterGroup</a>
 

 

