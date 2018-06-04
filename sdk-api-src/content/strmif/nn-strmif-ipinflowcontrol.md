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

# IPinFlowControl interface


## -description



Blocks data flow from an active output pin. This interface is exposed by output pins that can reconnect dynamically. Use this interface to start a dynamic reconnection within the filter graph. For more information, see <a href="https://msdn.microsoft.com/13fed430-979b-40f7-91ba-aff2d811bd92">Dynamic Graph Building</a>.

<b>Filter developers: </b>Parser and capture filters that support dynamic reconnection should support this interface on their output pins. Generally, other types of filters do not need to implement this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPinFlowControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPinFlowControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPinFlowControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9bcd325d-41fc-4166-8fce-50fc921efdba">Block</a>
</td>
<td align="left" width="63%">
Blocks or unblocks the flow of data from the pin.

</td>
</tr>
</table> 

