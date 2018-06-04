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

# IInkLineInfo interface


## -description



          The <b>IInkLineInfo</b> interface provides access to the display properties and recognition result list of a text ink object (tInk).
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkLineInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkLineInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInkLineInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59005f51-7052-4aef-915d-4c939eecec99">GetCandidate</a>
</td>
<td align="left" width="63%">
Returns one word from the recognition alternates list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f894963-7075-46f4-8809-82d1aa7e13e7">GetFormat</a>
</td>
<td align="left" width="63%">
Returns the display properties currently set on the text ink object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0082b7d3-61b2-478a-a6dd-ba59c20b7e1d">GetInkExtent</a>
</td>
<td align="left" width="63%">
Specifies the display properties to set on the text ink object, and retrieves the width of the text ink object in <b>HIMETRIC</b> units.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6a0f559-72e8-40db-ba9a-0f1b27ba6a96">Recognize</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0301706b-6d3e-4fe4-af87-764b1c959707">SetCandidate</a>
</td>
<td align="left" width="63%">
Updates one recognition alternate in the recognition result list, either by replacing an existing alternate, or by adding an alternate to the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42e16e86-fc90-4089-9ae0-9a896cbeaccc">SetFormat</a>
</td>
<td align="left" width="63%">
Specifies the display properties to set on the text ink object.

</td>
</tr>
</table> 

