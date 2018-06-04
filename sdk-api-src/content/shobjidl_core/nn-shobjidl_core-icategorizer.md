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

# ICategorizer interface


## -description


Exposes methods that are used to obtain information about item identifier lists.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICategorizer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICategorizer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICategorizer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25775fa5-595d-4911-9cd4-47fde429b923">CompareCategory</a>
</td>
<td align="left" width="63%">
Determines the relative order of two items in their item identifier lists, and hence in the UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3756e9e-7d68-4e30-92d4-1fddccf66ba5">GetCategory</a>
</td>
<td align="left" width="63%">
Gets a list of categories associated with a list of identifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b789033-ce42-4fb5-8a3d-b05243b62d4e">GetCategoryInfo</a>
</td>
<td align="left" width="63%">
Gets information about a category, such as the default display and the text to display in the UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546575">GetDescription</a>
</td>
<td align="left" width="63%">
Gets the name of a categorizer, such as <i>Group By Device Type</i>, that can be displayed in the UI.

</td>
</tr>
</table> 

