---
UID: NN:propsys.IPropertyEnumTypeList
title: IPropertyEnumTypeList
author: windows-driver-content
description: Exposes methods that enumerate the possible values for a property.
old-location: properties\IPropertyEnumTypeList.htm
old-project: properties
ms.assetid: 5df237a8-6468-43ee-870c-11b39e5e9dd9
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: IPropertyEnumTypeList, IPropertyEnumTypeList interface [Windows Properties], IPropertyEnumTypeList interface [Windows Properties],described, properties.IPropertyEnumTypeList, propsys/IPropertyEnumTypeList, shell.IPropertyEnumTypeList, shell_IPropertyEnumTypeList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Propsys.h
api_name:
-	IPropertyEnumTypeList
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0.6001 or later)
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPropertyEnumTypeList interface


## -description


Exposes methods that enumerate the possible values for a property.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyEnumTypeList</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPropertyEnumTypeList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyEnumTypeList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyEnumTypeList_FindMatchingIndex">FindMatchingIndex</a>
</td>
<td align="left" width="63%">
Compares the specified property value against the enumerated values in a list and returns the matching index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406567">GetAt</a>
</td>
<td align="left" width="63%">
Gets the <a href="shell.IPropertyEnumType">IPropertyEnumType</a> object at the specified index in the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyEnumTypeList_GetConditionAt">GetConditionAt</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of elements in the list.

</td>
</tr>
</table> 

