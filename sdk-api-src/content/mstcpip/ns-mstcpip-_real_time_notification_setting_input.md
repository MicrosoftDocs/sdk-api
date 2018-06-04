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

# _REAL_TIME_NOTIFICATION_SETTING_INPUT structure


## -description


The <b>REAL_TIME_NOTIFICATION_SETTING_INPUT</b> structure provides input settings to apply for the <b>REAL_TIME_NOTIFICATION_CAPABILITY</b> transport setting for a TCP socket that is used with <a href="https://msdn.microsoft.com/35cdf588-0f26-4c88-a898-e1d2ba8203ac">ControlChannelTrigger</a> to receive background network notifications in a Windows Store app.


## -struct-fields




### -field TransportSettingId

The transort setting ID.


### -field BrokerEventGuid

The realtime notification broker event GUID for this transport ID.


## -remarks



The <b>REAL_TIME_NOTIFICATION_SETTING_INPUT</b>  structure is supported on Windows 8,   and Windows Server 2012, and later versions of the operating system.

 If the <a href="https://msdn.microsoft.com/8ECBF92A-0AF9-4419-A4E8-0EDEF63FCE16">TRANSPORT_SETTING_ID</a> in the <i>lpvInBuffer</i> parameter passed to the <a href="https://msdn.microsoft.com/FA0657EE-B65E-4EFA-AF1E-CA0EA7B27715">SIO_APPLY_TRANSPORT_SETTING</a> 
        IOCTL  has the <b>Guid</b> member set to <b>REAL_TIME_NOTIFICATION_CAPABILITY</b>, then this is a request to query the real time notification settings for the TCP socket used with <a href="https://msdn.microsoft.com/35cdf588-0f26-4c88-a898-e1d2ba8203ac">ControlChannelTrigger</a> to receive background network notifications in a Windows Store app. The <i>lpvInBuffer</i> parameter should point to a <b>REAL_TIME_NOTIFICATION_SETTING_INPUT</b> structure used as input to the <b>SIO_APPLY_TRANSPORT_SETTING</b> 
        IOCTL to apply the transport setting. 




## -see-also




<a href="https://msdn.microsoft.com/35cdf588-0f26-4c88-a898-e1d2ba8203ac">ControlChannelTrigger</a>



<a href="https://msdn.microsoft.com/A008310D-D812-4DCD-A3F2-64FEEEB31DB8">REAL_TIME_NOTIFICATION_SETTING_OUTPUT</a>



<a href="https://msdn.microsoft.com/FA0657EE-B65E-4EFA-AF1E-CA0EA7B27715">SIO_APPLY_TRANSPORT_SETTING</a>



<a href="https://msdn.microsoft.com/3845BE07-A414-4118-96E8-8BEF1DEDB1D3">SIO_QUERY_TRANSPORT_SETTING</a>



<a href="https://msdn.microsoft.com/8ECBF92A-0AF9-4419-A4E8-0EDEF63FCE16">TRANSPORT_SETTING_ID</a>
 

 

