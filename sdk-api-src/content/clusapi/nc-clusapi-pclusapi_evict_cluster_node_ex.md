---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PCLUSAPI_EVICT_CLUSTER_NODE_EX callback function


## -description


Evicts a 
    <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> from the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> and initiates cleanup operations on the node. The <b>PCLUSAPI_EVICT_CLUSTER_NODE_EX</b> type defines a pointer to this function.


## -parameters




### -param hNode [in]

Handle to the node to remove from the cluster.


### -param dwTimeOut [in]

Specifies the number of milliseconds for the function to wait for cleanup operations to occur. The function 
      will return when the cleanup is complete or when the specified time elapses, whichever is sooner.


### -param *phrCleanupStatus [out]

Pointer to an <b>HRESULT</b>   that describes the results of the cleanup operation.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
      <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>, including the following value.




## -see-also




<a href="https://msdn.microsoft.com/0353b640-5fa6-4e83-a7e5-1b4bd2ca16d9">EvictClusterNode</a>



<a href="https://msdn.microsoft.com/7658a030-d4b2-407c-829f-61491b5907e6">OpenClusterNode</a>
 

 

