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

# PCLUSAPI_CLUSTER_OPEN_ENUM_EX callback function


## -description


Opens a handle to a cluster  in order to    iterate through its objects.


## -parameters




### -param hCluster [in]

The handle to the cluster.


### -param dwType [in]

A bitmask that describes the type of objects to be enumerated. This must be one or more of the 
       <a href="https://msdn.microsoft.com/e3d5a207-d30e-4935-be95-0957e68d4fe6">CLUSTER_ENUM</a> enumeration values.


### -param pOptions [in, optional]

TBD


## -returns



If the operation succeeds, returns a handle to a cluster enumerator.

If the operation fails, the function returns <b>NULL</b>. For more information about the 
       error, call the function <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/e3d5a207-d30e-4935-be95-0957e68d4fe6">CLUSTER_ENUM</a>



<a href="https://msdn.microsoft.com/1b3a3b23-39db-47b7-b4a8-17fc1ee45df6">Failover Cluster Management Function</a>
 

 

