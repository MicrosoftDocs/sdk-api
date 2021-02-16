---
UID: NF:mbnapi.IMbnDeviceServicesEvents.OnQuerySupportedCommandsComplete
title: IMbnDeviceServicesEvents::OnQuerySupportedCommandsComplete (mbnapi.h)
description: Notification method indicating that a query for the messages supported on a device service has completed.
helpviewer_keywords: ["IMbnDeviceServicesEvents interface [Microsoft Broadband Networks]","OnQuerySupportedCommandsComplete method","IMbnDeviceServicesEvents.OnQuerySupportedCommandsComplete","IMbnDeviceServicesEvents::OnQuerySupportedCommandsComplete","OnQuerySupportedCommandsComplete","OnQuerySupportedCommandsComplete method [Microsoft Broadband Networks]","OnQuerySupportedCommandsComplete method [Microsoft Broadband Networks]","IMbnDeviceServicesEvents interface","mbn.imbndeviceservicesevents_onquerysupportedcommandscomplete","mbnapi/IMbnDeviceServicesEvents::OnQuerySupportedCommandsComplete"]
old-location: mbn\imbndeviceservicesevents_onquerysupportedcommandscomplete.htm
tech.root: mbn
ms.assetid: CA304FF5-B630-4CD5-8E23-844499D6A8D1
ms.date: 12/05/2018
ms.keywords: IMbnDeviceServicesEvents interface [Microsoft Broadband Networks],OnQuerySupportedCommandsComplete method, IMbnDeviceServicesEvents.OnQuerySupportedCommandsComplete, IMbnDeviceServicesEvents::OnQuerySupportedCommandsComplete, OnQuerySupportedCommandsComplete, OnQuerySupportedCommandsComplete method [Microsoft Broadband Networks], OnQuerySupportedCommandsComplete method [Microsoft Broadband Networks],IMbnDeviceServicesEvents interface, mbn.imbndeviceservicesevents_onquerysupportedcommandscomplete, mbnapi/IMbnDeviceServicesEvents::OnQuerySupportedCommandsComplete
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
 - IMbnDeviceServicesEvents::OnQuerySupportedCommandsComplete
 - mbnapi/IMbnDeviceServicesEvents::OnQuerySupportedCommandsComplete
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
 - IMbnDeviceServicesEvents.OnQuerySupportedCommandsComplete
---

# IMbnDeviceServicesEvents::OnQuerySupportedCommandsComplete


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method indicating that a query for the messages supported on a device service has completed.

## -parameters

### -param deviceService [in]

The <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservice">IMbnDeviceService</a> object on which the query was requested.

### -param commandIDList [in]

An array that contains the list of command IDs supported by the device service.  This field is valid only if the status is <b>S_OK</b>.

### -param status [in]

A status code that indicates the outcome of the operation.

### -param requestID [in]

The request ID that was assigned by the Mobile Broadband service to the query operation request.

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

The Mobile Broadband service will free the memory for <i>commandIDList</i> after the function call returns. If an application wants to use this data then it should copy the contents in its own memory.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicesevents">IMbnDeviceServicesEvents</a>