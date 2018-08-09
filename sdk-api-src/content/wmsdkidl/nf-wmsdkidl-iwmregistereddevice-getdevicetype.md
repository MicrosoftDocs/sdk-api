---
UID: NF:wmsdkidl.IWMRegisteredDevice.GetDeviceType
title: IWMRegisteredDevice::GetDeviceType
author: windows-sdk-content
description: The GetDeviceType method retrieves the device type associated with the device.
old-location: wmformat\iwmregistereddevice_getdevicetype.htm
old-project: wmformat
ms.assetid: 12f0dbf5-bc76-4fa2-ab64-cced1f41c313
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetDeviceType, GetDeviceType method [windows Media Format], GetDeviceType method [windows Media Format],IWMRegisteredDevice interface, IWMRegisteredDevice interface [windows Media Format],GetDeviceType method, IWMRegisteredDevice.GetDeviceType, IWMRegisteredDevice::GetDeviceType, IWMRegisteredDeviceGetDeviceType, wmformat.iwmregistereddevice_getdevicetype, wmsdkidl/IWMRegisteredDevice::GetDeviceType
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
 - IWMRegisteredDevice.GetDeviceType
product: Windows
targetos: Windows
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMRegisteredDevice::GetDeviceType


## -description



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



Devices that support Windows Media DRM 10 for Network Devices use the DRM_DEVICE_REGISTER_TYPE_STREAMING register type. To determine whether the device supports Windows Media DRM 10 for Network Devices, call <a href="https://msdn.microsoft.com/45bc7abb-1d39-4988-a9f0-867eaefe148f">IsWmdrmCompliant</a>.

The DRM_DEVICE_REGISTER_TYPE_STORAGE register type is defined, but is not used in this release.




## -see-also




<a href="https://msdn.microsoft.com/6babdfbd-51d5-4973-9712-f79a95f5f367">IWMRegisteredDevice Interface</a>
 

 

