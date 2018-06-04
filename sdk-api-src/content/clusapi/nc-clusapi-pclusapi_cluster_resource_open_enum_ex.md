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

# PCLUSAPI_CLUSTER_RESOURCE_OPEN_ENUM_EX callback function


## -description


Opens a handle to a  resource enumeration  that  enables iteration   through a resource's dependencies and nodes.




## -parameters




### -param hCluster [in]

A handle to the resource to iterate through.


### -param lpszProperties [in, optional]

A pointer to a list of names of common properties.


### -param cbProperties [in]

The size, in bytes, of the <i>lpszProperties</i>  parameter.


### -param lpszRoProperties [in, optional]

A pointer to a list of names of read-only common properties.


### -param cbRoProperties [in]

The size, in bytes, of the <i>lpszRoProperties</i>  parameter.


### -param dwFlags [in]

The index that identifies the next object to enumerate. This parameter should be zero for the first call to <i>ClusterResourceOpenEnumEx</i> and then be incremented for subsequent calls.


## -returns



If the operation succeeds, the function returns an enumeration handle.

If the operation fails, the function returns <b>NULL</b>. For more information about the 
       error, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d1f7360d-f592-49fb-b3b4-60d93afd7c6f">Failover Cluster Resource Management Functions</a>
 

 

