---
UID: NS:powrprof._DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS
title: "_DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS"
author: windows-driver-content
description: Contains parameters used when registering for a power notification.
old-location: base\device_notify_subscribe_parameters.htm
old-project: Power
ms.assetid: 749F7C6F-1A42-43DE-921E-C3654034570D
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PDEVICE_NOTIFY_SUBSCRIBE_PARAMETERS, DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS, DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS structure, PDEVICE_NOTIFY_SUBSCRIBE_PARAMETERS, PDEVICE_NOTIFY_SUBSCRIBE_PARAMETERS structure pointer, _DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS, base.device_notify_subscribe_parameters, powrprof/DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS, powrprof/PDEVICE_NOTIFY_SUBSCRIBE_PARAMETERS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS, *PDEVICE_NOTIFY_SUBSCRIBE_PARAMETERS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Powrprof.h
api_name:
-	DEVICE_NOTIFY_SUBSCRIBE_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
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
 

 

