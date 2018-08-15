---
UID: NF:mbnapi.IMbnDeviceService.OpenCommandSession
title: IMbnDeviceService::OpenCommandSession
author: windows-sdk-content
description: Opens a command session to a device service on a Mobile Broadband device.
old-location: mbn\imbndeviceservice_opencommandsession.htm
old-project: mbn
ms.assetid: EC4FF42D-EFE9-432C-997F-426B2187BBBE
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IMbnDeviceService interface [Microsoft Broadband Networks],OpenCommandSession method, IMbnDeviceService.OpenCommandSession, IMbnDeviceService::OpenCommandSession, OpenCommandSession, OpenCommandSession method [Microsoft Broadband Networks], OpenCommandSession method [Microsoft Broadband Networks],IMbnDeviceService interface, mbn.imbndeviceservice_opencommandsession, mbnapi/IMbnDeviceService::OpenCommandSession
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
 - IMbnDeviceService.OpenCommandSession
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnDeviceService::OpenCommandSession


## -description


Opens a command session to a device service on a Mobile Broadband device.


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



<b>OpenCommandSession</b> allows an application to open a command session to a the device service on the mobile broadband device.

This is an asynchronous operation and <b>OpenCommandSession</b> will return immediately. On completion of the operation, the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/DE8F8AB7-62DE-47B1-A8E2-E24DFC63892E">OnOpenCommandSessionComplete</a> method of the <a href="https://msdn.microsoft.com/66A388D0-C704-45D2-AD56-4F81E1928774">IMbnDeviceServicesEvents</a> interface.





## -see-also




<a href="https://msdn.microsoft.com/5C587408-DF03-4123-BA5A-C2CCC378F60A">IMbnDeviceService</a>
 

 

