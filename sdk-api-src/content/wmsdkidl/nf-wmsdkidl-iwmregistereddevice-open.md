---
UID: NF:wmsdkidl.IWMRegisteredDevice.Open
title: IWMRegisteredDevice::Open
author: windows-sdk-content
description: The Open method opens the device so that it can receive media data.
old-location: wmformat\iwmregistereddevice_open.htm
old-project: wmformat
ms.assetid: 277f2724-5d82-4db7-96d9-af392b39fccf
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IWMRegisteredDevice interface [windows Media Format],Open method, IWMRegisteredDevice.Open, IWMRegisteredDevice::Open, IWMRegisteredDeviceOpen, Open, Open method [windows Media Format], Open method [windows Media Format],IWMRegisteredDevice interface, wmformat.iwmregistereddevice_open, wmsdkidl/IWMRegisteredDevice::Open
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
 - IWMRegisteredDevice.Open
product: Windows
targetos: Windows
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMRegisteredDevice::Open


## -description



The <b>Open</b> method opens the device so that it can receive media data.




## -parameters






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
<dt><b>NS_E_DRM_DEVICE_LIMIT_REACHED</b></dt>
</dl>
</td>
<td width="60%">
The client computer already has the maximum number of devices opened.

</td>
</tr>
</table>
 




## -remarks



To receive data, a device must be opened, validated, and approved.

Use this method to open the device. To determine whether the device is already open, call <a href="https://msdn.microsoft.com/5a8a6b2a-6a04-4505-b4be-ec10e1e5effe">IsOpened</a>. Only 10 devices can be open on a computer at a time.

The device is valid only if proximity detection has been performed on it within the past 48 hours. You can check the validity of the device by calling <a href="https://msdn.microsoft.com/ce09e6ad-10c0-4cdd-8dee-4faacd958f2b">IsValid</a>. For more information, see the <a href="https://msdn.microsoft.com/0897ad8f-8e06-4de9-840e-1588e0e20c54">IWMProximityDetection</a> interface.

Call the <a href="https://msdn.microsoft.com/ab90468e-743f-4367-a49b-d494bf9be28f">IsApproved</a> method to determine whether the device is approved. To approve the device, call the <a href="https://msdn.microsoft.com/941714b8-c329-4768-9c48-86fa806550c3">Approve</a> method.




## -see-also




<a href="https://msdn.microsoft.com/6babdfbd-51d5-4973-9712-f79a95f5f367">IWMRegisteredDevice Interface</a>



<a href="https://msdn.microsoft.com/5d30eb82-1d5c-4d40-9dc9-7360e64cd55e">IWMRegisteredDevice::Close</a>
 

 

