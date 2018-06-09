---
UID: NN:wmsdkidl.IWMRegisteredDevice
title: IWMRegisteredDevice
author: windows-sdk-content
description: The IWMRegisteredDevice interface is the primary interface of the registered device object. It provides access to information about a playback device in the device registration database.
old-location: wmformat\iwmregistereddevice.htm
old-project: wmformat
ms.assetid: 6babdfbd-51d5-4973-9712-f79a95f5f367
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IWMRegisteredDevice, IWMRegisteredDevice interface [windows Media Format], IWMRegisteredDevice interface [windows Media Format],described, IWMRegisteredDeviceInterface, wmformat.iwmregistereddevice, wmsdkidl/IWMRegisteredDevice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - wmsdkidl.h
api_name:
 - IWMRegisteredDevice
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMRegisteredDevice interface


## -description



The <b>IWMRegisteredDevice</b> interface is the primary interface of the registered device object. It provides access to information about a playback device in the device registration database.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMRegisteredDevice</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMRegisteredDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMRegisteredDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/941714b8-c329-4768-9c48-86fa806550c3">Approve</a>
</td>
<td align="left" width="63%">
Sets the device approval state, which controls whether a device is approved for receiving media data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
Closes the device, if opened, and releases associated resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02a582d4-329e-47e3-9dbe-dba8a3e4b4b3">GetAttributeByIndex</a>
</td>
<td align="left" width="63%">
Retrieves an attribute that is associated with the device. This method uses the attribute index to identify the attribute to retrieve.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e74bd544-295d-4e83-8804-5a99d7efdbb8">GetAttributeByName</a>
</td>
<td align="left" width="63%">
Retrieves an attribute that is associated with the device. This method uses the attribute name to identify the attribute to retrieve.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6032cb18-4c4a-4cd7-905e-5cb390bfc37b">GetAttributeCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of attributes that are associated with the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80313abc-2212-4b1a-9d4e-9f3015370ea7">GetDeviceCertificate</a>
</td>
<td align="left" width="63%">
Retrieves the certificate of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e60d9f3-848e-4e90-9ef7-19f3e000fab7">GetDeviceSerialNumber</a>
</td>
<td align="left" width="63%">
Retrieves the device identification number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12f0dbf5-bc76-4fa2-ab64-cced1f41c313">GetDeviceType</a>
</td>
<td align="left" width="63%">
Retrieves the type of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab90468e-743f-4367-a49b-d494bf9be28f">IsApproved</a>
</td>
<td align="left" width="63%">
Returns the device approval state, which determines if a device is approved for receiving media data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a8a6b2a-6a04-4505-b4be-ec10e1e5effe">IsOpened</a>
</td>
<td align="left" width="63%">
Returns whether the device is open for receiving media data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce09e6ad-10c0-4cdd-8dee-4faacd958f2b">IsValid</a>
</td>
<td align="left" width="63%">
Returns the validation of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45bc7abb-1d39-4988-a9f0-867eaefe148f">IsWmdrmCompliant</a>
</td>
<td align="left" width="63%">
Returns whether the device supports Windows Media DRM 10 for Network Devices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>
</td>
<td align="left" width="63%">
Opens the device to receive media data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49562f2a-1bb5-46d7-81cc-c13b66cf691f">SetAttributeByName</a>
</td>
<td align="left" width="63%">
Sets an attribute associated with the device.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fb08ddae-2abf-4a86-a5d8-ea745ae35aa8">IWMDeviceRegistration Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

