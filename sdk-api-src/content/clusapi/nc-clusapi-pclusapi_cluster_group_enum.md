---
UID: NC:clusapi.PCLUSAPI_CLUSTER_GROUP_ENUM
title: PCLUSAPI_CLUSTER_GROUP_ENUM
author: windows-driver-content
description: Enumerates the resources in a group or the nodes that are the preferred owners of a group, returning the name of the resource or node with each call.
old-location: mscs\clustergroupenum.htm
old-project: MsCS
ms.assetid: fffcae88-8df0-487f-9f6d-bc3560283ef1
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: CLUSTER_GROUP_ENUM_CONTAINS, CLUSTER_GROUP_ENUM_NODES, PCLUSAPI_CLUSTER_GROUP_ENUM, PCLUSAPI_CLUSTER_GROUP_ENUM callback, PCLUSAPI_CLUSTER_GROUP_ENUM callback function [Failover Cluster], _wolf_clustergroupenum, clusapi/PCLUSAPI_CLUSTER_GROUP_ENUM, mscs.clustergroupenum
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
-	PCLUSAPI_CLUSTER_GROUP_ENUM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLUSTER_GROUP_ENUM callback function


## -description


Enumerates the <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resources</a> in a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a> or the <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">nodes</a> that 
    are the preferred owners of a group, returning the name of the resource or node with each call. The <b>PCLUSAPI_CLUSTER_GROUP_ENUM</b> type defines a pointer to this function.


## -parameters




### -param hGroupEnum [in]

A group enumeration handle returned by the 
       <a href="https://msdn.microsoft.com/d8f9eff0-1784-4b55-8603-c262d5c23f6c">ClusterGroupOpenEnum</a> function.


### -param dwIndex [in]

The index of the resource or node to return. This parameter should be zero for the first call to 
       <i>ClusterGroupEnum</i> and then incremented for 
       subsequent calls.


### -param lpdwType [out]

A pointer to the type of object returned by 
       <i>ClusterGroupEnum</i>. The following are valid values 
       of the <a href="https://msdn.microsoft.com/c70bc230-850b-4290-8275-f60ffc8d66bd">CLUSTER_GROUP_ENUM</a> enumeration.



#### CLUSTER_GROUP_ENUM_CONTAINS (1)

The object is one of the resources in the group.



#### CLUSTER_GROUP_ENUM_NODES (2)

The object is one of the nodes in the preferred owners list of the group.


### -param lpszResourceName [out]

A pointer to a null-terminated Unicode string containing the name of the returned resource or node.


### -param lpcchName [in, out]

A pointer to the size of the <i>lpszResourceName</i> buffer as a count of characters. On 
       input, specify the maximum number of characters the buffer can hold, including the terminating 
       <b>NULL</b>. On output, specifies the number of characters in the resulting name, excluding 
       the terminating <b>NULL</b>.


## -returns



The function can returns one of the following values.

If the operation was not successful due to a problem other than those described with the 
       <b>ERROR_NO_MORE_ITEMS</b> or <b>ERROR_MORE_DATA</b> values, 
       <i>ClusterGroupEnum</i> returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



Note that <i>lpcchName</i> refers to a count of characters and not a count of bytes, and 
     that the returned size does not include the terminating <b>NULL</b> in the count. For more 
     information on sizing buffers, see 
     <a href="https://msdn.microsoft.com/283dc560-d547-4b42-b45c-435045080639">Data Size Conventions</a>.

Do not call <i>ClusterGroupEnum</i> from any resource DLL 
     entry point function. <i>ClusterGroupEnum</i> can safely be 
     called from a worker thread. For more information, see 
     <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.


#### Examples

See <a href="https://msdn.microsoft.com/391b87d1-6765-45fd-bd27-37a1127e639a">Enumerating Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9bdab6b9-a54d-4166-988c-effdeb2ab254">ClusterGroupCloseEnum</a>



<a href="https://msdn.microsoft.com/d8f9eff0-1784-4b55-8603-c262d5c23f6c">ClusterGroupOpenEnum</a>



<a href="https://msdn.microsoft.com/a2336594-ac24-476e-94e8-460a31c1f643">Group Management Functions</a>
 

 

