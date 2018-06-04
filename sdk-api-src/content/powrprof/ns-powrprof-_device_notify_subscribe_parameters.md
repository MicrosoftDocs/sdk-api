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

# _DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS structure


## -description


Contains parameters used when registering for a power notification.


## -struct-fields




### -field Callback

Indicates the callback function that will be called when the application receives the notification.


### -field Context

The context of the application registering for the notification.


## -see-also




<a href="https://msdn.microsoft.com/5734FDEE-E330-4115-AFA5-725114023A5A">DEVICE_NOTIFY_CALLBACK_ROUTINE</a>



<a href="https://msdn.microsoft.com/3b39ec3a-417c-4ce4-a581-ed967f1baec9">PowerRegisterSuspendResumeNotification</a>
 

 

