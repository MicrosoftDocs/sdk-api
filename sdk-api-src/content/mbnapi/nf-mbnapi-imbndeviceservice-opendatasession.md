---
UID: NF:mbnapi.IMbnDeviceService.OpenDataSession
title: IMbnDeviceService::OpenDataSession (mbnapi.h)
description: Open a data session to the device service on a Mobile Broadband device.
helpviewer_keywords: ["IMbnDeviceService interface [Microsoft Broadband Networks]","OpenDataSession method","IMbnDeviceService.OpenDataSession","IMbnDeviceService::OpenDataSession","OpenDataSession","OpenDataSession method [Microsoft Broadband Networks]","OpenDataSession method [Microsoft Broadband Networks]","IMbnDeviceService interface","mbn.imbndeviceservice_opendatasession","mbnapi/IMbnDeviceService::OpenDataSession"]
old-location: mbn\imbndeviceservice_opendatasession.htm
tech.root: mbn
ms.assetid: A26EBECA-4390-4BB2-88CD-EE2356E44E3A
ms.date: 12/05/2018
ms.keywords: IMbnDeviceService interface [Microsoft Broadband Networks],OpenDataSession method, IMbnDeviceService.OpenDataSession, IMbnDeviceService::OpenDataSession, OpenDataSession, OpenDataSession method [Microsoft Broadband Networks], OpenDataSession method [Microsoft Broadband Networks],IMbnDeviceService interface, mbn.imbndeviceservice_opendatasession, mbnapi/IMbnDeviceService::OpenDataSession
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMbnDeviceService::OpenDataSession
 - mbnapi/IMbnDeviceService::OpenDataSession
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
 - IMbnDeviceService.OpenDataSession
---

# IMbnDeviceService::OpenDataSession


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

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

This is an asynchronous operation and <b>OpenDataSession</b> will return immediately. On completion of the operation, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservicesevents-onopendatasessioncomplete">OnOpenDataSessionComplete</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicesevents">IMbnDeviceServicesEvents</a> interface.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservice">IMbnDeviceService</a>