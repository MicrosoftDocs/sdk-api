---
UID: NF:mbnapi.IMbnDeviceServicesEvents.OnEventNotification
title: IMbnDeviceServicesEvents::OnEventNotification (mbnapi.h)
author: windows-sdk-content
description: Notification method signaling a device service state change event from the Mobile Broadband device.
old-location: mbn\imbndeviceservicesevents_oneventnotification.htm
tech.root: mbn
ms.assetid: 6C3B223A-E791-4861-B93B-1EDC0DC8038B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnDeviceServicesEvents interface [Microsoft Broadband Networks],OnEventNotification method, IMbnDeviceServicesEvents.OnEventNotification, IMbnDeviceServicesEvents::OnEventNotification, OnEventNotification, OnEventNotification method [Microsoft Broadband Networks], OnEventNotification method [Microsoft Broadband Networks],IMbnDeviceServicesEvents interface, mbn.imbndeviceservicesevents_oneventnotification, mbnapi/IMbnDeviceServicesEvents::OnEventNotification
ms.topic: method
f1_keywords: 
 - "mbnapi/IMbnDeviceServicesEvents.OnEventNotification"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnDeviceServicesEvents.OnEventNotification
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnDeviceServicesEvents::OnEventNotification


## -description


Notification method signaling a device service state change event from the Mobile Broadband device.


## -parameters




### -param deviceService [in]

The <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservice">IMbnDeviceService</a> object for which the event notification was received.


### -param eventID [in]

An identifier for the event.


### -param deviceServiceData [in]

A byte array containing the data returned by underlying device.


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



The <i>deviceServiceData</i> byte array contains the byte-by-byte copy of data returned by the device. The Mobile Broadband service will free the memory after the function call returns. If an application wants to use this data then it should copy the contents in its own memory.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicesevents">IMbnDeviceServicesEvents</a>
 

 

