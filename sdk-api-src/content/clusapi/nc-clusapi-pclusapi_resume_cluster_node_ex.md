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

# PCLUSAPI_RESUME_CLUSTER_NODE_EX callback function


## -description


Initiates the specified failback operation, and then requests that a paused node  resumes cluster activity.


## -parameters




### -param hNode [in]

The  handle to the paused node.


### -param eResumeFailbackType [in]

The type of failback operation to use when cluster activity resumes. The available failback types are specified in the <a href="https://msdn.microsoft.com/26A002F6-A933-450B-84FF-F2BC8B301B6B">CLUSTER_NODE_RESUME_FAILBACK_TYPE</a> enumeration.


### -param dwResumeFlagsReserved [in]

This parameter is reserved for future use.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/26A002F6-A933-450B-84FF-F2BC8B301B6B">CLUSTER_NODE_RESUME_FAILBACK_TYPE</a>



<a href="https://msdn.microsoft.com/18981eec-42c0-4e31-8e5c-b79d8ff89fc8">Node Management Functions</a>
 

 

