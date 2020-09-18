---
UID: NF:mbnapi.IMbnDeviceService.WriteData
title: IMbnDeviceService::WriteData (mbnapi.h)
description: Write data to a device service data session.
helpviewer_keywords: ["IMbnDeviceService interface [Microsoft Broadband Networks]","WriteData method","IMbnDeviceService.WriteData","IMbnDeviceService::WriteData","WriteData","WriteData method [Microsoft Broadband Networks]","WriteData method [Microsoft Broadband Networks]","IMbnDeviceService interface","mbn.imbndeviceservice_writedata","mbnapi/IMbnDeviceService::WriteData"]
old-location: mbn\imbndeviceservice_writedata.htm
tech.root: mbn
ms.assetid: D2CD630B-FCD5-485D-84A6-B2A942842A1F
ms.date: 12/05/2018
ms.keywords: IMbnDeviceService interface [Microsoft Broadband Networks],WriteData method, IMbnDeviceService.WriteData, IMbnDeviceService::WriteData, WriteData, WriteData method [Microsoft Broadband Networks], WriteData method [Microsoft Broadband Networks],IMbnDeviceService interface, mbn.imbndeviceservice_writedata, mbnapi/IMbnDeviceService::WriteData
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IMbnDeviceService::WriteData
 - mbnapi/IMbnDeviceService::WriteData
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
 - IMbnDeviceService.WriteData
---

# IMbnDeviceService::WriteData


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Write data to a device service data session.

## -parameters

### -param deviceServiceData [in]

A byte array that is passed in to the device to write.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_BUFFER_OVERFLOW)</b></dt>
</dl>
</td>
<td width="60%">
The length of the <i>deviceServiceData</i> is greater than the supported <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservicescontext-get_maxdatasize">MaxDataSize</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_OPEN_FAILED)</b></dt>
</dl>
</td>
<td width="60%">
The device service session is not open.

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

<b>WriteData</b> passes a bulk data to a vendor-specific device service on the device. The Mobile Broadband service will forward this request to the device. <i>deviceServiceData</i> will be copied byte-by-byte into the data buffer passed in to the request. This data buffer must be less than <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservicescontext-get_maxdatasize">MaxDataSize</a> bytes.

The data session must be opened before the application can call <b>WriteData</b>. The operating system does not provide guarantees on the latency or performance of <b>WriteData</b>.

This is an asynchronous operation and <b>WriteData</b> will return immediately. On completion of the operation, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservicesevents-onwritedatacomplete">OnWriteDataComplete</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicesevents">IMbnDeviceServicesEvents</a> interface.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservice">IMbnDeviceService</a>