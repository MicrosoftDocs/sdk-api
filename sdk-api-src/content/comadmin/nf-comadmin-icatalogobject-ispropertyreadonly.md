---
UID: NF:comadmin.ICatalogObject.IsPropertyReadOnly
title: ICatalogObject::IsPropertyReadOnly (comadmin.h)
description: Indicates whether the specified property can be modified using Value.
helpviewer_keywords: ["ICatalogObject interface [COM+]","IsPropertyReadOnly method","ICatalogObject.IsPropertyReadOnly","ICatalogObject::IsPropertyReadOnly","IsPropertyReadOnly","IsPropertyReadOnly method [COM+]","IsPropertyReadOnly method [COM+]","ICatalogObject interface","_cos_ICatalogObject_IsPropertyReadOnly","comadmin/ICatalogObject::IsPropertyReadOnly","cos.icatalogobject_ispropertyreadonly"]
old-location: cos\icatalogobject_ispropertyreadonly.htm
tech.root: cos
ms.assetid: bd088794-1245-4cb8-a1f7-385354640675
ms.date: 12/05/2018
ms.keywords: ICatalogObject interface [COM+],IsPropertyReadOnly method, ICatalogObject.IsPropertyReadOnly, ICatalogObject::IsPropertyReadOnly, IsPropertyReadOnly, IsPropertyReadOnly method [COM+], IsPropertyReadOnly method [COM+],ICatalogObject interface, _cos_ICatalogObject_IsPropertyReadOnly, comadmin/ICatalogObject::IsPropertyReadOnly, cos.icatalogobject_ispropertyreadonly
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
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
 - ICatalogObject::IsPropertyReadOnly
 - comadmin/ICatalogObject::IsPropertyReadOnly
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICatalogObject.IsPropertyReadOnly
---

# ICatalogObject::IsPropertyReadOnly


## -description

Indicates whether the specified property can be modified using <a href="/windows/desktop/api/comadmin/nf-comadmin-icatalogobject-get_value">Value</a>.

## -parameters

### -param bstrPropName [in]

The name of the property to be modified.

### -param pbRetVal [out, retval]

If this value is True, you cannot modify the property. Otherwise, you can modify the property.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icatalogobject">ICatalogObject</a>