---
UID: NF:mbnapi.IMbnDeviceServicesEvents.OnQuerySupportedCommandsComplete
title: IMbnDeviceServicesEvents::OnQuerySupportedCommandsComplete
author: windows-sdk-content
description: Notification method indicating that a query for the messages supported on a device service has completed.
old-location: mbn\imbndeviceservicesevents_onquerysupportedcommandscomplete.htm
old-project: mbn
ms.assetid: CA304FF5-B630-4CD5-8E23-844499D6A8D1
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IMbnDeviceServicesEvents interface [Microsoft Broadband Networks],OnQuerySupportedCommandsComplete method, IMbnDeviceServicesEvents.OnQuerySupportedCommandsComplete, IMbnDeviceServicesEvents::OnQuerySupportedCommandsComplete, OnQuerySupportedCommandsComplete, OnQuerySupportedCommandsComplete method [Microsoft Broadband Networks], OnQuerySupportedCommandsComplete method [Microsoft Broadband Networks],IMbnDeviceServicesEvents interface, mbn.imbndeviceservicesevents_onquerysupportedcommandscomplete, mbnapi/IMbnDeviceServicesEvents::OnQuerySupportedCommandsComplete
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnDeviceServicesEvents.OnQuerySupportedCommandsComplete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnDeviceServicesEvents::OnQuerySupportedCommandsComplete


## -description


Notification method indicating that a query for the messages supported on a device service has completed.


## -parameters




### -param deviceService [in]

The <a href="https://msdn.microsoft.com/library/Hh780509(v=VS.85).aspx">IMbnDeviceService</a> object on which the query was requested.


### -param commandIDList [in]

An array that contains the list of command IDs supported by the device service.  This field is valid only if the status is <b>S_OK</b>.


### -param status [in]

A status code that indicates the outcome of the operation.


### -param requestID [in]

The request ID that was assigned by the Mobile Broadband service to the query operation request.


## -returns



The method must return the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
</table>
 




## -remarks



The Mobile Broadband service will free the memory for <i>commandIDList</i> after the function call returns. If an application wants to use this data then it should copy the contents in its own memory.




## -see-also




<a href="https://msdn.microsoft.com/66A388D0-C704-45D2-AD56-4F81E1928774">IMbnDeviceServicesEvents</a>
 

 

