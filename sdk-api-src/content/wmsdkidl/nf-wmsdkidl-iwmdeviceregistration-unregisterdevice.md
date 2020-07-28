---
UID: NF:wmsdkidl.IWMDeviceRegistration.UnregisterDevice
title: IWMDeviceRegistration::UnregisterDevice (wmsdkidl.h)
description: The UnregisterDevice method removes a device from the device registration database.
helpviewer_keywords: ["IWMDeviceRegistration interface [windows Media Format]","UnregisterDevice method","IWMDeviceRegistration.UnregisterDevice","IWMDeviceRegistration::UnregisterDevice","IWMDeviceRegistrationUnregisterDevice","UnregisterDevice","UnregisterDevice method [windows Media Format]","UnregisterDevice method [windows Media Format]","IWMDeviceRegistration interface","wmformat.iwmdeviceregistration_unregisterdevice","wmsdkidl/IWMDeviceRegistration::UnregisterDevice"]
old-location: wmformat\iwmdeviceregistration_unregisterdevice.htm
tech.root: wmformat
ms.assetid: 5cb1282a-5744-4264-8f73-ecad2854a125
ms.date: 12/05/2018
ms.keywords: IWMDeviceRegistration interface [windows Media Format],UnregisterDevice method, IWMDeviceRegistration.UnregisterDevice, IWMDeviceRegistration::UnregisterDevice, IWMDeviceRegistrationUnregisterDevice, UnregisterDevice, UnregisterDevice method [windows Media Format], UnregisterDevice method [windows Media Format],IWMDeviceRegistration interface, wmformat.iwmdeviceregistration_unregisterdevice, wmsdkidl/IWMDeviceRegistration::UnregisterDevice
f1_keywords:
- wmsdkidl/IWMDeviceRegistration.UnregisterDevice
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- WMStubDRM.lib
- WMStubDRM.dll
api_name:
- IWMDeviceRegistration.UnregisterDevice
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDeviceRegistration::UnregisterDevice


## -description


<p class="CCE_Message">[<b>UnregisterDevice</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>UnregisterDevice</b> method removes a device from the device registration database.




## -parameters




### -param dwRegisterType [in]

<b>DWORD</b> containing the type of the device to remove. Devices that support Windows Media DRM 10 for Network Devices use the DRM_DEVICE_REGISTER_TYPE_STREAMING register type.


### -param pbCertificate [in]

Address of the device certificate in memory.


### -param cbCertificate [in]

The size of the certificate data in bytes.


### -param SerialNumber [in]

128-bit device identifier, stored in a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_val16">DRM_VAL16</a> structure.


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

</td>
</tr>
</table>
 




## -remarks



The DRM_DEVICE_REGISTER_TYPE_STORAGE register type is defined, but is not used in this release.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration">IWMDeviceRegistration Interface</a>
 

 

