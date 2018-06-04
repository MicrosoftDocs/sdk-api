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

# IItemContainerProvider interface


## -description


Provides access to controls that act as containers of other controls, such as a virtual list-view.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IItemContainerProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IItemContainerProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IItemContainerProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2873bbb-5bb4-4eaa-b0bd-60061fc06f53">FindItemByProperty</a>
</td>
<td align="left" width="63%">
Retrieves an element within a containing element, based on a specified property value.

</td>
</tr>
</table> 


## -remarks



The <a href="https://msdn.microsoft.com/6f3dd94e-3563-4a13-9db9-5928a02bab77">ItemContainer</a> control pattern allows a container object to efficiently lookup an item by a 
		specified automation element property, such as Name, AutomationId, or IsSelected state. While this control 
		pattern is introduced with a view to being used by virtualized containers, it can be implemented by any container 
		that provides name lookup, independently of whether that container uses virtualization.




## -see-also




<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

