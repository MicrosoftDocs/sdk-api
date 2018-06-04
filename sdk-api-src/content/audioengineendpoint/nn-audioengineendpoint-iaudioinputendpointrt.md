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

# IAudioInputEndpointRT interface


## -description


Gets the input buffer for each processing pass.The 
    <b>IAudioInputEndpointRT</b> interface is used by the 
    audio engine.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioInputEndpointRT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioInputEndpointRT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioInputEndpointRT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1da81a49-d421-4643-9be6-b13d45d678f0">GetInputDataPointer</a>
</td>
<td align="left" width="63%">
Gets a pointer to the buffer from which data will be read by the audio engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b23eac3-48e2-4d58-be6c-878967e7fa5c">PulseEndpoint</a>
</td>
<td align="left" width="63%">
This method is  reserved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9dd3f72a-79fe-4d07-a301-d0960e30a2d1">ReleaseInputDataPointer</a>
</td>
<td align="left" width="63%">
Releases the acquired data pointer.

</td>
</tr>
</table> 


## -remarks



<b>IAudioInputEndpointRT</b> methods can be called 
     from a real-time processing thread. The implementation of the methods of this interface must not block, access 
     paged memory, or call any blocking system routines.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client 
    applications.



