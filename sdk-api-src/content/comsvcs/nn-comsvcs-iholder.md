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

# IHolder interface


## -description


Allocates or frees resources for an installed Resource Dispenser. The Dispenser Manager exposes a different <b>IHolder</b> interface to each installed Resource Dispenser.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IHolder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IHolder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IHolder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b6c5d54-4917-460f-9740-abe4b578761f">AllocResource</a>
</td>
<td align="left" width="63%">
Allocates a resource from the inventory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
Closes the Holder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d110bf6-7204-4fbb-abb7-ced7cf885e5b">FreeResource</a>
</td>
<td align="left" width="63%">
Returns a resource to the inventory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1602718-2221-4e49-a57c-f65f87174dc9">RequestDestroyResource</a>
</td>
<td align="left" width="63%">
Deletes a resource, calling its destructor to free memory and other associated system resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c87727a-fefd-4ef6-964c-3379d22178c2">TrackResource</a>
</td>
<td align="left" width="63%">
Tracks the resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1971820f-49aa-455d-a533-1a88fd8c28b8">TrackResourceS</a>
</td>
<td align="left" width="63%">
Tracks the resource (string version).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/380b09ad-08d6-4d25-8d80-0e56d4295b8f">UntrackResource</a>
</td>
<td align="left" width="63%">
Stops tracking a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03e54d2d-9dfb-46cf-abb9-d3f37784c449">UnTrackResourceS</a>
</td>
<td align="left" width="63%">
Stops tracking a resource (string version).

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/dba9c616-031d-48a7-b3e3-eb28b95a573a">IDispenserDriver</a>



<a href="https://msdn.microsoft.com/a0465d78-f8b7-4934-9dc6-c8f0ead04bf1">IDispenserManager</a>
 

 

