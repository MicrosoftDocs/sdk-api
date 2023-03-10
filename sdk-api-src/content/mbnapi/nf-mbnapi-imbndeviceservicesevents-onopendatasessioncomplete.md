---
UID: NF:mbnapi.IMbnDeviceServicesEvents.OnOpenDataSessionComplete
title: IMbnDeviceServicesEvents::OnOpenDataSessionComplete (mbnapi.h)
description: Notification method indicating that a device service OpenDataSession request has completed.
helpviewer_keywords: ["IMbnDeviceServicesEvents interface [Microsoft Broadband Networks]","OnOpenDataSessionComplete method","IMbnDeviceServicesEvents.OnOpenDataSessionComplete","IMbnDeviceServicesEvents::OnOpenDataSessionComplete","OnOpenDataSessionComplete","OnOpenDataSessionComplete method [Microsoft Broadband Networks]","OnOpenDataSessionComplete method [Microsoft Broadband Networks]","IMbnDeviceServicesEvents interface","mbn.imbndeviceservicesevents_onopendatasessioncomplete","mbnapi/IMbnDeviceServicesEvents::OnOpenDataSessionComplete"]
old-location: mbn\imbndeviceservicesevents_onopendatasessioncomplete.htm
tech.root: mbn
ms.assetid: 50FDF285-0C93-45C3-AB07-9BFB067DAD94
ms.date: 12/05/2018
ms.keywords: IMbnDeviceServicesEvents interface [Microsoft Broadband Networks],OnOpenDataSessionComplete method, IMbnDeviceServicesEvents.OnOpenDataSessionComplete, IMbnDeviceServicesEvents::OnOpenDataSessionComplete, OnOpenDataSessionComplete, OnOpenDataSessionComplete method [Microsoft Broadband Networks], OnOpenDataSessionComplete method [Microsoft Broadband Networks],IMbnDeviceServicesEvents interface, mbn.imbndeviceservicesevents_onopendatasessioncomplete, mbnapi/IMbnDeviceServicesEvents::OnOpenDataSessionComplete
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
 - IMbnDeviceServicesEvents::OnOpenDataSessionComplete
 - mbnapi/IMbnDeviceServicesEvents::OnOpenDataSessionComplete
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
 - IMbnDeviceServicesEvents.OnOpenDataSessionComplete
---

# IMbnDeviceServicesEvents::OnOpenDataSessionComplete


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method indicating that a device service <b>OpenDataSession</b> request has completed.

## -parameters

### -param deviceService [in]

The <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservice">IMbnDeviceService</a> object on which the <b>OpenDataSession</b>  was requested.

### -param status [in]

A status code that indicates the outcome of the operation.

### -param requestID [in]

The request ID that was assigned by the Mobile Broadband service to the <b>OpenDataSession</b> request.

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

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicesevents">IMbnDeviceServicesEvents</a>