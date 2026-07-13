---
UID: NF:wmsdkidl.IWMDeviceRegistration.GetFirstRegisteredDevice
title: IWMDeviceRegistration::GetFirstRegisteredDevice (wmsdkidl.h)
description: The GetFirstRegisteredDevice method retrieves information about the first device of a specified type that is in the device registration database.
helpviewer_keywords: ["GetFirstRegisteredDevice","GetFirstRegisteredDevice method [windows Media Format]","GetFirstRegisteredDevice method [windows Media Format]","IWMDeviceRegistration interface","IWMDeviceRegistration interface [windows Media Format]","GetFirstRegisteredDevice method","IWMDeviceRegistration.GetFirstRegisteredDevice","IWMDeviceRegistration::GetFirstRegisteredDevice","IWMDeviceRegistrationGetFirstRegisteredDevice","wmformat.iwmdeviceregistration_getfirstregistereddevice","wmsdkidl/IWMDeviceRegistration::GetFirstRegisteredDevice"]
old-location: wmformat\iwmdeviceregistration_getfirstregistereddevice.htm
tech.root: wmformat
ms.assetid: a11249f5-0604-4de7-9dd2-152d570183c3
ms.date: 4/26/2023
ms.keywords: GetFirstRegisteredDevice, GetFirstRegisteredDevice method [windows Media Format], GetFirstRegisteredDevice method [windows Media Format],IWMDeviceRegistration interface, IWMDeviceRegistration interface [windows Media Format],GetFirstRegisteredDevice method, IWMDeviceRegistration.GetFirstRegisteredDevice, IWMDeviceRegistration::GetFirstRegisteredDevice, IWMDeviceRegistrationGetFirstRegisteredDevice, wmformat.iwmdeviceregistration_getfirstregistereddevice, wmsdkidl/IWMDeviceRegistration::GetFirstRegisteredDevice
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
 - IWMDeviceRegistration::GetFirstRegisteredDevice
 - wmsdkidl/IWMDeviceRegistration::GetFirstRegisteredDevice
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
 - IWMDeviceRegistration.GetFirstRegisteredDevice
---

# IWMDeviceRegistration::GetFirstRegisteredDevice


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>GetFirstRegisteredDevice</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>GetFirstRegisteredDevice</b> method retrieves information about the first device of a specified type that is in the device registration database.

## -parameters

### -param dwRegisterType [in]

The type of device for which to retrieve information. Devices that support Windows Media DRM 10 for Network Devices use the DRM_DEVICE_REGISTER_TYPE_STREAMING register type.

### -param ppDevice [out]

Address of a variable that receives a pointer to an <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice">IWMRegisteredDevice</a> interface. This interface provides access to information about the first registered device in the database that matches the type specified by <i>dwRegisterType</i>.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppDevice</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There are no registered devices to enumerate. When this value is returned, the address pointed to by <i>ppDevice</i> is set to <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

To enumerate registered devices of a given type, begin by calling this method to retrieve the first device entry. Then make repeated calls to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice">GetNextRegisteredDevice</a> to get subsequent device entries from the database.

The DRM_DEVICE_REGISTER_TYPE_STORAGE register type is defined, but is not used in this release.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration">IWMDeviceRegistration Interface</a>