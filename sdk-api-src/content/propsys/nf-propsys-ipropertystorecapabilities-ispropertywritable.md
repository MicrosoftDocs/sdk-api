---
UID: NF:propsys.IPropertyStoreCapabilities.IsPropertyWritable
title: IPropertyStoreCapabilities::IsPropertyWritable (propsys.h)
description: Queries whether the property handler allows a specific property to be edited in the UI by the user.
helpviewer_keywords: ["IPropertyStoreCapabilities interface [Windows Properties]","IsPropertyWritable method","IPropertyStoreCapabilities.IsPropertyWritable","IPropertyStoreCapabilities::IsPropertyWritable","IsPropertyWritable","IsPropertyWritable method [Windows Properties]","IsPropertyWritable method [Windows Properties]","IPropertyStoreCapabilities interface","_shell_IPropertyStoreCapabilities_IsPropertyWritable","properties.IPropertyStoreCapabilities_IsPropertyWritable","propsys/IPropertyStoreCapabilities::IsPropertyWritable","shell.IPropertyStoreCapabilities_IsPropertyWritable"]
old-location: properties\IPropertyStoreCapabilities_IsPropertyWritable.htm
tech.root: properties
ms.assetid: ffd13c93-3011-4955-ad1e-2731afd83956
ms.date: 12/05/2018
ms.keywords: IPropertyStoreCapabilities interface [Windows Properties],IsPropertyWritable method, IPropertyStoreCapabilities.IsPropertyWritable, IPropertyStoreCapabilities::IsPropertyWritable, IsPropertyWritable, IsPropertyWritable method [Windows Properties], IsPropertyWritable method [Windows Properties],IPropertyStoreCapabilities interface, _shell_IPropertyStoreCapabilities_IsPropertyWritable, properties.IPropertyStoreCapabilities_IsPropertyWritable, propsys/IPropertyStoreCapabilities::IsPropertyWritable, shell.IPropertyStoreCapabilities_IsPropertyWritable
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
 - IPropertyStoreCapabilities::IsPropertyWritable
 - propsys/IPropertyStoreCapabilities::IsPropertyWritable
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
 - IPropertyStoreCapabilities.IsPropertyWritable
---

# IPropertyStoreCapabilities::IsPropertyWritable


## -description

Queries whether the property handler allows a specific property to be edited in the UI by the user.

## -parameters

### -param key [in]

Type: <b>REFPROPERTYKEY</b>

A reference to <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure that represents the property being queried.

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
The property can be edited and stored by the handler.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The property cannot be edited.

</td>
</tr>
</table>

## -remarks

The Shell disables the editing of controls by the user as appropriate through this method. A handler that does not support <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystorecapabilities">IPropertyStoreCapabilities</a> is assumed to support writing of any property.