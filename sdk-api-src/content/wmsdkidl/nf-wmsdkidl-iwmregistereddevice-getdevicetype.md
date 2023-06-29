---
UID: NF:wmsdkidl.IWMRegisteredDevice.GetDeviceType
title: IWMRegisteredDevice::GetDeviceType (wmsdkidl.h)
description: The GetDeviceType method retrieves the device type associated with the device.
helpviewer_keywords: ["GetDeviceType","GetDeviceType method [windows Media Format]","GetDeviceType method [windows Media Format]","IWMRegisteredDevice interface","IWMRegisteredDevice interface [windows Media Format]","GetDeviceType method","IWMRegisteredDevice.GetDeviceType","IWMRegisteredDevice::GetDeviceType","IWMRegisteredDeviceGetDeviceType","wmformat.iwmregistereddevice_getdevicetype","wmsdkidl/IWMRegisteredDevice::GetDeviceType"]
old-location: wmformat\iwmregistereddevice_getdevicetype.htm
tech.root: wmformat
ms.assetid: 12f0dbf5-bc76-4fa2-ab64-cced1f41c313
ms.date: 4/26/2023
ms.keywords: GetDeviceType, GetDeviceType method [windows Media Format], GetDeviceType method [windows Media Format],IWMRegisteredDevice interface, IWMRegisteredDevice interface [windows Media Format],GetDeviceType method, IWMRegisteredDevice.GetDeviceType, IWMRegisteredDevice::GetDeviceType, IWMRegisteredDeviceGetDeviceType, wmformat.iwmregistereddevice_getdevicetype, wmsdkidl/IWMRegisteredDevice::GetDeviceType
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
 - IWMRegisteredDevice::GetDeviceType
 - wmsdkidl/IWMRegisteredDevice::GetDeviceType
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
 - IWMRegisteredDevice.GetDeviceType
---

# IWMRegisteredDevice::GetDeviceType


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetDeviceType</b> method retrieves the device type associated with the device.

## -parameters

### -param pdwType [out]

Address of a variable that receives the device type.

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

Devices that support Windows Media DRM 10 for Network Devices use the DRM_DEVICE_REGISTER_TYPE_STREAMING register type. To determine whether the device supports Windows Media DRM 10 for Network Devices, call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-iswmdrmcompliant">IsWmdrmCompliant</a>.

The DRM_DEVICE_REGISTER_TYPE_STORAGE register type is defined, but is not used in this release.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice">IWMRegisteredDevice Interface</a>