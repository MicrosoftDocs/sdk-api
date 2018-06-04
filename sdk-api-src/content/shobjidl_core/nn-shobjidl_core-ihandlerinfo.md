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

# IHandlerInfo interface


## -description


Supplies methods that provide information about the handler to methods of the <a href="https://msdn.microsoft.com/4c60a3f8-48ec-4686-9e27-692f88cd1c55">IHandlerActivationHost</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IHandlerInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IHandlerInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IHandlerInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19b3b042-7c2d-4402-913e-daa5c8bba595">GetApplicationDisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the display name of the application that implemented the handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be886508-16a5-4a77-9fa4-b6a8d028c9e9">GetApplicationIconReference</a>
</td>
<td align="left" width="63%">
Retrieves the icon of the application that implemented the handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5e22afa-69eb-4cf5-98b0-f46e25fb136e">GetApplicationPublisher</a>
</td>
<td align="left" width="63%">
Retrieves the name of the publisher of the application that implemented the handler.

</td>
</tr>
</table> 

