---
UID: NF:mbnapi.IMbnDeviceServicesEvents.OnCloseDataSessionComplete
title: IMbnDeviceServicesEvents::OnCloseDataSessionComplete
author: windows-sdk-content
description: Notification method indicating that a device service session CloseDataSession request has completed.
old-location: mbn\imbndeviceservicesevents_onclosedatasessioncomplete.htm
old-project: mbn
ms.assetid: 003D87F7-CFFD-47A3-8DAA-0CF9F64E2CF6
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IMbnDeviceServicesEvents interface [Microsoft Broadband Networks],OnCloseDataSessionComplete method, IMbnDeviceServicesEvents.OnCloseDataSessionComplete, IMbnDeviceServicesEvents::OnCloseDataSessionComplete, OnCloseDataSessionComplete, OnCloseDataSessionComplete method [Microsoft Broadband Networks], OnCloseDataSessionComplete method [Microsoft Broadband Networks],IMbnDeviceServicesEvents interface, mbn.imbndeviceservicesevents_onclosedatasessioncomplete, mbnapi/IMbnDeviceServicesEvents::OnCloseDataSessionComplete
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.redist: 
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
 - IMbnDeviceServicesEvents.OnCloseDataSessionComplete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnDeviceServicesEvents::OnCloseDataSessionComplete


## -description


Notification method indicating that a device service session <b>CloseDataSession</b> request has completed.


## -parameters




### -param deviceService [in]

The <a href="https://msdn.microsoft.com/en-us/library/Hh780509(v=VS.85).aspx">IMbnDeviceService</a> session object on which the <b>CloseDataSession</b> was requested.


### -param status [in]

A status code that indicates the outcome of the operation.


### -param requestID [in]

The request ID that was assigned by the Mobile Broadband service to the <b>CloseDataSession</b> request.


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
 

 

