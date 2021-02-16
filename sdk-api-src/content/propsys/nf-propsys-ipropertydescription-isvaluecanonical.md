---
UID: NF:propsys.IPropertyDescription.IsValueCanonical
title: IPropertyDescription::IsValueCanonical (propsys.h)
description: Gets a value that indicates whether a property is canonical according to the definition of the property description.
old-location: properties\IPropertyDescription_IsValueCanonical.htm
tech.root: properties
ms.assetid: e0eedb58-82ed-4481-8319-633ddf20949c
ms.date: 12/05/2018
ms.keywords: IPropertyDescription interface [Windows Properties],IsValueCanonical method, IPropertyDescription.IsValueCanonical, IPropertyDescription::IsValueCanonical, IsValueCanonical, IsValueCanonical method [Windows Properties], IsValueCanonical method [Windows Properties],IPropertyDescription interface, properties.IPropertyDescription_IsValueCanonical, propsys/IPropertyDescription::IsValueCanonical, shell.IPropertyDescription_IsValueCanonical, shell_IPropertyDescription_IsValueCanonical
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertyDescription::IsValueCanonical
 - propsys/IPropertyDescription::IsValueCanonical
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyDescription.IsValueCanonical
---

# IPropertyDescription::IsValueCanonical


## -description

Gets a value that indicates whether a property is canonical according to the definition of the property description.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

A reference to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure that contains the type and value of the property.

## -returns

Type: <b>HRESULT</b>

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The value is canonical.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The value is not canonical.

</td>
</tr>
</table>