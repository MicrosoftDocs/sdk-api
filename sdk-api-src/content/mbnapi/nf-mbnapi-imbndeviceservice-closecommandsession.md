---
UID: NF:mbnapi.IMbnDeviceService.CloseCommandSession
title: IMbnDeviceService::CloseCommandSession (mbnapi.h)
author: windows-sdk-content
description: Closes a command session to a device service on a Mobile Broadband device.
old-location: mbn\imbndeviceservice_closecommandsession.htm
tech.root: mbn
ms.assetid: B0066062-0F10-49B8-85CC-0658757BF52B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CloseCommandSession, CloseCommandSession method [Microsoft Broadband Networks], CloseCommandSession method [Microsoft Broadband Networks],IMbnDeviceService interface, IMbnDeviceService interface [Microsoft Broadband Networks],CloseCommandSession method, IMbnDeviceService.CloseCommandSession, IMbnDeviceService::CloseCommandSession, mbn.imbndeviceservice_closecommandsession, mbnapi/IMbnDeviceService::CloseCommandSession
ms.topic: method
f1_keywords: ["mbnapi/IMbnDeviceService.CloseCommandSession"]
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
 - IMbnDeviceService.CloseCommandSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnDeviceService::CloseCommandSession


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

This is an asynchronous operation and <b>CloseCommandSession</b> will return immediately. On completion of the operation, the Mobile Broadband service will call the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservicesevents-onclosecommandsessioncomplete">OnCloseCommandSessionComplete</a> method of the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicesevents">IMbnDeviceServicesEvents</a> interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservice">IMbnDeviceService</a>
 

 

