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

# IPropertyUI interface


## -description


Developers should use <a href="shell.IPropertyDescription">IPropertyDescription</a> instead.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyUI</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPropertyUI</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyUI</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyUI_FormatForDisplay">FormatForDisplay</a>
</td>
<td align="left" width="63%">
Developers should use <a href="shell.IPropertyDescription">IPropertyDescription</a> instead. Gets a formatted, Unicode string representation of a property value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyUI_GetCanonicalName">GetCanonicalName</a>
</td>
<td align="left" width="63%">
Developers should use <a href="shell.IPropertyDescription">IPropertyDescription</a> instead. Gets the canonical name of the property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyUI_GetDefaultWidth">GetDefaultWidth</a>
</td>
<td align="left" width="63%">
Developers should use <a href="shell.IPropertyDescription">IPropertyDescription</a> instead. Gets the width of the property description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyUI_GetDisaplayName">GetDisplayName</a>
</td>
<td align="left" width="63%">
Developers should use <a href="shell.IPropertyDescription">IPropertyDescription</a> instead. Gets a string specifying the name of the property suitable for display to users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546791">GetFlags</a>
</td>
<td align="left" width="63%">
Developers should use <a href="shell.IPropertyDescription">IPropertyDescription</a> instead. Gets property feature flags for a specified property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyUI_GetHelpInfo">GetHelpInfo</a>
</td>
<td align="left" width="63%">
Developers should use <a href="shell.IPropertyDescription">IPropertyDescription</a> instead. Gets

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyUI_GetPropertyDescription">GetPropertyDescription</a>
</td>
<td align="left" width="63%">
Developers should use <a href="shell.IPropertyDescription">IPropertyDescription</a> instead. Gets the property description of a specified property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyUI_ParsePropertyName">ParsePropertyName</a>
</td>
<td align="left" width="63%">
Developers should use <a href="shell.IPropertyDescription">IPropertyDescription</a> instead. Reads the characters of the specified property name and identifies the FMTID and PROPID of the property.

</td>
</tr>
</table> 

