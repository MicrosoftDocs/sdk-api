---
UID: NN:propsys.IPropertyEnumTypeList
title: IPropertyEnumTypeList (propsys.h)
description: Exposes methods that enumerate the possible values for a property.
helpviewer_keywords: ["IPropertyEnumTypeList","IPropertyEnumTypeList interface [Windows Properties]","IPropertyEnumTypeList interface [Windows Properties]","described","properties.IPropertyEnumTypeList","propsys/IPropertyEnumTypeList","shell.IPropertyEnumTypeList","shell_IPropertyEnumTypeList"]
old-location: properties\IPropertyEnumTypeList.htm
tech.root: properties
ms.assetid: 5df237a8-6468-43ee-870c-11b39e5e9dd9
ms.date: 12/05/2018
ms.keywords: IPropertyEnumTypeList, IPropertyEnumTypeList interface [Windows Properties], IPropertyEnumTypeList interface [Windows Properties],described, properties.IPropertyEnumTypeList, propsys/IPropertyEnumTypeList, shell.IPropertyEnumTypeList, shell_IPropertyEnumTypeList
f1_keywords:
- propsys/IPropertyEnumTypeList
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Propsys.h
api_name:
- IPropertyEnumTypeList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyEnumTypeList interface


## -description


Exposes methods that enumerate the possible values for a property.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyEnumTypeList</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPropertyEnumTypeList</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertyenumtypelist-findmatchingindex">FindMatchingIndex</a>
</td>
<td align="left" width="63%">
Compares the specified property value against the enumerated values in a list and returns the matching index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcolorprofileresourcecollection-getat">GetAt</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertyenumtype">IPropertyEnumType</a> object at the specified index in the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertyenumtypelist-getconditionat">GetConditionAt</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of elements in the list.

</td>
</tr>
</table> 

