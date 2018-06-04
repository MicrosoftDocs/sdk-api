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

# DEVICE_NOTIFY_CALLBACK_ROUTINE callback function


## -description


An application's 
    <i>DeviceNotifyCallbackRoutine</i> 
    callback function is used for receiving power notifications.


## -parameters




### -param Context

The context provided when registering for the power notification.


### -param Type

The type of power event that caused this notification.


### -param Setting

The value of this parameter depends on the type of notification subscribed to.


## -returns



This function returns a Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/749F7C6F-1A42-43DE-921E-C3654034570D">DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS</a>



<a href="https://msdn.microsoft.com/3b39ec3a-417c-4ce4-a581-ed967f1baec9">PowerRegisterSuspendResumeNotification</a>
 

 

