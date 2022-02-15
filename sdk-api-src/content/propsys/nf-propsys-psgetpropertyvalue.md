---
UID: NF:propsys.PSGetPropertyValue
title: PSGetPropertyValue function (propsys.h)
description: Gets a property value from a property store.
helpviewer_keywords: ["PSGetPropertyValue","PSGetPropertyValue function [Windows Properties]","_shell_PSGetPropertyValue","properties.PSGetPropertyValue","propsys/PSGetPropertyValue","shell.PSGetPropertyValue"]
old-location: properties\PSGetPropertyValue.htm
tech.root: properties
ms.assetid: 9369dc85-b006-4b30-a25e-58d53b76f334
ms.date: 12/05/2018
ms.keywords: PSGetPropertyValue, PSGetPropertyValue function [Windows Properties], _shell_PSGetPropertyValue, properties.PSGetPropertyValue, propsys/PSGetPropertyValue, shell.PSGetPropertyValue
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - PSGetPropertyValue
 - propsys/PSGetPropertyValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSGetPropertyValue
---

# PSGetPropertyValue function


## -description

Gets a property value from a property store.

## -parameters

### -param pps [in]

Type: <b><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>*</b>

Pointer to an instance of the <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface, which represents the property store from which to get the value.

### -param ppd [in]

Type: <b><a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>*</b>

Pointer to an instance of the <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a> interface, which represents the property in the property store.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

Pointer to an uninitialized <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure. When this function returns, points to the requested property value.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This helper function is used to read a property value from a store. If the calling code already has a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure, it might be simpler to call <a href="/windows/desktop/api/propsys/nf-propsys-ipropertystore-getvalue">IPropertyStore::GetValue</a> directly.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertyvalue">PSGetPropertyValue</a>.


```cpp
// IPropertyDescription *pPropDesc;
// IPropertyStore *pStore;
// Assume the variables pPropDesc and pStore are initialized and valid.
PROPVARIANT propvar;

HRESULT hr = PSGetPropertyValue(pStore, pPropDesc, &propvar);

if (SUCCEEDED(hr))
{
    // propvar is valid.
 
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-pssetpropertyvalue">PSSetPropertyValue</a>