---
UID: NF:mbnapi.IMbnDeviceServicesEvents.OnReadData
title: IMbnDeviceServicesEvents::OnReadData
author: windows-sdk-content
description: Notification for data being read from a device service data session.
old-location: mbn\imbndeviceservicesevents_onreaddata.htm
old-project: mbn
ms.assetid: 14D2A2A3-E3E0-4C8B-B4FE-F85CA1316877
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IMbnDeviceServicesEvents interface [Microsoft Broadband Networks],OnReadData method, IMbnDeviceServicesEvents.OnReadData, IMbnDeviceServicesEvents::OnReadData, OnReadData, OnReadData method [Microsoft Broadband Networks], OnReadData method [Microsoft Broadband Networks],IMbnDeviceServicesEvents interface, mbn.imbndeviceservicesevents_onreaddata, mbnapi/IMbnDeviceServicesEvents::OnReadData
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
 - IMbnDeviceServicesEvents.OnReadData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnDeviceServicesEvents::OnReadData


## -description


Notification for data being read from a device service data session.


## -parameters




### -param deviceService [in]

The <a href="IMbnDeviceService">IMbnDeviceService</a> session object on which the data was read.


### -param deviceServiceData [in]

A byte array containing the data read from the underlying device service session.


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



This byte array contains the byte-by-byte copy of data read from the device service session. The Mobile Broadband service will free the memory for this field after the function call returns. If an application wants to use this data then it should copy the contents in its own memory.




## -see-also




<a href="https://msdn.microsoft.com/66A388D0-C704-45D2-AD56-4F81E1928774">IMbnDeviceServicesEvents</a>
 

 

