---
UID: NN:shobjidl_core.IPropertyUI
title: IPropertyUI
author: windows-sdk-content
description: Developers should use IPropertyDescription instead.
old-location: properties\IPropertyUI.htm
old-project: properties
ms.assetid: FB3DD615-F08B-4cdb-A6EB-3458C474EBEE
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IPropertyUI, IPropertyUI interface [Windows Properties], IPropertyUI interface [Windows Properties],described, _shell_IPropertyUI, properties.IPropertyUI, shell.IPropertyUI, shobjidl_core/IPropertyUI
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl_core.h
api_name:
 - IPropertyUI
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
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

