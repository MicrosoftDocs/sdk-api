---
UID: NF:mbnapi.IMbnDeviceServicesEvents.OnWriteDataComplete
title: IMbnDeviceServicesEvents::OnWriteDataComplete (mbnapi.h)
description: Notification method indicating that a device service session Write request has completed.
helpviewer_keywords: ["IMbnDeviceServicesEvents interface [Microsoft Broadband Networks]","OnWriteDataComplete method","IMbnDeviceServicesEvents.OnWriteDataComplete","IMbnDeviceServicesEvents::OnWriteDataComplete","OnWriteDataComplete","OnWriteDataComplete method [Microsoft Broadband Networks]","OnWriteDataComplete method [Microsoft Broadband Networks]","IMbnDeviceServicesEvents interface","mbn.imbndeviceservicesevents_onwritedatacomplete","mbnapi/IMbnDeviceServicesEvents::OnWriteDataComplete"]
old-location: mbn\imbndeviceservicesevents_onwritedatacomplete.htm
tech.root: mbn
ms.assetid: 2C885E15-C689-4ADF-BFB0-24D03932FAC7
ms.date: 12/05/2018
ms.keywords: IMbnDeviceServicesEvents interface [Microsoft Broadband Networks],OnWriteDataComplete method, IMbnDeviceServicesEvents.OnWriteDataComplete, IMbnDeviceServicesEvents::OnWriteDataComplete, OnWriteDataComplete, OnWriteDataComplete method [Microsoft Broadband Networks], OnWriteDataComplete method [Microsoft Broadband Networks],IMbnDeviceServicesEvents interface, mbn.imbndeviceservicesevents_onwritedatacomplete, mbnapi/IMbnDeviceServicesEvents::OnWriteDataComplete
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
 - IMbnDeviceServicesEvents::OnWriteDataComplete
 - mbnapi/IMbnDeviceServicesEvents::OnWriteDataComplete
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
 - IMbnDeviceServicesEvents.OnWriteDataComplete
---

# IMbnDeviceServicesEvents::OnWriteDataComplete


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method indicating that a device service session <b>Write</b> request has completed.

## -parameters

### -param deviceService [in]

The <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservice">IMbnDeviceService</a> session object on which the <b>Write</b> was requested.

### -param status [in]

A status code that indicates the outcome of the operation.

### -param requestID [in]

The request ID that was assigned by the Mobile Broadband service to the <b>Write</b> request.

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