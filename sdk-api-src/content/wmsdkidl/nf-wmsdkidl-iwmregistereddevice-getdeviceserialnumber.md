---
UID: NF:wmsdkidl.IWMRegisteredDevice.GetDeviceSerialNumber
title: IWMRegisteredDevice::GetDeviceSerialNumber
author: windows-sdk-content
description: The GetDeviceID method retrieves the 128-bit value that identifies the device.
old-location: wmformat\iwmregistereddevice_getdeviceserialnumber.htm
tech.root: wmformat
ms.assetid: 3e60d9f3-848e-4e90-9ef7-19f3e000fab7
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetDeviceSerialNumber, GetDeviceSerialNumber method [windows Media Format], GetDeviceSerialNumber method [windows Media Format],IWMRegisteredDevice interface, IWMRegisteredDevice interface [windows Media Format],GetDeviceSerialNumber method, IWMRegisteredDevice.GetDeviceSerialNumber, IWMRegisteredDevice::GetDeviceSerialNumber, IWMRegisteredDeviceGetDeviceID, wmformat.iwmregistereddevice_getdeviceserialnumber, wmsdkidl/IWMRegisteredDevice::GetDeviceSerialNumber
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
 - IWMRegisteredDevice.GetDeviceSerialNumber
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmsdkidl.h
: 
- IWMRegisteredDevice.GetDeviceSerialNumber
: 
---

# IWMRegisteredDevice::GetDeviceSerialNumber


## -description



The <b>GetDeviceID</b> method retrieves the 128-bit value that identifies the device.




## -parameters




### -param pSerialNumber [out]

Address of a <a href="https://msdn.microsoft.com/8981042a-f11d-458d-be27-3b1749f9e995">DRM_VAL16</a> structure that receives the device serial number.


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




<a href="https://msdn.microsoft.com/6babdfbd-51d5-4973-9712-f79a95f5f367">IWMRegisteredDevice Interface</a>
 

 

