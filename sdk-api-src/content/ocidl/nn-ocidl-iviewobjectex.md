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

# IViewObjectEx interface


## -description


An extension derived from <a href="https://msdn.microsoft.com/b150ca4b-c53c-4bcb-85fa-461f9fa8b63b">IViewObject2</a> to provide support for:
<ul>
<li>Enhanced, flicker-free drawing for non-rectangular objects and transparent objects</li>
<li>Hit testing for non-rectangular objects</li>
<li>Control sizing</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IViewObjectEx</b> interface inherits from <a href="https://msdn.microsoft.com/b150ca4b-c53c-4bcb-85fa-461f9fa8b63b">IViewObject2</a>. <b>IViewObjectEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IViewObjectEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5759c482-2dea-4b94-956d-9560f72acbd5">GetNaturalExtent</a>
</td>
<td align="left" width="63%">
Provides sizing hints from the container for the object to use as the user resizes it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff060cd2-c7e4-4c12-842a-663415b80c17">GetRect</a>
</td>
<td align="left" width="63%">
Retrieves a rectangle describing a requested drawing aspect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf8ec90c-07bb-4f60-93c9-4cee3fb5a056">GetViewStatus</a>
</td>
<td align="left" width="63%">
Retrieves information about the opacity of the object, and what drawing aspects are supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9ee26c4-cf5f-4ca9-b40a-0522097a2f07">QueryHitPoint</a>
</td>
<td align="left" width="63%">
Indicates whether a point is within a given aspect of an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb155424-e74c-497f-a9c0-33ed3b2b5513">QueryHitRect</a>
</td>
<td align="left" width="63%">
Indicates whether any point in a rectangle is within a given drawing aspect of an object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b150ca4b-c53c-4bcb-85fa-461f9fa8b63b">IViewObject2</a>
 

 

