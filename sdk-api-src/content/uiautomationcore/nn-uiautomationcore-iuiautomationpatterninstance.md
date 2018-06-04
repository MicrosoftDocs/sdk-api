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

# IUIAutomationPatternInstance interface


## -description


Represents a control pattern object. The client API wrapper uses this interface to implement all property and method calls in terms of the <a href="https://msdn.microsoft.com/cb64569f-799b-4e9a-a9f4-84513b98c941">GetProperty</a> and <a href="https://msdn.microsoft.com/a3c1aa20-c512-4752-8da6-c8e86bd56beb">CallMethod</a> methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationPatternInstance</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationPatternInstance</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationPatternInstance</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3c1aa20-c512-4752-8da6-c8e86bd56beb">CallMethod</a>
</td>
<td align="left" width="63%">
Client wrapper implements methods by calling this CallMethod function, specifying the parameters as an array of pointers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb64569f-799b-4e9a-a9f4-84513b98c941">GetProperty</a>
</td>
<td align="left" width="63%">
The client wrapper object implements the <b>IUIAutomation::get_Current</b><i>X</i> and <b>IUIAutomationElement::get_Cached</b><i>X</i> methods by calling this function, specifying the property by index. 

</td>
</tr>
</table> 


## -remarks



This interface is implemented by Microsoft UI Automation and returned by methods such as <a href="https://msdn.microsoft.com/3ad4df7c-979d-464f-9600-d1f3de064b59">GetCurrentPattern</a>. The interface is passed to <a href="https://msdn.microsoft.com/03530381-52f8-4d9b-a54c-faebf7cd4a06">CreateClientWrapper</a>, where it is used to call the appropriate methods and property getters.




## -see-also




<a href="https://msdn.microsoft.com/14358ef0-aa54-42c1-a3da-0f835f5f5ef6">Control Pattern Interfaces for Clients</a>
 

 

