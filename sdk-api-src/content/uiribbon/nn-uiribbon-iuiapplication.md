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

# IUIApplication interface


## -description


The <b>IUIApplication</b> interface is implemented by the application and defines the callback entry-point methods for the Windows Ribbon framework.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIApplication</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIApplication</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIApplication</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13e03acd-1a1e-48f9-b413-5a24d8b784d0">OnCreateUICommand</a>
</td>
<td align="left" width="63%">

			Called for each Command specified in the Ribbon framework markup to bind the Command to an <a href="https://msdn.microsoft.com/cd739f99-b3f2-4ddb-a844-eb888d9c7f67">IUICommandHandler</a>.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c25f2279-1227-4ce2-9787-c046479b3a33">OnDestroyUICommand</a>
</td>
<td align="left" width="63%">
Called for each Command specified in the Ribbon framework markup when the application window is destroyed.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9672131d-bc7a-4e7b-935e-cd38dff2bb5c">OnViewChanged</a>
</td>
<td align="left" width="63%">
Called when the state of a  <a href="https://msdn.microsoft.com/library/windows/hardware/dn927297">View</a> changes.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/79d092c9-347b-4b8f-8ba4-a8f696ce6a85">Windows Ribbon Framework Samples</a>
 

 

