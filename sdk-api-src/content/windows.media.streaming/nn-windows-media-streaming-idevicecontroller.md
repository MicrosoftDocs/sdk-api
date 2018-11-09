---
UID: NN:windows.media.streaming.IDeviceController
title: IDeviceController
author: windows-sdk-content
description: Encapsulates the methods and events needed to retrieve a list of cached Digital Media Renderers (DMRs) and/or Digital Media Servers (DMSs), or to asynchronously find the DMRs and/or DMSs that are currently on the network.
old-location: mediastreaming\idevicecontroller.htm
tech.root: mediastreaming
ms.assetid: 18989598-86C5-4BD7-B8F4-27496897DFBA
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IDeviceController, IDeviceController interface [Media Streaming API], IDeviceController interface [Media Streaming API],described, mediastreaming.idevicecontroller, windows/IDeviceController
ms.prod: windows
ms.technology: windows-sdk
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
 - IDeviceController
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDeviceController interface


## -description


Encapsulates the methods and events  needed to retrieve a list of cached Digital Media Renderers (DMRs) and/or Digital Media Servers (DMSs), or to asynchronously find the DMRs and/or DMSs that are currently on the network.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDeviceController</b> interface inherits from <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>. <b>IDeviceController</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/968A30D5-42ED-472B-9436-EBC77A3F76C9">add_DeviceArrival</a>
</td>
<td align="left" width="63%">
Registers an event handler for the <a href="https://msdn.microsoft.com/C7CB49AE-C05F-4A2A-8A30-4B4BB7C7D9D2">DeviceArrival</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3DCE2BA9-1F94-45F2-97B7-64BD62B21578">add_DeviceDeparture</a>
</td>
<td align="left" width="63%">
Registers an event handler for the <a href="https://msdn.microsoft.com/10451878-E685-4042-9F92-BA3A408C4DA0">DeviceDeparture</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9D7DD7C2-21C0-4DD2-BB71-613203097692">AddDevice</a>
</td>
<td align="left" width="63%">
Adds a DLNA DMR or DMS Device, identified by its UPnP Unique Device Name (UDN), to the list of devices that is returned by the <a href="https://msdn.microsoft.com/94C2A7FF-5AF8-4F13-BBA5-54ED78C3BBF6">CachedDevices</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94C2A7FF-5AF8-4F13-BBA5-54ED78C3BBF6">CachedDevices</a>
</td>
<td align="left" width="63%">
Retrieves a collection of <a href="https://msdn.microsoft.com/E4F99A11-4ED5-44CB-BE16-CBB558412ED4">IBasicDevice</a> interface pointers that represents the cached view of all discoverable DLNA devices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D1026B13-627C-4FD4-A402-C05E42CF3DCF">remove_DeviceArrival</a>
</td>
<td align="left" width="63%">
Unregisters an event handler for the <a href="https://msdn.microsoft.com/C7CB49AE-C05F-4A2A-8A30-4B4BB7C7D9D2">DeviceArrival</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42C7E011-ABC8-493E-853A-0925D2A94118">remove_DeviceDeparture</a>
</td>
<td align="left" width="63%">
Unregisters an event handler for the <a href="https://msdn.microsoft.com/10451878-E685-4042-9F92-BA3A408C4DA0">DeviceDeparture</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07002D00-4E7B-4679-A521-A6F4B3148923">RemoveDevice</a>
</td>
<td align="left" width="63%">
Removes the specified device from the list of devices that is returned by the <a href="https://msdn.microsoft.com/94C2A7FF-5AF8-4F13-BBA5-54ED78C3BBF6">CachedDevices</a> method.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>
 

 

