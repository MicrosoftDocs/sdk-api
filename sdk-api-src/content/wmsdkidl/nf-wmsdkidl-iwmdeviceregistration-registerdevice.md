---
UID: NF:wmsdkidl.IWMDeviceRegistration.RegisterDevice
title: IWMDeviceRegistration::RegisterDevice
author: windows-driver-content
description: The RegisterDevice method adds a device to the device list.
old-location: wmformat\iwmdeviceregistration_registerdevice.htm
old-project: wmformat
ms.assetid: cdce6941-dac9-4de5-8230-904c26e82642
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IWMDeviceRegistration interface [windows Media Format],RegisterDevice method, IWMDeviceRegistration.RegisterDevice, IWMDeviceRegistration::RegisterDevice, IWMDeviceRegistrationRegisterDevice, RegisterDevice, RegisterDevice method [windows Media Format], RegisterDevice method [windows Media Format],IWMDeviceRegistration interface, wmformat.iwmdeviceregistration_registerdevice, wmsdkidl/IWMDeviceRegistration::RegisterDevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMDeviceRegistration.RegisterDevice
product: Windows
targetos: Windows
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMDeviceRegistration::RegisterDevice


## -description


<p class="CCE_Message">[<b>RegisterDevice</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
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

128-bit device identifier, stored in a <a href="https://msdn.microsoft.com/8981042a-f11d-458d-be27-3b1749f9e995">DRM_VAL16</a> structure.


### -param ppDevice [out]

Address of a variable that receives a pointer to the <a href="https://msdn.microsoft.com/6babdfbd-51d5-4973-9712-f79a95f5f367">IWMRegisteredDevice</a> interface of the newly registered device.


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



Registration is triggered by a registration request message sent to your application by the device. When you receive this message, you must first extract the certificate and device identifier from it by calling <a href="https://msdn.microsoft.com/d2d142bf-0fed-42c8-a2f1-b539a40ac074">IWMDRMMessageParser::ParseRegistrationReqMsg</a>. After parsing the message, pass the certificate and device identifier to this method.

After you register a device, you must perform proximity detection before sending any protected media data to it.

The DRM_DEVICE_REGISTER_TYPE_STORAGE register type is defined, but is not used in this release.




## -see-also




<a href="https://msdn.microsoft.com/fb08ddae-2abf-4a86-a5d8-ea745ae35aa8">IWMDeviceRegistration Interface</a>



<a href="https://msdn.microsoft.com/0897ad8f-8e06-4de9-840e-1588e0e20c54">IWMProximityDetection Interface</a>
 

 

