---
UID: NF:clusapi.SetClusterNetworkPriorityOrder
title: SetClusterNetworkPriorityOrder function
author: windows-sdk-content
description: Sets the priority order for the set of networks used for internal communication between cluster nodes.
old-location: mscs\setclusternetworkpriorityorder.htm
tech.root: mscs
ms.assetid: 538e5024-6c51-4b11-a5ff-9df6aa7a4606
ms.author: windowssdkdev
ms.date: 11/06/2018
ms.keywords: PCLUSAPI_SET_CLUSTER_NETWORK_PRIORITY_ORDER, PCLUSAPI_SET_CLUSTER_NETWORK_PRIORITY_ORDER function [Failover Cluster], SetClusterNetworkPriorityOrder, SetClusterNetworkPriorityOrder function [Failover Cluster], _wolf_setclusternetworkpriorityorder, clusapi/PCLUSAPI_SET_CLUSTER_NETWORK_PRIORITY_ORDER, clusapi/SetClusterNetworkPriorityOrder, mscs.setclusternetworkpriorityorder
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - SetClusterNetworkPriorityOrder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetClusterNetworkPriorityOrder function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008 and this function does nothing and returns 
    <b>ERROR_CALL_NOT_IMPLEMENTED</b>.]

Sets the priority order for the set of <a href="https://msdn.microsoft.com/en-us/library/Aa371501(v=VS.85).aspx">networks</a> used for 
    internal communication between cluster <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">nodes</a>. The <b>PCLUSAPI_SET_CLUSTER_NETWORK_PRIORITY_ORDER</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to the <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a> to be affected.


### -param NetworkCount [in]

Number of items in the list specified by the <i>NetworkList</i> parameter.


### -param NetworkList [in]

Prioritized array of handles to network objects. The first handle in the array has the highest priority. The 
       list must contain only those networks that are used for internal communication between nodes in the cluster, 
       and there can be no duplicates.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b> (0).

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following are possible error 
       codes.




## -remarks



Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
     can have additional destructive effects. For information on how LPC and RPC handles are created, see 
     <a href="https://msdn.microsoft.com/709effda-5ff1-439e-805a-9169ca63c182">Using Object Handles</a> and 
     <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.




## -see-also




<a href="https://msdn.microsoft.com/a7511ac6-04cb-407b-90aa-3382c5160cb6">ClusterEnum</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/a888ca91-e56f-42bc-81c5-9235c6fd5172">OpenClusterNetwork</a>
 

 

