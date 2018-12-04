---
UID: NE:mstcpip.__unnamed_enum_0
title: CONTROL_CHANNEL_TRIGGER_STATUS
author: windows-sdk-content
description: Specifies the status from a query for the REAL_TIME_NOTIFICATION_CAPABILITY transport setting for a TCP socket that is used with ControlChannelTrigger to receive background network notifications in a Windows Store app.
old-location: winsock\control_channel_trigger_status.htm
tech.root: winsock
ms.assetid: D2E7663E-C388-48A5-8553-72DE2213CA97
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*PCONTROL_CHANNEL_TRIGGER_STATUS, CONTROL_CHANNEL_TRIGGER_STATUS, CONTROL_CHANNEL_TRIGGER_STATUS enumeration [Winsock], CONTROL_CHANNEL_TRIGGER_STATUS_HARDWARE_SLOT_ALLOCATED, CONTROL_CHANNEL_TRIGGER_STATUS_INVALID, CONTROL_CHANNEL_TRIGGER_STATUS_POLICY_ERROR, CONTROL_CHANNEL_TRIGGER_STATUS_SERVICE_UNAVAILABLE, CONTROL_CHANNEL_TRIGGER_STATUS_SOFTWARE_SLOT_ALLOCATED, CONTROL_CHANNEL_TRIGGER_STATUS_SYSTEM_ERROR, CONTROL_CHANNEL_TRIGGER_STATUS_TRANSPORT_DISCONNECTED, mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS, mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS_HARDWARE_SLOT_ALLOCATED, mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS_INVALID, mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS_POLICY_ERROR, mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS_SERVICE_UNAVAILABLE, mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS_SOFTWARE_SLOT_ALLOCATED, mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS_SYSTEM_ERROR, mstcpip/CONTROL_CHANNEL_TRIGGER_STATUS_TRANSPORT_DISCONNECTED, winsock.control_channel_trigger_status"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: mstcpip.h
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
 - HeaderDef
api_location:
 - Mstcpip.h
api_name:
 - CONTROL_CHANNEL_TRIGGER_STATUS
product: Windows
targetos: Windows
req.typenames: CONTROL_CHANNEL_TRIGGER_STATUS, *PCONTROL_CHANNEL_TRIGGER_STATUS
req.redist: 
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
 

 

