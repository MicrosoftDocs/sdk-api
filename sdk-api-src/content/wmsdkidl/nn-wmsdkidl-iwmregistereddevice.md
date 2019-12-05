---
UID: NN:wmsdkidl.IWMRegisteredDevice
title: IWMRegisteredDevice (wmsdkidl.h)
description: The IWMRegisteredDevice interface is the primary interface of the registered device object. It provides access to information about a playback device in the device registration database.
old-location: wmformat\iwmregistereddevice.htm
tech.root: wmformat
ms.assetid: 6babdfbd-51d5-4973-9712-f79a95f5f367
ms.date: 12/05/2018
ms.keywords: IWMRegisteredDevice, IWMRegisteredDevice interface [windows Media Format], IWMRegisteredDevice interface [windows Media Format],described, IWMRegisteredDeviceInterface, wmformat.iwmregistereddevice, wmsdkidl/IWMRegisteredDevice
ms.topic: interface
f1_keywords:
- wmsdkidl/IWMRegisteredDevice
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMRegisteredDevice interface


## -description



The <b>IWMRegisteredDevice</b> interface is the primary interface of the registered device object. It provides access to information about a playback device in the device registration database.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMRegisteredDevice</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMRegisteredDevice</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve">Approve</a>
</td>
<td align="left" width="63%">
Sets the device approval state, which controls whether a device is approved for receiving media data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-close">Close</a>
</td>
<td align="left" width="63%">
Closes the device, if opened, and releases associated resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-getattributebyindex">GetAttributeByIndex</a>
</td>
<td align="left" width="63%">
Retrieves an attribute that is associated with the device. This method uses the attribute index to identify the attribute to retrieve.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-getattributebyname">GetAttributeByName</a>
</td>
<td align="left" width="63%">
Retrieves an attribute that is associated with the device. This method uses the attribute name to identify the attribute to retrieve.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-getattributecount">GetAttributeCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of attributes that are associated with the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-getdevicecertificate">GetDeviceCertificate</a>
</td>
<td align="left" width="63%">
Retrieves the certificate of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-getdeviceserialnumber">GetDeviceSerialNumber</a>
</td>
<td align="left" width="63%">
Retrieves the device identification number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-getdevicetype">GetDeviceType</a>
</td>
<td align="left" width="63%">
Retrieves the type of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isapproved">IsApproved</a>
</td>
<td align="left" width="63%">
Returns the device approval state, which determines if a device is approved for receiving media data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isopened">IsOpened</a>
</td>
<td align="left" width="63%">
Returns whether the device is open for receiving media data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid">IsValid</a>
</td>
<td align="left" width="63%">
Returns the validation of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-iswmdrmcompliant">IsWmdrmCompliant</a>
</td>
<td align="left" width="63%">
Returns whether the device supports Windows Media DRM 10 for Network Devices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open">Open</a>
</td>
<td align="left" width="63%">
Opens the device to receive media data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-setattributebyname">SetAttributeByName</a>
</td>
<td align="left" width="63%">
Sets an attribute associated with the device.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration">IWMDeviceRegistration Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>
 

 

