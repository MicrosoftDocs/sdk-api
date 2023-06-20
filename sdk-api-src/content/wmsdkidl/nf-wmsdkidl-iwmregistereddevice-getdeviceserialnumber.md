---
UID: NF:wmsdkidl.IWMRegisteredDevice.GetDeviceSerialNumber
title: IWMRegisteredDevice::GetDeviceSerialNumber (wmsdkidl.h)
description: The GetDeviceID method retrieves the 128-bit value that identifies the device.
helpviewer_keywords: ["GetDeviceSerialNumber","GetDeviceSerialNumber method [windows Media Format]","GetDeviceSerialNumber method [windows Media Format]","IWMRegisteredDevice interface","IWMRegisteredDevice interface [windows Media Format]","GetDeviceSerialNumber method","IWMRegisteredDevice.GetDeviceSerialNumber","IWMRegisteredDevice::GetDeviceSerialNumber","IWMRegisteredDeviceGetDeviceID","wmformat.iwmregistereddevice_getdeviceserialnumber","wmsdkidl/IWMRegisteredDevice::GetDeviceSerialNumber"]
old-location: wmformat\iwmregistereddevice_getdeviceserialnumber.htm
tech.root: wmformat
ms.assetid: 3e60d9f3-848e-4e90-9ef7-19f3e000fab7
ms.date: 4/26/2023
ms.keywords: GetDeviceSerialNumber, GetDeviceSerialNumber method [windows Media Format], GetDeviceSerialNumber method [windows Media Format],IWMRegisteredDevice interface, IWMRegisteredDevice interface [windows Media Format],GetDeviceSerialNumber method, IWMRegisteredDevice.GetDeviceSerialNumber, IWMRegisteredDevice::GetDeviceSerialNumber, IWMRegisteredDeviceGetDeviceID, wmformat.iwmregistereddevice_getdeviceserialnumber, wmsdkidl/IWMRegisteredDevice::GetDeviceSerialNumber
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMRegisteredDevice::GetDeviceSerialNumber
 - wmsdkidl/IWMRegisteredDevice::GetDeviceSerialNumber
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMRegisteredDevice.GetDeviceSerialNumber
---

# IWMRegisteredDevice::GetDeviceSerialNumber


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetDeviceID</b> method retrieves the 128-bit value that identifies the device.

## -parameters

### -param pSerialNumber [out]

Address of a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_val16">DRM_VAL16</a> structure that receives the device serial number.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -remarks

The serial number can be any value that can be stored in 128 bits of memory.

Together, the device serial number and the device certificate uniquely identify the device. Manufacturers are encouraged to use a separate certificate for each device. However, a manufacturer may share a certificate between all devices of a particular type, differentiating individual devices by serial number.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice">IWMRegisteredDevice Interface</a>