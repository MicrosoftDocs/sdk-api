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

# IAudioEndpointRT interface


## -description


Gets the difference between the current read and write positions in the endpoint buffer. The 
    <b>IAudioEndpointRT</b> interface is used by the audio 
    engine.

<b>IAudioEndpointRT</b> methods can be called from a 
    real-time processing thread. The implementation of the methods of this interface must not block, access paged 
    memory, or call any blocking system routines.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioEndpointRT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioEndpointRT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioEndpointRT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f61497c8-35da-4fbf-af83-1f15d5fe94f7">
        GetCurrentPadding</a>
</td>
<td align="left" width="63%">
Gets the amount, in 100-nanosecond units, of data that is queued up in the endpoint.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a9c52fa-27ff-4e63-ae87-f5a3cd8d4f9b">ProcessingComplete</a>
</td>
<td align="left" width="63%">
Notifies the endpoint that a processing pass has been completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c445b06-d576-4474-be8f-b984c43d3765">SetPinActive</a>
</td>
<td align="left" width="63%">
Notifies the endpoint that it must change the state of the underlying stream to an active state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07062063-cae1-4517-aeed-fb73ec602b27">SetPinInactive</a>
</td>
<td align="left" width="63%">
Notifies the endpoint that it must change the state of the underlying stream to an inactive state.

</td>
</tr>
</table> 


## -remarks



The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client 
    applications.



