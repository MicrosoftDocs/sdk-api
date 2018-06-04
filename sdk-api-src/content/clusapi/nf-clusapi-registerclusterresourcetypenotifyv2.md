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

# RegisterClusterResourceTypeNotifyV2 function


## -description


Adds a notification type to a cluster notification port.
   This allows      an application to register for notification events that only affect a particular      cluster object.


## -parameters




### -param hChange [in]

A handle to the notification port.


### -param hCluster [in]

A handle to the cluster object.


### -param Flags [in]

A <a href="https://msdn.microsoft.com/2A49AA32-F1E2-4810-B093-F6EC050DA841">CLUSTER_CHANGE_RESOURCE_TYPE_V2</a> enumeration value that specifies the notification type to add.


### -param resTypeName [in]

A pointer to a null-terminated Unicode string that contains the name of the resource type.


### -param dwNotifyKey [in]

The notification key that is returned from the <a href="https://msdn.microsoft.com/0AF127E1-D517-4F4B-B797-40822B3B236F">GetClusterNotifyV2</a> function when the event occurs.


## -returns



<b>ERROR_SUCCESS</b> if the operation is successful; otherwise, a system error code.




## -see-also




<a href="https://msdn.microsoft.com/5bcb0411-d9c1-47e7-b799-5b1fcf2a9274">Resource Type Management Functions</a>
 

 

