---
UID: NF:mbnapi.IMbnDeviceServicesEvents.OnCloseDataSessionComplete
title: IMbnDeviceServicesEvents::OnCloseDataSessionComplete (mbnapi.h)
description: Notification method indicating that a device service session CloseDataSession request has completed.
helpviewer_keywords: ["IMbnDeviceServicesEvents interface [Microsoft Broadband Networks]","OnCloseDataSessionComplete method","IMbnDeviceServicesEvents.OnCloseDataSessionComplete","IMbnDeviceServicesEvents::OnCloseDataSessionComplete","OnCloseDataSessionComplete","OnCloseDataSessionComplete method [Microsoft Broadband Networks]","OnCloseDataSessionComplete method [Microsoft Broadband Networks]","IMbnDeviceServicesEvents interface","mbn.imbndeviceservicesevents_onclosedatasessioncomplete","mbnapi/IMbnDeviceServicesEvents::OnCloseDataSessionComplete"]
old-location: mbn\imbndeviceservicesevents_onclosedatasessioncomplete.htm
tech.root: mbn
ms.assetid: 003D87F7-CFFD-47A3-8DAA-0CF9F64E2CF6
ms.date: 12/05/2018
ms.keywords: IMbnDeviceServicesEvents interface [Microsoft Broadband Networks],OnCloseDataSessionComplete method, IMbnDeviceServicesEvents.OnCloseDataSessionComplete, IMbnDeviceServicesEvents::OnCloseDataSessionComplete, OnCloseDataSessionComplete, OnCloseDataSessionComplete method [Microsoft Broadband Networks], OnCloseDataSessionComplete method [Microsoft Broadband Networks],IMbnDeviceServicesEvents interface, mbn.imbndeviceservicesevents_onclosedatasessioncomplete, mbnapi/IMbnDeviceServicesEvents::OnCloseDataSessionComplete
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
 - IMbnDeviceServicesEvents::OnCloseDataSessionComplete
 - mbnapi/IMbnDeviceServicesEvents::OnCloseDataSessionComplete
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
 - IMbnDeviceServicesEvents.OnCloseDataSessionComplete
---

# IMbnDeviceServicesEvents::OnCloseDataSessionComplete


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method indicating that a device service session <b>CloseDataSession</b> request has completed.

## -parameters

### -param deviceService [in]

The <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservice">IMbnDeviceService</a> session object on which the <b>CloseDataSession</b> was requested.

### -param status [in]

A status code that indicates the outcome of the operation.

### -param requestID [in]

The request ID that was assigned by the Mobile Broadband service to the <b>CloseDataSession</b> request.

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