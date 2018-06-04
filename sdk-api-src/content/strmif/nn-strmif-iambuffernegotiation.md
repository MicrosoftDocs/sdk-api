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

# IAMBufferNegotiation interface


## -description



The <code>IAMBufferNegotiation</code> interface requests the number of buffers for a filter to create and size of each buffer. This interface can be exposed by any pin that connects using the <a href="https://msdn.microsoft.com/a4407c6f-6bb5-4274-920b-8bf7d76268bc">IMemInputPin</a> pin interface, but is typically exposed on the output pins of capture filters.

When two pins connect through <b>IMemInputPin</b>, they agree on an allocator object that is responsible for creating buffers. Normally this process is transparent to the application, but in some situations the application needs more control. If a pin exposes <code>IAMBufferNegotiation</code>, the application can suggest how many buffers to create, the size of the buffers, and other properties. If your application performs preview of captured audio, you can specify a smaller buffer size to reduce latency. Teleconferencing applications should specify a minimal number of buffers.

To use this interface, call the <b>SuggestAllocatorProperties</b> method before the pins connect. After the pins connect, call the <b>GetAllocatorProperties</b> method to determine whether the pin honored the request.

<b>Filter developers</b>: Capture filters should always support this interface when possible.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMBufferNegotiation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMBufferNegotiation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMBufferNegotiation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85bbb900-772c-4091-83e3-f2a5dd198d39">GetAllocatorProperties</a>
</td>
<td align="left" width="63%">
Retrieves the allocator properties that the pin is using.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f6a7f2c4-be8b-4721-87f4-274ba365784f">SuggestAllocatorProperties</a>
</td>
<td align="left" width="63%">
Informs the pin of the application's preferred allocator properties

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

