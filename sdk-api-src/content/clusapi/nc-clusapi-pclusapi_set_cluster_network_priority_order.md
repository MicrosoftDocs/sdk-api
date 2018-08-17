---
UID: NC:clusapi.PCLUSAPI_SET_CLUSTER_NETWORK_PRIORITY_ORDER
title: PCLUSAPI_SET_CLUSTER_NETWORK_PRIORITY_ORDER
author: windows-sdk-content
description: Sets the priority order for the set of networks used for internal communication between cluster nodes.
old-location: mscs\setclusternetworkpriorityorder.htm
old-project: mscs
ms.assetid: 538e5024-6c51-4b11-a5ff-9df6aa7a4606
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PCLUSAPI_SET_CLUSTER_NETWORK_PRIORITY_ORDER, PCLUSAPI_SET_CLUSTER_NETWORK_PRIORITY_ORDER callback, PCLUSAPI_SET_CLUSTER_NETWORK_PRIORITY_ORDER callback function [Failover Cluster], _wolf_setclusternetworkpriorityorder, clusapi/PCLUSAPI_SET_CLUSTER_NETWORK_PRIORITY_ORDER, mscs.setclusternetworkpriorityorder
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 Enterprise, Windows Server 2003 Datacenter
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
 - PCLUSAPI_SET_CLUSTER_NETWORK_PRIORITY_ORDER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_SET_CLUSTER_NETWORK_PRIORITY_ORDER callback function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008 and this function does nothing and returns 
    <b>ERROR_CALL_NOT_IMPLEMENTED</b>.]

Sets the priority order for the set of <a href="https://msdn.microsoft.com/en-us/library/Aa371501(v=VS.85).aspx">networks</a> used for 
    internal communication between cluster <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">nodes</a>. The <b>PCLUSAPI_SET_CLUSTER_NETWORK_PRIORITY_ORDER</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to the <a href="https://msdn.microsoft.com/en-us/library/Aa369114(v=VS.85).aspx">cluster</a> to be affected.


### -param NetworkCount [in]

Number of items in the list specified by the <i>NetworkList</i> parameter.


### -param NetworkList[]








#### - NetworkList [in]

Prioritized array of handles to network objects. The first handle in the array has the highest priority. The 
       list must contain only those networks that are used for internal communication between nodes in the cluster, 
       and there can be no duplicates.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b> (0).

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>. The following are possible error 
       codes.




## -remarks



Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
     can have additional destructive effects. For information on how LPC and RPC handles are created, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa372959(v=VS.85).aspx">Using Object Handles</a> and 
     <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.




## -see-also




<a href="https://msdn.microsoft.com/a7511ac6-04cb-407b-90aa-3382c5160cb6">ClusterEnum</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/a888ca91-e56f-42bc-81c5-9235c6fd5172">OpenClusterNetwork</a>
 

 

