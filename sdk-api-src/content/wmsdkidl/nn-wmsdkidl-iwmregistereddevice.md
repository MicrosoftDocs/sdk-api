---
UID: NN:wmsdkidl.IWMRegisteredDevice
title: IWMRegisteredDevice (wmsdkidl.h)
author: windows-sdk-content
description: The IWMRegisteredDevice interface is the primary interface of the registered device object. It provides access to information about a playback device in the device registration database.
old-location: wmformat\iwmregistereddevice.htm
tech.root: wmformat
ms.assetid: 6babdfbd-51d5-4973-9712-f79a95f5f367
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMRegisteredDevice, IWMRegisteredDevice interface [windows Media Format], IWMRegisteredDevice interface [windows Media Format],described, IWMRegisteredDeviceInterface, wmformat.iwmregistereddevice, wmsdkidl/IWMRegisteredDevice
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://msdn.microsoft.com/en-us/library/Dd743624(v=VS.85).aspx">Approve</a>
</td>
<td align="left" width="63%">
Sets the device approval state, which controls whether a device is approved for receiving media data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743627(v=VS.85).aspx">Close</a>
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
<a href="https://msdn.microsoft.com/en-us/library/Dd743632(v=VS.85).aspx">GetAttributeByName</a>
</td>
<td align="left" width="63%">
Retrieves an attribute that is associated with the device. This method uses the attribute name to identify the attribute to retrieve.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743633(v=VS.85).aspx">GetAttributeCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of attributes that are associated with the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743636(v=VS.85).aspx">GetDeviceCertificate</a>
</td>
<td align="left" width="63%">
Retrieves the certificate of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743691(v=VS.85).aspx">GetDeviceSerialNumber</a>
</td>
<td align="left" width="63%">
Retrieves the device identification number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743692(v=VS.85).aspx">GetDeviceType</a>
</td>
<td align="left" width="63%">
Retrieves the type of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743693(v=VS.85).aspx">IsApproved</a>
</td>
<td align="left" width="63%">
Returns the device approval state, which determines if a device is approved for receiving media data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743694(v=VS.85).aspx">IsOpened</a>
</td>
<td align="left" width="63%">
Returns whether the device is open for receiving media data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743695(v=VS.85).aspx">IsValid</a>
</td>
<td align="left" width="63%">
Returns the validation of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743696(v=VS.85).aspx">IsWmdrmCompliant</a>
</td>
<td align="left" width="63%">
Returns whether the device supports Windows Media DRM 10 for Network Devices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743697(v=VS.85).aspx">Open</a>
</td>
<td align="left" width="63%">
Opens the device to receive media data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743698(v=VS.85).aspx">SetAttributeByName</a>
</td>
<td align="left" width="63%">
Sets an attribute associated with the device.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743357(v=VS.85).aspx">IWMDeviceRegistration Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>
 

 

