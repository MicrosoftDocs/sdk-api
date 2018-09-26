---
UID: NF:clusapi.EvictClusterNodeEx
title: EvictClusterNodeEx function
author: windows-sdk-content
description: Evicts a node from the cluster and initiates cleanup operations on the node.
old-location: mscs\evictclusternodeex.htm
tech.root: mscs
ms.assetid: 7f7ba010-265e-40d5-a429-a776d164fa07
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: EvictClusterNodeEx, EvictClusterNodeEx function [Failover Cluster], PCLUSAPI_EVICT_CLUSTER_NODE_EX, PCLUSAPI_EVICT_CLUSTER_NODE_EX function [Failover Cluster], _wolf_evictclusternodeex, clusapi/EvictClusterNodeEx, clusapi/PCLUSAPI_EVICT_CLUSTER_NODE_EX, mscs.evictclusternodeex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - EvictClusterNodeEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EvictClusterNodeEx function


## -description


Evicts a 
    <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> from the 
    <a href="c_gly.htm">cluster</a> and initiates cleanup operations on the node. The <b>PCLUSAPI_EVICT_CLUSTER_NODE_EX</b> type defines a pointer to this function.


## -parameters




### -param hNode [in]

Handle to the node to remove from the cluster.


### -param dwTimeOut [in]

Specifies the number of milliseconds for the function to wait for cleanup operations to occur. The function 
      will return when the cleanup is complete or when the specified time elapses, whichever is sooner.


### -param phrCleanupStatus [out]

Pointer to an <b>HRESULT</b>   that describes the results of the cleanup operation.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
      <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>, including the following value.




## -see-also




<a href="https://msdn.microsoft.com/0353b640-5fa6-4e83-a7e5-1b4bd2ca16d9">EvictClusterNode</a>



<a href="https://msdn.microsoft.com/7658a030-d4b2-407c-829f-61491b5907e6">OpenClusterNode</a>
 

 

