---
UID: NN:propsys.IPropertyEnumType
title: IPropertyEnumType (propsys.h)
description: Exposes methods that extract data from enumeration information. IPropertyEnumType gives access to the enum and enumRange elements in the property schema in a programmatic way at run time.
helpviewer_keywords: ["IPropertyEnumType","IPropertyEnumType interface [Windows Properties]","IPropertyEnumType interface [Windows Properties]","described","_shell_IPropertyEnumType","properties.IPropertyEnumType","propsys/IPropertyEnumType","shell.IPropertyEnumType"]
old-location: properties\IPropertyEnumType.htm
tech.root: properties
ms.assetid: 05ae6763-a3e1-461d-af90-08bddbe82300
ms.date: 12/05/2018
ms.keywords: IPropertyEnumType, IPropertyEnumType interface [Windows Properties], IPropertyEnumType interface [Windows Properties],described, _shell_IPropertyEnumType, properties.IPropertyEnumType, propsys/IPropertyEnumType, shell.IPropertyEnumType
f1_keywords:
- propsys/IPropertyEnumType
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
- IPropertyEnumType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyEnumType interface


## -description


Exposes methods that extract data from enumeration information. <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertyenumtype">IPropertyEnumType</a> gives access to the <a href="https://docs.microsoft.com/windows/desktop/properties/propdesc-schema-enum">enum</a> and <a href="https://docs.microsoft.com/windows/desktop/properties/propdesc-schema-enumrange">enumRange</a> elements in the <a href="https://docs.microsoft.com/windows/desktop/properties/propdesc-schema-entry">property schema</a> in a programmatic way at run time.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyEnumType</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPropertyEnumType</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertyenumtype-getdisplaytext">GetDisplayText</a>
</td>
<td align="left" width="63%">
Gets display text from an enumeration information structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertyenumtype-getenumtype">GetEnumType</a>
</td>
<td align="left" width="63%">
Gets an enumeration type from an enumeration information structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertyenumtype-getrangeminvalue">GetRangeMinValue</a>
</td>
<td align="left" width="63%">
Gets a minimum value from an enumeration information structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertyenumtype-getrangesetvalue">GetRangeSetValue</a>
</td>
<td align="left" width="63%">
Gets a set value from an enumeration information structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-getvalue">GetValue</a>
</td>
<td align="left" width="63%">
Gets a value from an enumeration information structure.

</td>
</tr>
</table> 


## -remarks



For additional information, see <a href="https://docs.microsoft.com/windows/desktop/properties/propdesc-schema-enumeratedlist">enumeratedList</a>.



