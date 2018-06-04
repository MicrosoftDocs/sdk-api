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

# PCLUSTER_REG_GET_BATCH_NOTIFICATION callback function


## -description


Reads a command from a batch notification.


## -parameters




### -param hBatchNotify


### -param *phBatchNotification








#### - hBatchNotification [in]

A handle to the batch notification.


#### - pBatchCommand [out]

Pointer to a <a href="https://msdn.microsoft.com/31f8e255-80c8-4381-a8f3-0d48a3831a89">CLUSTER_BATCH_COMMAND</a> structure 
       that will be filled with information about the command on successful return.


## -returns



The function returns one of the following 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



The <b>PCLUSTER_REG_GET_BATCH_NOTIFICATION</b> type defines a pointer to this 
     function.




## -see-also




<a href="https://msdn.microsoft.com/31f8e255-80c8-4381-a8f3-0d48a3831a89">CLUSTER_BATCH_COMMAND</a>



<a href="https://msdn.microsoft.com/2bb0650f-ef9c-40bb-ae90-229bfa23838e">Cluster Registry Access Functions</a>
 

 

