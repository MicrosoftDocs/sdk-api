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

# ITfComposition interface


## -description


The <b>ITfComposition</b> interface is implemented by the TSF manager and is used by a text service to obtain data about and terminate a <a href="https://msdn.microsoft.com/3d9da4f2-ceb9-4abc-8979-d3756d948a57">composition</a>. An instance of this interface is provided by the <a href="https://msdn.microsoft.com/aab84e6c-39c7-438e-b4f0-1d174473aa02">ITfContextComposition::StartComposition</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfComposition</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfComposition</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfComposition</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5717c03-2611-4199-b07d-b6f3b6f65d3a">EndComposition</a>
</td>
<td align="left" width="63%">
Terminates a composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14a726c3-6531-4d49-9f22-20460be02b81">GetRange</a>
</td>
<td align="left" width="63%">
Obtains a range object that contains the text covered by the composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40472318-85de-4cff-ac60-adfcbacc1537">ShiftEnd</a>
</td>
<td align="left" width="63%">
Moves the end anchor of a composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85a5121a-7be0-4703-a1d4-4de21dd98697">ShiftStart</a>
</td>
<td align="left" width="63%">
Moves the start anchor of a composition.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3d9da4f2-ceb9-4abc-8979-d3756d948a57">Compositions</a>



<a href="https://msdn.microsoft.com/aab84e6c-39c7-438e-b4f0-1d174473aa02">ITfContextComposition::StartComposition
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

