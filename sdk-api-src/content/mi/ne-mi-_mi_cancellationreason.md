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

# _MI_CancellationReason enumeration


## -description


Value to pass to an operation cancel request to notify the system of the reason the operation is being canceled.  If the service is being shutdown, it may pass one of these values to the provider as well.


## -enum-fields




### -field MI_REASON_NONE

No reason for cancellation.


### -field MI_REASON_TIMEOUT

Operation timed out.


### -field MI_REASON_SHUTDOWN

The system is being shutdown.


### -field MI_REASON_SERVICESTOP

The service is being stopped.


## -see-also




<a href="https://msdn.microsoft.com/f2296852-ac09-447c-8088-5639f1e48efd">MI_CancelCallback</a>
 

 

