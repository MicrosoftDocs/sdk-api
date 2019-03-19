---
UID: NN:windows.media.streaming.IBasicDevice
title: IBasicDevice (windows.media.streaming.h)
author: windows-sdk-content
description: Encapsulates the methods and events needed to model a DLNA Device.
old-location: mediastreaming\ibasicdevice.htm
tech.root: mediastreaming
ms.assetid: E4F99A11-4ED5-44CB-BE16-CBB558412ED4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBasicDevice, IBasicDevice interface [Media Streaming API], IBasicDevice interface [Media Streaming API],described, mediastreaming.ibasicdevice, windows/IBasicDevice
ms.topic: interface
req.header: windows.media.streaming.h
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
 - windows.media.streaming.h
api_name:
 - IBasicDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBasicDevice interface


## -description


Encapsulates the methods and events  needed to model a DLNA Device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBasicDevice</b> interface inherits from <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>. <b>IBasicDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBasicDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1A4CCEFE-B6B6-4AFD-9296-EE923B9EF399">add_ConnectionStatusChanged</a>
</td>
<td align="left" width="63%">
Registers an event handler for the <a href="https://msdn.microsoft.com/D1F04FA5-895E-4E86-9643-E880388DCDED">ConnectionStatusChanged</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AAD0597C-AD33-40EE-A5DA-27AC66375D38">CanWakeDevices</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates if the device can wake.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2F080C23-62AF-41EF-B51A-AE28BEE6D999">ConnectionStatus</a>
</td>
<td align="left" width="63%">
Returns an enumeration value indicating whether the device is currently on-line, off-line or sleeping but wakeable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9973AC46-E6BA-4931-BDEB-E64B147AB291">Description</a>
</td>
<td align="left" width="63%">
Retrieves a description of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E64D4E49-9790-4647-9A01-2C28C407F238">DiscoveredOnCurrentNetwork</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates if the device is on the current network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/693806E1-CA66-457D-A25B-D79064776965">FriendlyName</a>
</td>
<td align="left" width="63%">
Retrieves the device’s friendly name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0C083AF3-FE22-4A8E-87B7-0FFA7B65ADBD">Icons</a>
</td>
<td align="left" width="63%">
Returns a vector of <a href="https://msdn.microsoft.com/F86C9107-447D-47F7-A711-0687A30EF58E">IDeviceIcon</a> interfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F48B91DC-3AE2-462F-835B-292BF86904B3">IpAddresses</a>
</td>
<td align="left" width="63%">
Returns a vector of IP addresses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F04400C9-02FC-4CB5-B355-A7E84BECD098">ManufacturerName</a>
</td>
<td align="left" width="63%">
Retrieves the device’s manufacturer name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E8372D15-D8B5-49E4-950A-96B4A88B0450">ManufacturerUrl</a>
</td>
<td align="left" width="63%">
Retrieves the device’s manufacturer URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8F871E89-97C1-4788-83AB-B7E0D8D6E0B5">ModelName</a>
</td>
<td align="left" width="63%">
Retrieves the device’s model name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C4199135-0C6C-4427-8152-224D7D29C270">ModelNumber</a>
</td>
<td align="left" width="63%">
Retrieves the device’s model number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/093D306B-5DFC-4A68-803D-3DDE195A8B85">ModelUrl</a>
</td>
<td align="left" width="63%">
Retrieves the device’s model URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85F48EE3-14A1-46DA-A3C3-F94A8A43CF92">PhysicalAddresses</a>
</td>
<td align="left" width="63%">
Returns a vector of physical addresses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F1EF1BBE-F35D-4828-B4F6-D6DEFF5A6391">PresentationUrl</a>
</td>
<td align="left" width="63%">
Retrieves the device’s presentation URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19B4475F-A7E4-4DC4-9C88-68D91D023AF4">RemoteStreamingUrls</a>
</td>
<td align="left" width="63%">
Returns a vector of remote streaming URLs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/577D9C50-486D-441A-A9FE-AF79D1FC2B52">remove_ConnectionStatusChanged</a>
</td>
<td align="left" width="63%">
Unregisters an event handler for the <a href="https://msdn.microsoft.com/D1F04FA5-895E-4E86-9643-E880388DCDED">ConnectionStatusChanged</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/238A5999-0E8B-4462-AFCF-790DB58CFCB4">SerialNumber</a>
</td>
<td align="left" width="63%">
Retrieves the device’s serial number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D9FB3A02-7796-4ACB-B7D3-D171D1D9B77F">Type</a>
</td>
<td align="left" width="63%">
Retreives an enumeration value indicating the device type of the DLNA device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/393EFF96-69E1-4081-905D-D8CC47B5FC4A">UniqueDeviceName</a>
</td>
<td align="left" width="63%">
Retrieves the device’s unique device name (UDN).

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>
 

 

