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

# _IManipulationEvents interface


## -description


Handles manipulation and inertia events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">_IManipulationEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>_IManipulationEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>_IManipulationEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1284df32-f4e8-43b3-b825-9172ad39f0e6">ManipulationCompleted</a>
</td>
<td align="left" width="63%">
Handles the event when manipulation or inertia finishes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bebac896-c48d-4e6e-98ce-4b7d1dec101c">ManipulationDelta</a>
</td>
<td align="left" width="63%">
Handles events that happen when a manipulated object changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3e63eb7-65e7-4394-89e4-d95d7e7877cf">ManipulationStarted</a>
</td>
<td align="left" width="63%">
Handles the event when manipulation or inertia begins.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/056bcaa2-580a-457c-a0a6-e01a316dc21a">Classes and Interfaces</a>
 

 

