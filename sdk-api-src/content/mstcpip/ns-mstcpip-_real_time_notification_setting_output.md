---
UID: NS:mstcpip._REAL_TIME_NOTIFICATION_SETTING_OUTPUT
title: "_REAL_TIME_NOTIFICATION_SETTING_OUTPUT"
author: windows-sdk-content
description: Provides the output settings from a query for the REAL_TIME_NOTIFICATION_CAPABILITY transport setting for a TCP socket that is used with ControlChannelTrigger to receive background network notifications in a Windows Store app.
old-location: winsock\real_time_notification_setting_output.htm
old-project: winsock
ms.assetid: 7585CA60-8C7B-4187-A311-72DFA38EB577
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PREAL_TIME_NOTIFICATION_SETTING_OUTPUT, PREAL_TIME_NOTIFICATION_SETTING_OUTPUT, PREAL_TIME_NOTIFICATION_SETTING_OUTPUT structure pointer [Winsock], REAL_TIME_NOTIFICATION_SETTING_OUTPUT, REAL_TIME_NOTIFICATION_SETTING_OUTPUT structure [Winsock], _REAL_TIME_NOTIFICATION_SETTING_OUTPUT, mstcpip/PREAL_TIME_NOTIFICATION_SETTING_OUTPUT, mstcpip/REAL_TIME_NOTIFICATION_SETTING_OUTPUT, winsock.real_time_notification_setting_output"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mstcpip.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: REAL_TIME_NOTIFICATION_SETTING_OUTPUT, *PREAL_TIME_NOTIFICATION_SETTING_OUTPUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mstcpip.h
api_name:
 - REAL_TIME_NOTIFICATION_SETTING_OUTPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _REAL_TIME_NOTIFICATION_SETTING_OUTPUT structure


## -description


The <a href="https://msdn.microsoft.com/A008310D-D812-4DCD-A3F2-64FEEEB31DB8">REAL_TIME_NOTIFICATION_SETTING_OUTPUT</a> structure provides the output settings from a query for the <b>REAL_TIME_NOTIFICATION_CAPABILITY</b> transport setting for a TCP socket that is used with <a href="https://msdn.microsoft.com/35cdf588-0f26-4c88-a898-e1d2ba8203ac">ControlChannelTrigger</a> to receive background network notifications in a Windows Store app.


## -struct-fields




### -field ChannelStatus

The channel status for a socket that is used with the <a href="https://msdn.microsoft.com/35cdf588-0f26-4c88-a898-e1d2ba8203ac">ControlChannelTrigger</a>.


## -remarks



The <a href="https://msdn.microsoft.com/A008310D-D812-4DCD-A3F2-64FEEEB31DB8">REAL_TIME_NOTIFICATION_SETTING_OUTPUT</a>   structure is supported on Windows 8,   and Windows Server 2012, and later versions of the operating system.

 If the <a href="https://msdn.microsoft.com/8ECBF92A-0AF9-4419-A4E8-0EDEF63FCE16">TRANSPORT_SETTING_ID</a> in the <i>lpvInBuffer</i> parameter passed to the <a href="https://msdn.microsoft.com/3845BE07-A414-4118-96E8-8BEF1DEDB1D3">SIO_QUERY_TRANSPORT_SETTING</a> 
        IOCTL  has the <b>Guid</b> member set to <b>REAL_TIME_NOTIFICATION_CAPABILITY</b>, then this is a request to query the real time notification settings for the TCP socket used with <a href="https://msdn.microsoft.com/35cdf588-0f26-4c88-a898-e1d2ba8203ac">ControlChannelTrigger</a> to receive background network notifications in a Windows Store app. If the <a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> or <a href="https://msdn.microsoft.com/098d85e3-8fe2-46c2-966d-deae4b12afd6">WSPIoctl</a> call is successful, this IOCTL returns a <a href="https://msdn.microsoft.com/A008310D-D812-4DCD-A3F2-64FEEEB31DB8">REAL_TIME_NOTIFICATION_SETTING_OUTPUT</a> structure with the current status.




## -see-also




<a href="https://msdn.microsoft.com/F60DC5AD-9114-46FA-BCFF-981D637B3683">CONTROL_CHANNEL_TRIGGER_STATUS</a>



<a href="https://msdn.microsoft.com/35cdf588-0f26-4c88-a898-e1d2ba8203ac">ControlChannelTrigger</a>



<a href="https://msdn.microsoft.com/A008310D-D812-4DCD-A3F2-64FEEEB31DB8">REAL_TIME_NOTIFICATION_SETTING_INPUT</a>



<a href="https://msdn.microsoft.com/FA0657EE-B65E-4EFA-AF1E-CA0EA7B27715">SIO_APPLY_TRANSPORT_SETTING</a>



<a href="https://msdn.microsoft.com/3845BE07-A414-4118-96E8-8BEF1DEDB1D3">SIO_QUERY_TRANSPORT_SETTING</a>
 

 

