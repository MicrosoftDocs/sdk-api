---
UID: NF:mbnapi.IMbnDeviceService.OpenDataSession
title: IMbnDeviceService::OpenDataSession
author: windows-sdk-content
description: Open a data session to the device service on a Mobile Broadband device.
old-location: mbn\imbndeviceservice_opendatasession.htm
old-project: mbn
ms.assetid: A26EBECA-4390-4BB2-88CD-EE2356E44E3A
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IMbnDeviceService interface [Microsoft Broadband Networks],OpenDataSession method, IMbnDeviceService.OpenDataSession, IMbnDeviceService::OpenDataSession, OpenDataSession, OpenDataSession method [Microsoft Broadband Networks], OpenDataSession method [Microsoft Broadband Networks],IMbnDeviceService interface, mbn.imbndeviceservice_opendatasession, mbnapi/IMbnDeviceService::OpenDataSession
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.redist: 
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
 - IMbnDeviceService.OpenDataSession
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnDeviceService::OpenDataSession


## -description


Open a data session to the device service on a Mobile Broadband device.


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
<dt><b>HRESULT_FROM_WIN32(ERROR_TOO_MANY_SESS)</b></dt>
</dl>
</td>
<td width="60%">
The device service has reached the maximum number of sessions it can support

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



<b>OpenDataSession</b> allows an application to open a data session to the mobile broadband device service.

This is an asynchronous operation and <b>OpenDataSession</b> will return immediately. On completion of the operation, the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/50FDF285-0C93-45C3-AB07-9BFB067DAD94">OnOpenDataSessionComplete</a> method of the <a href="https://msdn.microsoft.com/66A388D0-C704-45D2-AD56-4F81E1928774">IMbnDeviceServicesEvents</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/5C587408-DF03-4123-BA5A-C2CCC378F60A">IMbnDeviceService</a>
 

 

