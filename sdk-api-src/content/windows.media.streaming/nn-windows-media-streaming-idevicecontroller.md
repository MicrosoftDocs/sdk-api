---
UID: NN:windows.media.streaming.IDeviceController
title: IDeviceController (windows.media.streaming.h)
author: windows-sdk-content
description: Encapsulates the methods and events needed to retrieve a list of cached Digital Media Renderers (DMRs) and/or Digital Media Servers (DMSs), or to asynchronously find the DMRs and/or DMSs that are currently on the network.
old-location: mediastreaming\idevicecontroller.htm
tech.root: mediastreaming
ms.assetid: 18989598-86C5-4BD7-B8F4-27496897DFBA
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDeviceController, IDeviceController interface [Media Streaming API], IDeviceController interface [Media Streaming API],described, mediastreaming.idevicecontroller, windows/IDeviceController
ms.topic: interface
f1_keywords: 
 - "windows.media.streaming/IDeviceController"
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
 - IDeviceController
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDeviceController interface


## -description


Encapsulates the methods and events  needed to retrieve a list of cached Digital Media Renderers (DMRs) and/or Digital Media Servers (DMSs), or to asynchronously find the DMRs and/or DMSs that are currently on the network.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDeviceController</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>. <b>IDeviceController</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDeviceController</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828903(v=vs.85)">add_DeviceArrival</a>
</td>
<td align="left" width="63%">
Registers an event handler for the <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/devicearrival">DeviceArrival</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828904(v=vs.85)">add_DeviceDeparture</a>
</td>
<td align="left" width="63%">
Registers an event handler for the <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/devicedeparture">DeviceDeparture</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828902(v=vs.85)">AddDevice</a>
</td>
<td align="left" width="63%">
Adds a DLNA DMR or DMS Device, identified by its UPnP Unique Device Name (UDN), to the list of devices that is returned by the <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/idevicecontroller-cacheddevices">CachedDevices</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/idevicecontroller-cacheddevices">CachedDevices</a>
</td>
<td align="left" width="63%">
Retrieves a collection of <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice">IBasicDevice</a> interface pointers that represents the cached view of all discoverable DLNA devices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828907(v=vs.85)">remove_DeviceArrival</a>
</td>
<td align="left" width="63%">
Unregisters an event handler for the <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/devicearrival">DeviceArrival</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828908(v=vs.85)">remove_DeviceDeparture</a>
</td>
<td align="left" width="63%">
Unregisters an event handler for the <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/devicedeparture">DeviceDeparture</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828906(v=vs.85)">RemoveDevice</a>
</td>
<td align="left" width="63%">
Removes the specified device from the list of devices that is returned by the <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/idevicecontroller-cacheddevices">CachedDevices</a> method.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>
 

 

