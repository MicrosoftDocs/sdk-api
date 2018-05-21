---
UID: NC:clusapi.PCLUSAPI_CLUSTER_NODE_ENUM
title: PCLUSAPI_CLUSTER_NODE_ENUM
author: windows-driver-content
description: Enumerates the network interfaces or groups installed on a node, returning the name of each with each call.
old-location: mscs\clusternodeenum.htm
old-project: MsCS
ms.assetid: e184ef8e-9ec6-4d84-a3d0-850298262b81
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: CLUSTER_NODE_ENUM_GROUPS, CLUSTER_NODE_ENUM_NETINTERFACES, PCLUSAPI_CLUSTER_NODE_ENUM, PCLUSAPI_CLUSTER_NODE_ENUM callback, PCLUSAPI_CLUSTER_NODE_ENUM callback function [Failover Cluster], _wolf_clusternodeenum, clusapi/PCLUSAPI_CLUSTER_NODE_ENUM, mscs.clusternodeenum
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
-	PCLUSAPI_CLUSTER_NODE_ENUM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLUSTER_NODE_ENUM callback function


## -description


Enumerates the <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interfaces</a> or 
    <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">groups</a> installed on a 
    <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a>, returning the name of each with each call. The <b>PCLUSAPI_CLUSTER_NODE_ENUM</b> type defines a pointer to this function.


## -parameters




### -param hNodeEnum [in]

Handle to an existing enumeration object originally returned by the 
       <a href="https://msdn.microsoft.com/f187f4d7-24c8-477d-91fc-0ef738b66f22">ClusterNodeOpenEnum</a> function.


### -param dwIndex [in]

Index used to identify the next entry to be enumerated. This parameter should be zero for the first call to 
       <i>ClusterNodeEnum</i> and then incremented for subsequent 
       calls.


### -param lpdwType [out]

Pointer to the type of object returned. The following value of the 
       <a href="https://msdn.microsoft.com/e8660f86-f4e5-4aa3-851a-94f0a230e12d">CLUSTER_NODE_ENUM</a> enumeration is returned with each 
       call.



#### CLUSTER_NODE_ENUM_NETINTERFACES (1)

The object is a network interface.



#### CLUSTER_NODE_ENUM_GROUPS (0x00000002)

The object is a cluster group.

<b>Windows Server 2008:  </b>The <b>CLUSTER_NODE_ENUM_GROUPS</b> value is not supported before 
          Windows Server 2008 R2.


### -param lpszName [out]

Pointer to a null-terminated Unicode string containing the name of the returned object.


### -param lpcchName [in, out]

Pointer to the size of the <i>lpszName</i> buffer as a count of characters. On input, 
       specify the maximum number of characters the buffer can hold, including the terminating 
       <b>NULL</b>. On output, specifies the number of characters in the resulting name, excluding 
       the terminating <b>NULL</b>.


## -returns



The function returns one of the following values.




## -remarks



To use <i>ClusterNodeEnum</i>, applications first open a 
     node enumeration handle by calling 
     <a href="https://msdn.microsoft.com/f187f4d7-24c8-477d-91fc-0ef738b66f22">ClusterNodeOpenEnum</a> with the 
     <i>dwType</i> parameter set to <b>CLUSTER_NODE_ENUM_NETINTERFACES</b>. 
     For more information, see <a href="https://msdn.microsoft.com/391b87d1-6765-45fd-bd27-37a1127e639a">Enumerating Objects</a>.

Note that the <i>lpcchName</i> parameter refers to a count of characters and not a count of 
     bytes, and that the returned size does not include the terminating <b>NULL</b> in the count. 
     For more information on sizing buffers, see 
     <a href="https://msdn.microsoft.com/283dc560-d547-4b42-b45c-435045080639">Data Size Conventions</a>.


#### Examples

See <a href="https://msdn.microsoft.com/391b87d1-6765-45fd-bd27-37a1127e639a">Enumerating Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/8133125f-eb5a-4cbc-a39d-72fb5f3ee384">ClusterNodeCloseEnum</a>



<a href="https://msdn.microsoft.com/f187f4d7-24c8-477d-91fc-0ef738b66f22">ClusterNodeOpenEnum</a>



<a href="https://msdn.microsoft.com/18981eec-42c0-4e31-8e5c-b79d8ff89fc8">Node Management Functions</a>
 

 

