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

# IPropertyDescription2 interface


## -description


Exposes methods that enumerate and retrieve individual property description details.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyDescription2</b> interface inherits from <a href="shell.IPropertyDescription">IPropertyDescription</a>. <b>IPropertyDescription2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyDescription2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyDescription2_GetImageReferenceForValue">GetImageReferenceForValue</a>
</td>
<td align="left" width="63%">
Gets the image reference associated with a property value.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="shell.IPropertyDescription">IPropertyDescription</a> interface, from which it inherits.

To obtain this interface, call <a href="shell.PSGetPropertyDescription">PSGetPropertyDescription</a>, <a href="shell.PSGetPropertyDescriptionByName">PSGetPropertyDescriptionByName</a>, or <a href="shell.IPropertyDescriptionList_GetAt">IPropertyDescriptionList::GetAt</a>.

Only one property description exists for each property in the system.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Do not implement this interface. There is only one implementation of <a href="shell.IPropertyDescription">IPropertyDescription</a> in the system; it is provided by the Shell.




## -see-also




<a href="shell.IPropertyDescription">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 

