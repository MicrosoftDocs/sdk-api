---
UID: NN:windows.media.streaming.IBasicDevice
title: IBasicDevice (windows.media.streaming.h)
description: Encapsulates the methods and events needed to model a DLNA Device.
old-location: mediastreaming\ibasicdevice.htm
tech.root: mediastreaming
ms.assetid: E4F99A11-4ED5-44CB-BE16-CBB558412ED4
ms.date: 12/05/2018
ms.keywords: IBasicDevice, IBasicDevice interface [Media Streaming API], IBasicDevice interface [Media Streaming API],described, mediastreaming.ibasicdevice, windows/IBasicDevice
ms.topic: interface
f1_keywords:
- windows.media.streaming/IBasicDevice
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBasicDevice interface


## -description


Encapsulates the methods and events  needed to model a DLNA Device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBasicDevice</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>. <b>IBasicDevice</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice-add-connectionstatuschanged">add_ConnectionStatusChanged</a>
</td>
<td align="left" width="63%">
Registers an event handler for the <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/connectionstatuschanged">ConnectionStatusChanged</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice-canwakedevices">CanWakeDevices</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates if the device can wake.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828873(v=vs.85)">ConnectionStatus</a>
</td>
<td align="left" width="63%">
Returns an enumeration value indicating whether the device is currently on-line, off-line or sleeping but wakeable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice-description">Description</a>
</td>
<td align="left" width="63%">
Retrieves a description of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice-discoveredoncurrentnetwork">DiscoveredOnCurrentNetwork</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates if the device is on the current network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice-friendlyname">FriendlyName</a>
</td>
<td align="left" width="63%">
Retrieves the device’s friendly name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice-icons">Icons</a>
</td>
<td align="left" width="63%">
Returns a vector of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828909(v=vs.85)">IDeviceIcon</a> interfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice-ipaddresses">IpAddresses</a>
</td>
<td align="left" width="63%">
Returns a vector of IP addresses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice-manufacturername">ManufacturerName</a>
</td>
<td align="left" width="63%">
Retrieves the device’s manufacturer name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice-manufacturerurl">ManufacturerUrl</a>
</td>
<td align="left" width="63%">
Retrieves the device’s manufacturer URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice-modelname">ModelName</a>
</td>
<td align="left" width="63%">
Retrieves the device’s model name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice-modelnumber">ModelNumber</a>
</td>
<td align="left" width="63%">
Retrieves the device’s model number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice-modelurl">ModelUrl</a>
</td>
<td align="left" width="63%">
Retrieves the device’s model URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice-physicaladdresses">PhysicalAddresses</a>
</td>
<td align="left" width="63%">
Returns a vector of physical addresses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice-presentationurl">PresentationUrl</a>
</td>
<td align="left" width="63%">
Retrieves the device’s presentation URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice-remotestreamingurls">RemoteStreamingUrls</a>
</td>
<td align="left" width="63%">
Returns a vector of remote streaming URLs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice-remove-connectionstatuschanged">remove_ConnectionStatusChanged</a>
</td>
<td align="left" width="63%">
Unregisters an event handler for the <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/connectionstatuschanged">ConnectionStatusChanged</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice-serialnumber">SerialNumber</a>
</td>
<td align="left" width="63%">
Retrieves the device’s serial number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice-type">Type</a>
</td>
<td align="left" width="63%">
Retreives an enumeration value indicating the device type of the DLNA device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice-uniquedevicename">UniqueDeviceName</a>
</td>
<td align="left" width="63%">
Retrieves the device’s unique device name (UDN).

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>
 

 

