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

# IPropertyEnumType interface


## -description


Exposes methods that extract data from enumeration information. <a href="shell.IPropertyEnumType">IPropertyEnumType</a> gives access to the <a href="https://msdn.microsoft.com/c8cc040e-fcce-43a0-98c1-db2b2c616ac3">enum</a> and <a href="shell.propdesc_schema_enumRange">enumRange</a> elements in the <a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">property schema</a> in a programmatic way at run time.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyEnumType</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPropertyEnumType</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyEnumType</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyEnumType_GetDisplayText">GetDisplayText</a>
</td>
<td align="left" width="63%">
Gets display text from an enumeration information structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyEnumType_GetEnumType">GetEnumType</a>
</td>
<td align="left" width="63%">
Gets an enumeration type from an enumeration information structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyEnumType_GetRangeMinValue">GetRangeMinValue</a>
</td>
<td align="left" width="63%">
Gets a minimum value from an enumeration information structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyEnumType_GetRangeSetValue">GetRangeSetValue</a>
</td>
<td align="left" width="63%">
Gets a set value from an enumeration information structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597624">GetValue</a>
</td>
<td align="left" width="63%">
Gets a value from an enumeration information structure.

</td>
</tr>
</table> 


## -remarks



For additional information, see <a href="shell.propdesc_schema_enumeratedList">enumeratedList</a>.



