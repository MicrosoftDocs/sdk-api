---
UID: NF:mbnapi.IMbnDeviceServicesEvents.OnCloseCommandSessionComplete
title: IMbnDeviceServicesEvents::OnCloseCommandSessionComplete (mbnapi.h)
description: Notification method indicating that a device service CloseCommandSession request has completed.
helpviewer_keywords: ["IMbnDeviceServicesEvents interface [Microsoft Broadband Networks]","OnCloseCommandSessionComplete method","IMbnDeviceServicesEvents.OnCloseCommandSessionComplete","IMbnDeviceServicesEvents::OnCloseCommandSessionComplete","OnCloseCommandSessionComplete","OnCloseCommandSessionComplete method [Microsoft Broadband Networks]","OnCloseCommandSessionComplete method [Microsoft Broadband Networks]","IMbnDeviceServicesEvents interface","mbn.imbndeviceservicesevents_onclosecommandsessioncomplete","mbnapi/IMbnDeviceServicesEvents::OnCloseCommandSessionComplete"]
old-location: mbn\imbndeviceservicesevents_onclosecommandsessioncomplete.htm
tech.root: mbn
ms.assetid: DD313EF9-E45A-418E-91D5-0BD16C42972A
ms.date: 12/05/2018
ms.keywords: IMbnDeviceServicesEvents interface [Microsoft Broadband Networks],OnCloseCommandSessionComplete method, IMbnDeviceServicesEvents.OnCloseCommandSessionComplete, IMbnDeviceServicesEvents::OnCloseCommandSessionComplete, OnCloseCommandSessionComplete, OnCloseCommandSessionComplete method [Microsoft Broadband Networks], OnCloseCommandSessionComplete method [Microsoft Broadband Networks],IMbnDeviceServicesEvents interface, mbn.imbndeviceservicesevents_onclosecommandsessioncomplete, mbnapi/IMbnDeviceServicesEvents::OnCloseCommandSessionComplete
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
 - IMbnDeviceServicesEvents::OnCloseCommandSessionComplete
 - mbnapi/IMbnDeviceServicesEvents::OnCloseCommandSessionComplete
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
 - IMbnDeviceServicesEvents.OnCloseCommandSessionComplete
---

# IMbnDeviceServicesEvents::OnCloseCommandSessionComplete


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method indicating that a device service <b>CloseCommandSession</b> request has completed.

## -parameters

### -param deviceService [in]

The <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservice">IMbnDeviceService</a> object on which the <b>CloseCommandSession</b> was requested.

### -param status [in]

A status code that indicates the outcome of the operation.

### -param requestID [in]

The request ID that was assigned by the Mobile Broadband service to the close request.

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