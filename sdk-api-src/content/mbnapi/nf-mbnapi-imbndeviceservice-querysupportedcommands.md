---
UID: NF:mbnapi.IMbnDeviceService.QuerySupportedCommands
title: IMbnDeviceService::QuerySupportedCommands (mbnapi.h)
description: Gets the list of commands IDs supported by the Mobile Broadband device service.
helpviewer_keywords: ["IMbnDeviceService interface [Microsoft Broadband Networks]","QuerySupportedCommands method","IMbnDeviceService.QuerySupportedCommands","IMbnDeviceService::QuerySupportedCommands","QuerySupportedCommands","QuerySupportedCommands method [Microsoft Broadband Networks]","QuerySupportedCommands method [Microsoft Broadband Networks]","IMbnDeviceService interface","mbn.imbndeviceservice_querysupportedcommands","mbnapi/IMbnDeviceService::QuerySupportedCommands"]
old-location: mbn\imbndeviceservice_querysupportedcommands.htm
tech.root: mbn
ms.assetid: E82AAD40-1E91-449D-8F1C-CE31B394B2DF
ms.date: 12/05/2018
ms.keywords: IMbnDeviceService interface [Microsoft Broadband Networks],QuerySupportedCommands method, IMbnDeviceService.QuerySupportedCommands, IMbnDeviceService::QuerySupportedCommands, QuerySupportedCommands, QuerySupportedCommands method [Microsoft Broadband Networks], QuerySupportedCommands method [Microsoft Broadband Networks],IMbnDeviceService interface, mbn.imbndeviceservice_querysupportedcommands, mbnapi/IMbnDeviceService::QuerySupportedCommands
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
 - IMbnDeviceService::QuerySupportedCommands
 - mbnapi/IMbnDeviceService::QuerySupportedCommands
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
 - IMbnDeviceService.QuerySupportedCommands
---

# IMbnDeviceService::QuerySupportedCommands


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the list of commands IDs supported by the Mobile Broadband device service.

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

<b>QuerySupportedCommands</b> enables the application to enumerate the list of command messages supported by a device service on the Mobile Broadband device. 

This is an asynchronous operation and <b>QuerySupportedCommands</b> will return immediately. On completion of the operation, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservicesevents-onquerysupportedcommandscomplete">OnQuerySupportedCommandsComplete</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicesevents">IMbnDeviceServicesEvents</a> interface.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservice">IMbnDeviceService</a>