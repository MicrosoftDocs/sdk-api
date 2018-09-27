---
UID: NC:powrprof.DEVICE_NOTIFY_CALLBACK_ROUTINE
title: DEVICE_NOTIFY_CALLBACK_ROUTINE
author: windows-sdk-content
description: An application's DeviceNotifyCallbackRoutine callback function is used for receiving power notifications.
old-location: base\device_notify_callback_routine.htm
tech.root: power
ms.assetid: 5734FDEE-E330-4115-AFA5-725114023A5A
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: DEVICE_NOTIFY_CALLBACK_ROUTINE, DEVICE_NOTIFY_CALLBACK_ROUTINE callback function, DeviceNotifyCallbackRoutine, DeviceNotifyCallbackRoutine callback, DeviceNotifyCallbackRoutine callback function, PDEVICE_NOTIFY_CALLBACK_ROUTINE, PDEVICE_NOTIFY_CALLBACK_ROUTINE callback function pointer, base.device_notify_callback_routine, powrprof/DeviceNotifyCallbackRoutine, powrprof/PDEVICE_NOTIFY_CALLBACK_ROUTINE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: powrprof.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Powrprof.h
api_name:
 - DEVICE_NOTIFY_CALLBACK_ROUTINE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

