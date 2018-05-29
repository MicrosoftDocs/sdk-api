---
UID: NF:mbnapi.IMbnDeviceService.CloseDataSession
title: IMbnDeviceService::CloseDataSession
author: windows-sdk-content
description: Closes the data session to a device service on a Mobile Broadband device.
old-location: mbn\imbndeviceservice_closedatasession.htm
old-project: mbn
ms.assetid: E00322FC-05DF-4342-A182-E1F4F40FBD60
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: CloseDataSession, CloseDataSession method [Microsoft Broadband Networks], CloseDataSession method [Microsoft Broadband Networks],IMbnDeviceService interface, IMbnDeviceService interface [Microsoft Broadband Networks],CloseDataSession method, IMbnDeviceService.CloseDataSession, IMbnDeviceService::CloseDataSession, mbn.imbndeviceservice_closedatasession, mbnapi/IMbnDeviceService::CloseDataSession
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
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
req.typenames: MBN_VOICE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mbnapi.h
api_name:
-	IMbnDeviceService.CloseDataSession
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnDeviceService::CloseDataSession


## -description


Closes the data session to a device service on a Mobile Broadband device.


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



<b>CloseDataSession</b> closes the data session to the mobile broadband device service. The data session must be opened before the application can call <b>CloseDataSession</b>.

This is an asynchronous operation and <b>CloseDataSession</b> will return immediately. On completion of the operation, the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/003D87F7-CFFD-47A3-8DAA-0CF9F64E2CF6">OnCloseDataSessionComplete</a> method of the <a href="https://msdn.microsoft.com/66A388D0-C704-45D2-AD56-4F81E1928774">IMbnDeviceServicesEvents</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/5C587408-DF03-4123-BA5A-C2CCC378F60A">IMbnDeviceService</a>
 

 

