---
UID: NF:wmsdkidl.IWMDeviceRegistration.RegisterDevice
title: IWMDeviceRegistration::RegisterDevice (wmsdkidl.h)
description: The RegisterDevice method adds a device to the device list.
helpviewer_keywords: ["IWMDeviceRegistration interface [windows Media Format]","RegisterDevice method","IWMDeviceRegistration.RegisterDevice","IWMDeviceRegistration::RegisterDevice","IWMDeviceRegistrationRegisterDevice","RegisterDevice","RegisterDevice method [windows Media Format]","RegisterDevice method [windows Media Format]","IWMDeviceRegistration interface","wmformat.iwmdeviceregistration_registerdevice","wmsdkidl/IWMDeviceRegistration::RegisterDevice"]
old-location: wmformat\iwmdeviceregistration_registerdevice.htm
tech.root: wmformat
ms.assetid: cdce6941-dac9-4de5-8230-904c26e82642
ms.date: 4/26/2023
ms.keywords: IWMDeviceRegistration interface [windows Media Format],RegisterDevice method, IWMDeviceRegistration.RegisterDevice, IWMDeviceRegistration::RegisterDevice, IWMDeviceRegistrationRegisterDevice, RegisterDevice, RegisterDevice method [windows Media Format], RegisterDevice method [windows Media Format],IWMDeviceRegistration interface, wmformat.iwmdeviceregistration_registerdevice, wmsdkidl/IWMDeviceRegistration::RegisterDevice
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
 - IWMDeviceRegistration::RegisterDevice
 - wmsdkidl/IWMDeviceRegistration::RegisterDevice
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
 - IWMDeviceRegistration.RegisterDevice
---

# IWMDeviceRegistration::RegisterDevice


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>RegisterDevice</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>RegisterDevice</b> method adds a device to the device list.

## -parameters

### -param dwRegisterType [in]

The type of the device to register. Devices that support Windows Media DRM 10 for Network Devices use DRM_DEVICE_REGISTER_TYPE_STREAMING. To register a device that does not use Windows Media DRM 10 for Network Devices, set this parameter to 0.

### -param pbCertificate [in]

Address of the device certificate in memory.

### -param cbCertificate [in]

The size of the certificate data in bytes.

### -param SerialNumber [in]

128-bit device identifier, stored in a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_val16">DRM_VAL16</a> structure.

### -param ppDevice [out]

Address of a variable that receives a pointer to the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice">IWMRegisteredDevice</a> interface of the newly registered device.

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
The <i>pbCertificate</i> parameter is <b>NULL</b>, but the <i>cbCertificate</i> parameter is greater than zero.

OR

The <i>dwRegisterType</i> parameter is set to DRM_DEVICE_REGISTER_TYPE_STREAMING, but no certificate is provided.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method could not allocate memory for an internal variable.

</td>
</tr>
</table>

## -remarks

Registration is triggered by a registration request message sent to your application by the device. When you receive this message, you must first extract the certificate and device identifier from it by calling <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg">IWMDRMMessageParser::ParseRegistrationReqMsg</a>. After parsing the message, pass the certificate and device identifier to this method.

After you register a device, you must perform proximity detection before sending any protected media data to it.

The DRM_DEVICE_REGISTER_TYPE_STORAGE register type is defined, but is not used in this release.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration">IWMDeviceRegistration Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection">IWMProximityDetection Interface</a>