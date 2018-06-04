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

# ISyncMgrConflict interface


## -description


Exposes methods that provide information about a conflict retrieved from a conflict store, and allows the conflict to be resolved.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrConflict</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncMgrConflict</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrConflict</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9686a6e5-5a0a-4520-803e-1660676d9f61">GetConflictIdInfo</a>
</td>
<td align="left" width="63%">
Gets information that identifies a conflict within a conflict store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c836522-fb04-4176-a9b3-7602ae2d71a1">GetItemsArray</a>
</td>
<td align="left" width="63%">
Retrieves a conflict items array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b7b23e7-fbd4-4ced-9610-d001a2167bae">GetProperty</a>
</td>
<td align="left" width="63%">
Gets a conflict property, given a property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9adbc429-098c-4ba9-af62-54f772be83e3">GetResolutionHandler</a>
</td>
<td align="left" width="63%">
Gets the resolution handler for the conflict.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9680b96e-9a83-45e1-a2bf-674aff6490ec">Resolve</a>
</td>
<td align="left" width="63%">
Resolves the conflict using its own sync handler, controls UI.

</td>
</tr>
</table> 

