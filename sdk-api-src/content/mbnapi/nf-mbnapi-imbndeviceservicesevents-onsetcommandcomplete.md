---
UID: NF:mbnapi.IMbnDeviceServicesEvents.OnSetCommandComplete
title: IMbnDeviceServicesEvents::OnSetCommandComplete (mbnapi.h)
description: Notification method indicating that a device service SET request has completed.
helpviewer_keywords: ["IMbnDeviceServicesEvents interface [Microsoft Broadband Networks]","OnSetCommandComplete method","IMbnDeviceServicesEvents.OnSetCommandComplete","IMbnDeviceServicesEvents::OnSetCommandComplete","OnSetCommandComplete","OnSetCommandComplete method [Microsoft Broadband Networks]","OnSetCommandComplete method [Microsoft Broadband Networks]","IMbnDeviceServicesEvents interface","mbn.imbndeviceservicesevents_onsetcommandcomplete","mbnapi/IMbnDeviceServicesEvents::OnSetCommandComplete"]
old-location: mbn\imbndeviceservicesevents_onsetcommandcomplete.htm
tech.root: mbn
ms.assetid: A388F548-453B-4DAB-8AD8-ABC26B22F20E
ms.date: 12/05/2018
ms.keywords: IMbnDeviceServicesEvents interface [Microsoft Broadband Networks],OnSetCommandComplete method, IMbnDeviceServicesEvents.OnSetCommandComplete, IMbnDeviceServicesEvents::OnSetCommandComplete, OnSetCommandComplete, OnSetCommandComplete method [Microsoft Broadband Networks], OnSetCommandComplete method [Microsoft Broadband Networks],IMbnDeviceServicesEvents interface, mbn.imbndeviceservicesevents_onsetcommandcomplete, mbnapi/IMbnDeviceServicesEvents::OnSetCommandComplete
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
 - IMbnDeviceServicesEvents::OnSetCommandComplete
 - mbnapi/IMbnDeviceServicesEvents::OnSetCommandComplete
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
 - IMbnDeviceServicesEvents.OnSetCommandComplete
---

# IMbnDeviceServicesEvents::OnSetCommandComplete


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method indicating that a device service <b>SET</b> request has completed.

## -parameters

### -param deviceService [in]

The <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservice">IMbnDeviceService</a> object on which the operation was requested.

### -param responseID [in]

An identifier for the response.

### -param deviceServiceData [in]

A byte array containing the data returned by the device. If the response is fragmented across multiple indications, this only contains the information for one fragment. This field is valid only if the status is <b>S_OK</b>.

### -param status [in]

A status code that indicates the outcome of the operation.

### -param requestID [in]

The request ID that was assigned by the Mobile Broadband service to the set operation request.

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

## -remarks

The <i>deviceServiceData</i> byte array contains the byte-by-byte copy of data returned by the device. The Mobile Broadband service will free the memory after the function call returns. If an application wants to use this data then it should copy the contents in its own memory.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicesevents">IMbnDeviceServicesEvents</a>