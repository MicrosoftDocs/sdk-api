---
UID: NF:comsvcs.ISharedPropertyGroup.get_Property
title: ISharedPropertyGroup::get_Property (comsvcs.h)
description: Retrieves a reference to an existing shared property with the specified name.
helpviewer_keywords: ["ISharedPropertyGroup interface [COM+]","get_Property method","ISharedPropertyGroup.get_Property","ISharedPropertyGroup::get_Property","_cos_ISharedPropertyGroup_get_Property","comsvcs/ISharedPropertyGroup::get_Property","cos.isharedpropertygroup_get_property","get_Property","get_Property method [COM+]","get_Property method [COM+]","ISharedPropertyGroup interface"]
old-location: cos\isharedpropertygroup_get_property.htm
tech.root: cos
ms.assetid: ffbd82a8-35d5-4c9b-bf03-91f48dddc189
ms.date: 12/05/2018
ms.keywords: ISharedPropertyGroup interface [COM+],get_Property method, ISharedPropertyGroup.get_Property, ISharedPropertyGroup::get_Property, _cos_ISharedPropertyGroup_get_Property, comsvcs/ISharedPropertyGroup::get_Property, cos.isharedpropertygroup_get_property, get_Property, get_Property method [COM+], get_Property method [COM+],ISharedPropertyGroup interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - ISharedPropertyGroup::get_Property
 - comsvcs/ISharedPropertyGroup::get_Property
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISharedPropertyGroup.get_Property
---

# ISharedPropertyGroup::get_Property


## -description

Retrieves a reference to an existing shared property with the specified name.

## -parameters

### -param Name [in]

The name that was used to create the shared property that is retrieved.

### -param ppProperty [out]

A reference to the shared property specified in the <i>Name</i> parameter, or <b>NULL</b> if the property does not exist.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_FAIL, as well as the following values.

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
The shared property exists, and a reference to it is returned in the <i>ppProperty</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The shared property with the name specified in the <i>Name</i> parameter does not exist.


</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isharedproperty">ISharedProperty</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isharedpropertygroup">ISharedPropertyGroup</a>