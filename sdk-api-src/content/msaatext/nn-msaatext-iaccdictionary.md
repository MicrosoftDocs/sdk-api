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

# IAccDictionary interface


## -description


<p class="CCE_Message">[Active Accessibility Text Services is deprecated. Please see     
<a href="http://go.microsoft.com/fwlink/p/?linkid=131573">Microsoft Windows Text Services Framework</a>
for more information on advanced text input and natural language technologies.
		]

Exposes methods for string manipulation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAccDictionary</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAccDictionary</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAccDictionary</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30ac7ba4-9968-40dd-99d2-8600d25ade20">ConvertValueToString</a>
</td>
<td align="left" width="63%">
Converts a property value to a localized string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7419395d-d4be-4ee4-bf98-aef7e82cb3d5">GetLocalizedString</a>
</td>
<td align="left" width="63%">
Retrieves a localized string for a system property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4855acea-83a9-4752-a780-7f0350a7b137">GetMnemonicString</a>
</td>
<td align="left" width="63%">
Retrieves a mnemonic string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/202058e8-50c2-4366-9bb6-bbc46dc5ea3f">GetParentTerm</a>
</td>
<td align="left" width="63%">
Retrieves the parent object of a specified property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8a4dfde-3721-4bf5-a609-12f06154b5f0">LookupMnemonicTerm</a>
</td>
<td align="left" width="63%">
Retrieves the property for a given mnemonic string.

</td>
</tr>
</table> 

