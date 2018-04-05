---
UID: NF:mbnapi.IMbnDeviceService.CloseCommandSession
title: IMbnDeviceService::CloseCommandSession method
author: windows-driver-content
description: Closes a command session to a device service on a Mobile Broadband device.
old-location: mbn\imbndeviceservice_closecommandsession.htm
old-project: mbn
ms.assetid: B0066062-0F10-49B8-85CC-0658757BF52B
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: CloseCommandSession method [Microsoft Broadband Networks], CloseCommandSession method [Microsoft Broadband Networks], IMbnDeviceService interface, CloseCommandSession,IMbnDeviceService.CloseCommandSession, IMbnDeviceService, IMbnDeviceService interface [Microsoft Broadband Networks], CloseCommandSession method, IMbnDeviceService::CloseCommandSession, mbn.imbndeviceservice_closecommandsession, mbnapi/IMbnDeviceService::CloseCommandSession
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
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
req.typenames: MBN_VOICE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mbnapi.h
api_name:
-	IMbnDeviceService.CloseCommandSession
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnDeviceService::CloseCommandSession method


## -description


Closes a command session to a device service on a Mobile Broadband device.


## -parameters




### -param requestID [out]

A unique request ID assigned by the Mobile Broadband service to identify this request.


## -returns



The method can return one of the following values.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This device service command is not allowed for calling process privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
An error was encountered when executing this method.

</td>
</tr>
</table>
 




## -remarks



<b>CloseCommandSession</b> closes the command session to the mobile broadband device service.


This is an asynchronous operation and <b>CloseCommandSession</b> will return immediately. On completion of the operation, the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/DD313EF9-E45A-418E-91D5-0BD16C42972A">OnCloseCommandSessionComplete</a> method of the <a href="https://msdn.microsoft.com/66A388D0-C704-45D2-AD56-4F81E1928774">IMbnDeviceServicesEvents</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/5C587408-DF03-4123-BA5A-C2CCC378F60A">IMbnDeviceService</a>
 

 

