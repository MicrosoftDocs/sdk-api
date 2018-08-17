---
UID: NC:clusapi.PCLUSAPI_CLUSTER_GROUP_ENUM
title: PCLUSAPI_CLUSTER_GROUP_ENUM
author: windows-sdk-content
description: Enumerates the resources in a group or the nodes that are the preferred owners of a group, returning the name of the resource or node with each call.
old-location: mscs\clustergroupenum.htm
old-project: mscs
ms.assetid: fffcae88-8df0-487f-9f6d-bc3560283ef1
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: CLUSTER_GROUP_ENUM_CONTAINS, CLUSTER_GROUP_ENUM_NODES, PCLUSAPI_CLUSTER_GROUP_ENUM, PCLUSAPI_CLUSTER_GROUP_ENUM callback, PCLUSAPI_CLUSTER_GROUP_ENUM callback function [Failover Cluster], _wolf_clustergroupenum, clusapi/PCLUSAPI_CLUSTER_GROUP_ENUM, mscs.clustergroupenum
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
 - PCLUSAPI_CLUSTER_GROUP_ENUM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLUSTER_GROUP_ENUM callback function


## -description


Enumerates the <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resources</a> in a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a> or the <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">nodes</a> that 
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
       of the <a href="https://msdn.microsoft.com/en-us/library/Bb309149(v=VS.85).aspx">CLUSTER_GROUP_ENUM</a> enumeration.



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
       <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.




## -remarks



Note that <i>lpcchName</i> refers to a count of characters and not a count of bytes, and 
     that the returned size does not include the terminating <b>NULL</b> in the count. For more 
     information on sizing buffers, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa369338(v=VS.85).aspx">Data Size Conventions</a>.

Do not call <i>ClusterGroupEnum</i> from any resource DLL 
     entry point function. <i>ClusterGroupEnum</i> can safely be 
     called from a worker thread. For more information, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa369588(v=VS.85).aspx">Function Calls to Avoid in Resource DLLs</a>.


#### Examples

See <a href="https://msdn.microsoft.com/en-us/library/Aa369563(v=VS.85).aspx">Enumerating Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9bdab6b9-a54d-4166-988c-effdeb2ab254">ClusterGroupCloseEnum</a>



<a href="https://msdn.microsoft.com/d8f9eff0-1784-4b55-8603-c262d5c23f6c">ClusterGroupOpenEnum</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369686(v=VS.85).aspx">Group Management Functions</a>
 

 

