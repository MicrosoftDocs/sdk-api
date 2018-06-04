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

# CONTROL_CHANNEL_TRIGGER_STATUS enumeration


## -description


The <a href="https://msdn.microsoft.com/F60DC5AD-9114-46FA-BCFF-981D637B3683">CONTROL_CHANNEL_TRIGGER_STATUS</a> enumeration specifies the status from a query for the <b>REAL_TIME_NOTIFICATION_CAPABILITY</b> transport setting for a TCP socket that is used with <a href="https://msdn.microsoft.com/35cdf588-0f26-4c88-a898-e1d2ba8203ac">ControlChannelTrigger</a> to receive background network notifications in a Windows Store app. 


## -enum-fields




### -field CONTROL_CHANNEL_TRIGGER_STATUS_INVALID

Status is invalid.


### -field CONTROL_CHANNEL_TRIGGER_STATUS_SOFTWARE_SLOT_ALLOCATED

A software slot was allocated for the <a href="https://msdn.microsoft.com/35cdf588-0f26-4c88-a898-e1d2ba8203ac">ControlChannelTrigger</a>.


### -field CONTROL_CHANNEL_TRIGGER_STATUS_HARDWARE_SLOT_ALLOCATED

A hardware slot was allocated for the <a href="https://msdn.microsoft.com/35cdf588-0f26-4c88-a898-e1d2ba8203ac">ControlChannelTrigger</a>.


### -field CONTROL_CHANNEL_TRIGGER_STATUS_POLICY_ERROR

A status policy error.


### -field CONTROL_CHANNEL_TRIGGER_STATUS_SYSTEM_ERROR

A status system error.


### -field CONTROL_CHANNEL_TRIGGER_STATUS_TRANSPORT_DISCONNECTED

The TCP tranport is disconnected.


### -field CONTROL_CHANNEL_TRIGGER_STATUS_SERVICE_UNAVAILABLE

Service is unavailable.


## -remarks



The <a href="https://msdn.microsoft.com/F60DC5AD-9114-46FA-BCFF-981D637B3683">CONTROL_CHANNEL_TRIGGER_STATUS</a>  structure is supported on Windows 8,   and Windows Server 2012, and later versions of the operating system.

A <a href="https://msdn.microsoft.com/F60DC5AD-9114-46FA-BCFF-981D637B3683">CONTROL_CHANNEL_TRIGGER_STATUS</a> enumeration value is returned as output from the <a href="https://msdn.microsoft.com/3845BE07-A414-4118-96E8-8BEF1DEDB1D3">SIO_QUERY_TRANSPORT_SETTING</a> 
        IOCTL to a query the <b>REAL_TIME_NOTIFICATION_CAPABILITY</b> transport setting for a TCP socket that is used with <a href="https://msdn.microsoft.com/35cdf588-0f26-4c88-a898-e1d2ba8203ac">ControlChannelTrigger</a> to receive background network notifications in a Windows Store app.




## -see-also




<a href="https://msdn.microsoft.com/35cdf588-0f26-4c88-a898-e1d2ba8203ac">ControlChannelTrigger</a>



<a href="https://msdn.microsoft.com/A008310D-D812-4DCD-A3F2-64FEEEB31DB8">REAL_TIME_NOTIFICATION_SETTING_OUTPUT</a>



<a href="https://msdn.microsoft.com/FA0657EE-B65E-4EFA-AF1E-CA0EA7B27715">SIO_APPLY_TRANSPORT_SETTING</a>



<a href="https://msdn.microsoft.com/3845BE07-A414-4118-96E8-8BEF1DEDB1D3">SIO_QUERY_TRANSPORT_SETTING</a>
 

 

