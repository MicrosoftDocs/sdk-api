---
UID: NF:mbnapi.IMbnDeviceService.QueryCommand
title: IMbnDeviceService::QueryCommand (mbnapi.h)
description: Sends a QUERY control command to the device service of a Mobile Broadband device.
helpviewer_keywords: ["IMbnDeviceService interface [Microsoft Broadband Networks]","QueryCommand method","IMbnDeviceService.QueryCommand","IMbnDeviceService::QueryCommand","QueryCommand","QueryCommand method [Microsoft Broadband Networks]","QueryCommand method [Microsoft Broadband Networks]","IMbnDeviceService interface","mbn.imbndeviceservice_querycommand","mbnapi/IMbnDeviceService::QueryCommand"]
old-location: mbn\imbndeviceservice_querycommand.htm
tech.root: mbn
ms.assetid: EA68206E-5656-4C83-AFB0-26E7F3692DE2
ms.date: 12/05/2018
ms.keywords: IMbnDeviceService interface [Microsoft Broadband Networks],QueryCommand method, IMbnDeviceService.QueryCommand, IMbnDeviceService::QueryCommand, QueryCommand, QueryCommand method [Microsoft Broadband Networks], QueryCommand method [Microsoft Broadband Networks],IMbnDeviceService interface, mbn.imbndeviceservice_querycommand, mbnapi/IMbnDeviceService::QueryCommand
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
 - IMbnDeviceService::QueryCommand
 - mbnapi/IMbnDeviceService::QueryCommand
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
 - IMbnDeviceService.QueryCommand
---

# IMbnDeviceService::QueryCommand


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Sends a <b>QUERY</b> control command to the device service of a Mobile Broadband device.

## -parameters

### -param commandID [in]

An identifier for the command.

### -param deviceServiceData [in]

A byte array that is passed in to the device.

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

<b>QueryCommand</b> exists to implement vendor-specific device service functionality which is not otherwise covered in the Mobile Broadband API. The command session on a device service must be opened before the application can call <b>QueryCommand</b>.

The Mobile Broadband service will issue a <b>QUERY</b> request to the device. <i>deviceServiceData</i> will be copied byte-by-byte into the data buffer passed in to the request. This data buffer must not be more than <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservicescontext-get_maxcommandsize">MaxCommandSize</a> bytes.

This is an asynchronous operation and <b>QueryCommand</b> will return immediately. On completion of the operation, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservicesevents-onquerycommandcomplete">OnQueryCommandComplete</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicesevents">IMbnDeviceServicesEvents</a> interface.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservice">IMbnDeviceService</a>