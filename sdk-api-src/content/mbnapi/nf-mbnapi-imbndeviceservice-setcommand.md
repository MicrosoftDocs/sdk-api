---
UID: NF:mbnapi.IMbnDeviceService.SetCommand
title: IMbnDeviceService::SetCommand (mbnapi.h)
description: Sends a SET control command to the device service of a Mobile Broadband device.
helpviewer_keywords: ["IMbnDeviceService interface [Microsoft Broadband Networks]","SetCommand method","IMbnDeviceService.SetCommand","IMbnDeviceService::SetCommand","SetCommand","SetCommand method [Microsoft Broadband Networks]","SetCommand method [Microsoft Broadband Networks]","IMbnDeviceService interface","mbn.imbndeviceservice_setcommand","mbnapi/IMbnDeviceService::SetCommand"]
old-location: mbn\imbndeviceservice_setcommand.htm
tech.root: mbn
ms.assetid: DA45B319-4E6A-4999-85A7-7F5A4F9BED7B
ms.date: 12/05/2018
ms.keywords: IMbnDeviceService interface [Microsoft Broadband Networks],SetCommand method, IMbnDeviceService.SetCommand, IMbnDeviceService::SetCommand, SetCommand, SetCommand method [Microsoft Broadband Networks], SetCommand method [Microsoft Broadband Networks],IMbnDeviceService interface, mbn.imbndeviceservice_setcommand, mbnapi/IMbnDeviceService::SetCommand
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
 - IMbnDeviceService::SetCommand
 - mbnapi/IMbnDeviceService::SetCommand
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
 - IMbnDeviceService.SetCommand
---

# IMbnDeviceService::SetCommand


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Sends a <b>SET</b> control command to the device service of a Mobile Broadband device.

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

<b>SetCommand</b> exists to implement vendor-specific device service functionality which is not otherwise covered in the Mobile Broadband API. A command session on a device service must be opened before the application can call <b>SetCommand</b>.

The Mobile Broadband service will issue a <b>SET</b> request to the device. <i>deviceServiceData</i> will be copied byte-by-byte into the data buffer passed in to the request. This data buffer must be less than <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservicescontext-get_maxcommandsize">MaxCommandSize</a> bytes.

This is an asynchronous operation and <b>SetCommand</b> will return immediately. On completion of the operation, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservicesevents-onsetcommandcomplete">OnSetCommandComplete</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicesevents">IMbnDeviceServicesEvents</a> interface.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservice">IMbnDeviceService</a>