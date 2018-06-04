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

# IUIAutomation3 interface


## -description


Extends the <a href="https://msdn.microsoft.com/45B4D41E-9C5C-47C7-86EB-D7B9BA14211B">IUIAutomation2</a> interface to expose additional methods for controlling Microsoft UI Automation functionality.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomation3</b> interface inherits from <a href="https://msdn.microsoft.com/45B4D41E-9C5C-47C7-86EB-D7B9BA14211B">IUIAutomation2</a>. <b>IUIAutomation3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomation3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E4FBD04E-2E0B-6B87-F589-C3214EF54E5F">AddTextEditTextChangedEventHandler</a>
</td>
<td align="left" width="63%">
Registers a method that handles programmatic text-edit events.

<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://msdn.microsoft.com/0772969a-da55-488e-8b21-7368434df8a9">Understanding Threading Issues</a>.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CCB8C8FC-B0CF-2C3D-64B5-9CCF1BB64058">RemoveTextEditTextChangedEventHandler</a>
</td>
<td align="left" width="63%">
Removes a programmatic text-edit event handler.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/45B4D41E-9C5C-47C7-86EB-D7B9BA14211B">IUIAutomation2</a>



<a href="https://msdn.microsoft.com/dd7cdcf1-3511-424f-b729-b71a7e11cdd8">UI Automation Element Interfaces for Clients</a>
 

 

