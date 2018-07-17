---
UID: NF:wmsdkidl.IWMRegisteredDevice.GetDeviceCertificate
title: IWMRegisteredDevice::GetDeviceCertificate
author: windows-sdk-content
description: The GetDeviceCertificate method retrieves the certificate of the device.
old-location: wmformat\iwmregistereddevice_getdevicecertificate.htm
old-project: wmformat
ms.assetid: 80313abc-2212-4b1a-9d4e-9f3015370ea7
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetDeviceCertificate, GetDeviceCertificate method [windows Media Format], GetDeviceCertificate method [windows Media Format],IWMRegisteredDevice interface, IWMRegisteredDevice interface [windows Media Format],GetDeviceCertificate method, IWMRegisteredDevice.GetDeviceCertificate, IWMRegisteredDevice::GetDeviceCertificate, IWMRegisteredDeviceGetDeviceCertificate, wmformat.iwmregistereddevice_getdevicecertificate, wmsdkidl/IWMRegisteredDevice::GetDeviceCertificate
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WM_AETYPE
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
product: Windows
targetos: Windows
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMRegisteredDevice::GetDeviceCertificate


## -description



The <b>GetDeviceCertificate</b> method retrieves the certificate of the device.




## -parameters




### -param ppCertificate [out]

Address of a variable that receives a pointer to the <a href="https://msdn.microsoft.com/c47c016a-e7eb-4a2c-b365-5537749db5bc">INSSBuffer</a> interface of the buffer object that contains the certificate data.


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




<a href="https://msdn.microsoft.com/6babdfbd-51d5-4973-9712-f79a95f5f367">IWMRegisteredDevice Interface</a>
 

 

