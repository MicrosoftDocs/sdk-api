---
UID: NF:wmsdkidl.IWMDeviceRegistration.GetRegisteredDeviceByID
title: IWMDeviceRegistration::GetRegisteredDeviceByID (wmsdkidl.h)
description: The GetRegisteredDeviceByID method retrieves information about a registered device by the device identifier.
helpviewer_keywords: ["GetRegisteredDeviceByID","GetRegisteredDeviceByID method [windows Media Format]","GetRegisteredDeviceByID method [windows Media Format]","IWMDeviceRegistration interface","IWMDeviceRegistration interface [windows Media Format]","GetRegisteredDeviceByID method","IWMDeviceRegistration.GetRegisteredDeviceByID","IWMDeviceRegistration::GetRegisteredDeviceByID","IWMDeviceRegistrationGetRegisteredDeviceByID","wmformat.iwmdeviceregistration_getregistereddevicebyid","wmsdkidl/IWMDeviceRegistration::GetRegisteredDeviceByID"]
old-location: wmformat\iwmdeviceregistration_getregistereddevicebyid.htm
tech.root: wmformat
ms.assetid: 26ded37b-1169-4c47-8880-bd19c977171e
ms.date: 4/26/2023
ms.keywords: GetRegisteredDeviceByID, GetRegisteredDeviceByID method [windows Media Format], GetRegisteredDeviceByID method [windows Media Format],IWMDeviceRegistration interface, IWMDeviceRegistration interface [windows Media Format],GetRegisteredDeviceByID method, IWMDeviceRegistration.GetRegisteredDeviceByID, IWMDeviceRegistration::GetRegisteredDeviceByID, IWMDeviceRegistrationGetRegisteredDeviceByID, wmformat.iwmdeviceregistration_getregistereddevicebyid, wmsdkidl/IWMDeviceRegistration::GetRegisteredDeviceByID
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
 - IWMDeviceRegistration::GetRegisteredDeviceByID
 - wmsdkidl/IWMDeviceRegistration::GetRegisteredDeviceByID
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
 - IWMDeviceRegistration.GetRegisteredDeviceByID
---

# IWMDeviceRegistration::GetRegisteredDeviceByID


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>GetRegisteredDeviceByID</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>GetRegisteredDeviceByID</b> method retrieves information about a registered device by the device identifier.

## -parameters

### -param dwRegisterType [in]

The type of the device for which to retrieve information. Devices that support Windows Media DRM 10 for Network Devices use the DRM_DEVICE_REGISTER_TYPE_STREAMING register type.

### -param pbCertificate [in]

Address of the device certificate in memory.

### -param cbCertificate [in]

The size of the certificate data in bytes.

### -param SerialNumber [in]

128-bit device identifier, stored in a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_val16">DRM_VAL16</a> structure.

### -param ppDevice [out]

Address of a variable that receives a pointer to an <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice">IWMRegisteredDevice</a> interface. This interface provides access to information about the registered device in the list that matches the other identifying parameters.

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

OR

The <i>pbCertificate</i> parameter is <b>NULL</b>, but the <i>cbCertificate</i> parameter is greater than zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_DRM_DEVICE_NOT_REGISTERED</b></dt>
</dl>
</td>
<td width="60%">
The specified device is not registered.

</td>
</tr>
</table>

## -remarks

When your application receives messages from a device, you can use the methods of the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmmessageparser">IWMDRMMessageParser</a> interface to extract the device certificate and device identifier. You can identify the device by using that data as inputs to this method.

The DRM_DEVICE_REGISTER_TYPE_STORAGE register type is defined, but is not used in this release.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration">IWMDeviceRegistration Interface</a>