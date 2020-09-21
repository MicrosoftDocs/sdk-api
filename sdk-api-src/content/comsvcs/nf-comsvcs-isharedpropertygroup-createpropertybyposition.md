---
UID: NF:comsvcs.ISharedPropertyGroup.CreatePropertyByPosition
title: ISharedPropertyGroup::CreatePropertyByPosition (comsvcs.h)
description: Creates a new shared property with the specified index.
helpviewer_keywords: ["CreatePropertyByPosition","CreatePropertyByPosition method [COM+]","CreatePropertyByPosition method [COM+]","ISharedPropertyGroup interface","ISharedPropertyGroup interface [COM+]","CreatePropertyByPosition method","ISharedPropertyGroup.CreatePropertyByPosition","ISharedPropertyGroup::CreatePropertyByPosition","_cos_ISharedPropertyGroup_CreatePropertyByPosition","comsvcs/ISharedPropertyGroup::CreatePropertyByPosition","cos.isharedpropertygroup_createpropertybyposition"]
old-location: cos\isharedpropertygroup_createpropertybyposition.htm
tech.root: cos
ms.assetid: 47e0e230-0952-4afb-a757-af387a7cddfb
ms.date: 12/05/2018
ms.keywords: CreatePropertyByPosition, CreatePropertyByPosition method [COM+], CreatePropertyByPosition method [COM+],ISharedPropertyGroup interface, ISharedPropertyGroup interface [COM+],CreatePropertyByPosition method, ISharedPropertyGroup.CreatePropertyByPosition, ISharedPropertyGroup::CreatePropertyByPosition, _cos_ISharedPropertyGroup_CreatePropertyByPosition, comsvcs/ISharedPropertyGroup::CreatePropertyByPosition, cos.isharedpropertygroup_createpropertybyposition
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
 - ISharedPropertyGroup::CreatePropertyByPosition
 - comsvcs/ISharedPropertyGroup::CreatePropertyByPosition
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
 - ISharedPropertyGroup.CreatePropertyByPosition
---

# ISharedPropertyGroup::CreatePropertyByPosition


## -description

Creates a new shared property with the specified index. If a shared property with the specified index already exists, <b>CreatePropertyByPosition</b> returns a reference to the existing one.

## -parameters

### -param Index [in]

The numeric index within the <a href="/windows/desktop/cossdk/sharedpropertygroup">SharedPropertyGroup</a> object by which the new property is referenced. You can use this index later to retrieve the shared property with the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-isharedpropertygroup-get_propertybyposition">get_PropertyByPosition</a> method.

### -param fExists [out]

A reference to a Boolean value. If <i>fExists</i> is set to VARIANT_TRUE on return from this method, the shared property specified by <i>Index</i> existed prior to this call. If it is set to VARIANT_FALSE, the property was created by this call.

### -param ppProp [out]

A reference to a shared property object identified by the numeric index passed in the <i>Index</i> parameter, or <b>NULL</b> if an error is encountered.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

When you create a shared property, its value is set to the default, which is a VT_I4 VARIANT with a value of 0.



If you create a <a href="/windows/desktop/cossdk/sharedproperty">SharedProperty</a> object with the <b>CreatePropertyByPosition</b> method, you can access that property only by using the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-isharedpropertygroup-get_propertybyposition">get_PropertyByPosition</a> method. You cannot assign a string name to the same property and then access it by using the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-isharedpropertygroup-get_property">get_Property</a> method. Accessing a property by position is faster than accessing a property by using a string name because it requires less overhead.

The same shared property group can contain some <a href="/windows/desktop/cossdk/sharedproperty">SharedProperty</a> objects that are identified by position and others that are identified by name.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isharedproperty">ISharedProperty</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isharedpropertygroup">ISharedPropertyGroup</a>