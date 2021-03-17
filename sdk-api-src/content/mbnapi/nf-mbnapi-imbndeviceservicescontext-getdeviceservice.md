---
UID: NF:mbnapi.IMbnDeviceServicesContext.GetDeviceService
title: IMbnDeviceServicesContext::GetDeviceService (mbnapi.h)
description: Gets the IMbnDeviceService object that can be used for communicating with a device service on the Mobile Broadband device.
helpviewer_keywords: ["GetDeviceService","GetDeviceService method [Microsoft Broadband Networks]","GetDeviceService method [Microsoft Broadband Networks]","IMbnDeviceServicesContext interface","IMbnDeviceServicesContext interface [Microsoft Broadband Networks]","GetDeviceService method","IMbnDeviceServicesContext.GetDeviceService","IMbnDeviceServicesContext::GetDeviceService","mbn.imbndeviceservicescontext_getdeviceservice","mbnapi/IMbnDeviceServicesContext::GetDeviceService"]
old-location: mbn\imbndeviceservicescontext_getdeviceservice.htm
tech.root: mbn
ms.assetid: 293E9BE5-AD7D-41B7-9A27-E964EE745183
ms.date: 12/05/2018
ms.keywords: GetDeviceService, GetDeviceService method [Microsoft Broadband Networks], GetDeviceService method [Microsoft Broadband Networks],IMbnDeviceServicesContext interface, IMbnDeviceServicesContext interface [Microsoft Broadband Networks],GetDeviceService method, IMbnDeviceServicesContext.GetDeviceService, IMbnDeviceServicesContext::GetDeviceService, mbn.imbndeviceservicescontext_getdeviceservice, mbnapi/IMbnDeviceServicesContext::GetDeviceService
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
 - IMbnDeviceServicesContext::GetDeviceService
 - mbnapi/IMbnDeviceServicesContext::GetDeviceService
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
 - IMbnDeviceServicesContext.GetDeviceService
---

# IMbnDeviceServicesContext::GetDeviceService


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservice">IMbnDeviceService</a> object that can be used for communicating with a device service on the Mobile Broadband device.

## -parameters

### -param deviceServiceID [in]

The <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservice-get_deviceserviceid">deviceServiceID</a> of the Mobile Broadband device.

### -param mbnDeviceService [out, retval]

The <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservice">IMbnDeviceService</a> object.

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
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
An error was encountered when executing this method.

</td>
</tr>
</table>

## -remarks

<b>GetDeviceService</b> may return an <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservice">IMbnDeviceService</a> object that already has a command or data session open. The calling process can check if the device service is already open.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicescontext">IMbnDeviceServicesContext</a>