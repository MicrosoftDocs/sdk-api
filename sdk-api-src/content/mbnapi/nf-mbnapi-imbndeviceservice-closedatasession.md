---
UID: NF:mbnapi.IMbnDeviceService.CloseDataSession
title: IMbnDeviceService::CloseDataSession (mbnapi.h)
description: Closes the data session to a device service on a Mobile Broadband device.
helpviewer_keywords: ["CloseDataSession","CloseDataSession method [Microsoft Broadband Networks]","CloseDataSession method [Microsoft Broadband Networks]","IMbnDeviceService interface","IMbnDeviceService interface [Microsoft Broadband Networks]","CloseDataSession method","IMbnDeviceService.CloseDataSession","IMbnDeviceService::CloseDataSession","mbn.imbndeviceservice_closedatasession","mbnapi/IMbnDeviceService::CloseDataSession"]
old-location: mbn\imbndeviceservice_closedatasession.htm
tech.root: mbn
ms.assetid: E00322FC-05DF-4342-A182-E1F4F40FBD60
ms.date: 12/05/2018
ms.keywords: CloseDataSession, CloseDataSession method [Microsoft Broadband Networks], CloseDataSession method [Microsoft Broadband Networks],IMbnDeviceService interface, IMbnDeviceService interface [Microsoft Broadband Networks],CloseDataSession method, IMbnDeviceService.CloseDataSession, IMbnDeviceService::CloseDataSession, mbn.imbndeviceservice_closedatasession, mbnapi/IMbnDeviceService::CloseDataSession
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
 - IMbnDeviceService::CloseDataSession
 - mbnapi/IMbnDeviceService::CloseDataSession
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
 - IMbnDeviceService.CloseDataSession
---

# IMbnDeviceService::CloseDataSession


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

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

This is an asynchronous operation and <b>CloseDataSession</b> will return immediately. On completion of the operation, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservicesevents-onclosedatasessioncomplete">OnCloseDataSessionComplete</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicesevents">IMbnDeviceServicesEvents</a> interface.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservice">IMbnDeviceService</a>