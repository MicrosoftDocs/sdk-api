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

# IAccessibleEx interface


## -description


Exposes methods that are called by Microsoft UI Automation to retrieve extra information about a control that supports Microsoft Active Accessibility.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAccessibleEx</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAccessibleEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAccessibleEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eafda7ed-b18c-4d52-9d1c-a9d1a2d5dfd1">ConvertReturnedElement</a>
</td>
<td align="left" width="63%">
Retrieves the <b>IAccessibleEx</b> interface of an element returned as a property value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/282de8b1-67ce-42e3-9f17-dbd29374d910">GetIAccessiblePair</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface and child ID for this item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fbb279cc-2224-437e-875b-d08df175edf1">GetObjectForChild</a>
</td>
<td align="left" width="63%">
Retrieves an <b>IAccessibleEx</b> interface representing the specified child of this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00aeac66-398a-4c80-85e2-32bff0ae100f">GetRuntimeId</a>
</td>
<td align="left" width="63%">
Retrieves the runtime identifier of this element.

</td>
</tr>
</table> 


## -remarks



This interface can be implemented on custom controls that also implement the <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface, to provide added support for UI Automation without the cost of a full UI Automation provider implementation.
	




## -see-also




<a href="https://msdn.microsoft.com/7ceab704-3e02-4550-b236-748e4f0a092a">Adding UI Automation Functionality to Active Accessibility Servers</a>
 

 

