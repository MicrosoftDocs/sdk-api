---
UID: NF:mbnapi.IMbnDeviceService.OpenCommandSession
title: IMbnDeviceService::OpenCommandSession (mbnapi.h)
description: Opens a command session to a device service on a Mobile Broadband device.
helpviewer_keywords: ["IMbnDeviceService interface [Microsoft Broadband Networks]","OpenCommandSession method","IMbnDeviceService.OpenCommandSession","IMbnDeviceService::OpenCommandSession","OpenCommandSession","OpenCommandSession method [Microsoft Broadband Networks]","OpenCommandSession method [Microsoft Broadband Networks]","IMbnDeviceService interface","mbn.imbndeviceservice_opencommandsession","mbnapi/IMbnDeviceService::OpenCommandSession"]
old-location: mbn\imbndeviceservice_opencommandsession.htm
tech.root: mbn
ms.assetid: EC4FF42D-EFE9-432C-997F-426B2187BBBE
ms.date: 12/05/2018
ms.keywords: IMbnDeviceService interface [Microsoft Broadband Networks],OpenCommandSession method, IMbnDeviceService.OpenCommandSession, IMbnDeviceService::OpenCommandSession, OpenCommandSession, OpenCommandSession method [Microsoft Broadband Networks], OpenCommandSession method [Microsoft Broadband Networks],IMbnDeviceService interface, mbn.imbndeviceservice_opencommandsession, mbnapi/IMbnDeviceService::OpenCommandSession
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMbnDeviceService::OpenCommandSession
 - mbnapi/IMbnDeviceService::OpenCommandSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnDeviceService.OpenCommandSession
---

# IMbnDeviceService::OpenCommandSession


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

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

This is an asynchronous operation and <b>OpenCommandSession</b> will return immediately. On completion of the operation, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservicesevents-onopencommandsessioncomplete">OnOpenCommandSessionComplete</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicesevents">IMbnDeviceServicesEvents</a> interface.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservice">IMbnDeviceService</a>