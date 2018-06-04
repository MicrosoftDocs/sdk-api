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

# IMFWorkQueueServicesEx::GetPlatformWorkQueueMMCSSPriority


## -description


Gets the priority of the Multimedia Class Scheduler Service (MMCSS)  priority associated with
    the specified platform work queue.


## -parameters




### -param dwPlatformWorkQueueId [in]

Topology work queue id for which the info will be returned.


### -param plPriority [out]


## -returns



Pointer to a buffer allocated by the caller
    that the work queue's MMCSS task id will be copied to.




## -see-also




<a href="https://msdn.microsoft.com/12d4f0f4-9a6d-4782-b5ae-4add6608782a">IMFWorkQueueServicesEx</a>
 

 

