---
UID: NF:mbnapi.IMbnDeviceServicesEvents.OnOpenCommandSessionComplete
title: IMbnDeviceServicesEvents::OnOpenCommandSessionComplete
author: windows-sdk-content
description: Notification method indicating that a device service CommandSessionOpen request has completed.
old-location: mbn\imbndeviceservicesevents_onopencommandsessioncomplete.htm
tech.root: mbn
ms.assetid: DE8F8AB7-62DE-47B1-A8E2-E24DFC63892E
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMbnDeviceServicesEvents interface [Microsoft Broadband Networks],OnOpenCommandSessionComplete method, IMbnDeviceServicesEvents.OnOpenCommandSessionComplete, IMbnDeviceServicesEvents::OnOpenCommandSessionComplete, OnOpenCommandSessionComplete, OnOpenCommandSessionComplete method [Microsoft Broadband Networks], OnOpenCommandSessionComplete method [Microsoft Broadband Networks],IMbnDeviceServicesEvents interface, mbn.imbndeviceservicesevents_onopencommandsessioncomplete, mbnapi/IMbnDeviceServicesEvents::OnOpenCommandSessionComplete
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMbnDeviceServicesEvents.OnOpenCommandSessionComplete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mbnapi.h
: 
- IMbnDeviceServicesEvents.OnOpenCommandSessionComplete
: 
---

# IMbnDeviceServicesEvents::OnOpenCommandSessionComplete


## -description


Notification method indicating that a device service <b>CommandSessionOpen</b> request has completed.


## -parameters




### -param deviceService [in]

The <a href="IMbnDeviceService">IMbnDeviceService</a> object on which the <b>CommandSessionOpen</b> was requested.


### -param status [in]

A status code that indicates the outcome of the operation.


### -param requestID [in]

The request ID that was assigned by the Mobile Broadband service to the <b>CommandSessionOpen</b> request.


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
 




## -see-also




<a href="https://msdn.microsoft.com/66A388D0-C704-45D2-AD56-4F81E1928774">IMbnDeviceServicesEvents</a>
 

 

