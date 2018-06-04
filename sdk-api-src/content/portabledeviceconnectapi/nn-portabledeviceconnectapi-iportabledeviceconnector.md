---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IPortableDeviceConnector interface


## -description


The <b>IPortableDeviceConnector</b> interface defines methods used for connection-management and property-retrieval for a paired MTP/Bluetooth device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceConnector</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPortableDeviceConnector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDeviceConnector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406716">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a pending request to connect or disconnect an MTP Bluetooth device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2bb5b124-3018-4619-bb8f-67fcfc8981d9">Connect</a>
</td>
<td align="left" width="63%">
Sends an asynchronous connection request to the MTP Bluetooth device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0cc104e6-5e3a-4fce-ba3b-68f3fb94196b">Disconnect</a>
</td>
<td align="left" width="63%">
Sends an asynchronous disconnect request to the MTP Bluetooth device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39e7702a-f23e-4f04-8524-06a0fcc025a1">GetPnPID</a>
</td>
<td align="left" width="63%">
Retrieves the connector's Plug and Play (PnP) device identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7503df7a-826c-4e77-b51a-6b3d618732ca">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves a bus-level property for the given MTP Bluetooth device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/045268e1-3e91-41a9-a14e-eb20b8a707e4">SetProperty</a>
</td>
<td align="left" width="63%">
Sets a property for the given MTP Bluetooth Bus Enumerator device.

</td>
</tr>
</table> 

