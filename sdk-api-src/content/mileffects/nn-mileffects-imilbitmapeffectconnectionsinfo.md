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

# IMILBitmapEffectConnectionsInfo interface


## -description


Exposes methods that retrieves information about what input and output pins are exposed by the bitmap effect. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMILBitmapEffectConnectionsInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMILBitmapEffectConnectionsInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMILBitmapEffectConnectionsInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25456764-a237-4375-ae00-12d2db2f1a67">GetInputConnectorInfo</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/18f9260d-b7cd-4b45-a7bd-f3bd3647eebe">IMILBitmapEffectConnectorInfo</a> associated with the given input pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12a9aa29-0027-4275-8e0c-07335d10da0f">GetNumberInputs</a>
</td>
<td align="left" width="63%">
Retrieves the number of input pins the bitmap effect implements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/329395a7-a63a-4501-88ec-1a87d97ec281">GetNumberOutputs</a>
</td>
<td align="left" width="63%">
Retrieves the number of output pins the bitmap effect implements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/400c7153-af46-4067-b9f9-18fe0930760d">GetOutputConnectorInfo</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/18f9260d-b7cd-4b45-a7bd-f3bd3647eebe">IMILBitmapEffectConnectorInfo</a> associated with the given output pin.

</td>
</tr>
</table> 


## -remarks



If this interface is not implemented when creating a custom bitmap effect, a single input and output pin implementation with a 32bit RGBA format is assumes.



