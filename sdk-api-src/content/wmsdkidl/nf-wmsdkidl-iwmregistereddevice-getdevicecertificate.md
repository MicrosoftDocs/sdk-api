---
UID: NF:wmsdkidl.IWMRegisteredDevice.GetDeviceCertificate
title: IWMRegisteredDevice::GetDeviceCertificate (wmsdkidl.h)
description: The GetDeviceCertificate method retrieves the certificate of the device.
helpviewer_keywords: ["GetDeviceCertificate","GetDeviceCertificate method [windows Media Format]","GetDeviceCertificate method [windows Media Format]","IWMRegisteredDevice interface","IWMRegisteredDevice interface [windows Media Format]","GetDeviceCertificate method","IWMRegisteredDevice.GetDeviceCertificate","IWMRegisteredDevice::GetDeviceCertificate","IWMRegisteredDeviceGetDeviceCertificate","wmformat.iwmregistereddevice_getdevicecertificate","wmsdkidl/IWMRegisteredDevice::GetDeviceCertificate"]
old-location: wmformat\iwmregistereddevice_getdevicecertificate.htm
tech.root: wmformat
ms.assetid: 80313abc-2212-4b1a-9d4e-9f3015370ea7
ms.date: 4/26/2023
ms.keywords: GetDeviceCertificate, GetDeviceCertificate method [windows Media Format], GetDeviceCertificate method [windows Media Format],IWMRegisteredDevice interface, IWMRegisteredDevice interface [windows Media Format],GetDeviceCertificate method, IWMRegisteredDevice.GetDeviceCertificate, IWMRegisteredDevice::GetDeviceCertificate, IWMRegisteredDeviceGetDeviceCertificate, wmformat.iwmregistereddevice_getdevicecertificate, wmsdkidl/IWMRegisteredDevice::GetDeviceCertificate
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
 - IWMRegisteredDevice::GetDeviceCertificate
 - wmsdkidl/IWMRegisteredDevice::GetDeviceCertificate
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
 - IWMRegisteredDevice.GetDeviceCertificate
---

# IWMRegisteredDevice::GetDeviceCertificate


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetDeviceCertificate</b> method retrieves the certificate of the device.

## -parameters

### -param ppCertificate [out]

Address of a variable that receives a pointer to the <a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a> interface of the buffer object that contains the certificate data.

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

The device certificate contains protection information related to the device.

Together, the device certificate and the device serial number uniquely identify the device. Manufacturers are encouraged to use a separate certificate for each device. However, a manufacturer may share a certificate between all devices of a particular type, differentiating individual devices by serial number.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice">IWMRegisteredDevice Interface</a>