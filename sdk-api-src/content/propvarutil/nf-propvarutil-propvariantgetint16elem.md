---
UID: NF:propvarutil.PropVariantGetInt16Elem
title: PropVariantGetInt16Elem function (propvarutil.h)
description: Extracts a single Int16 element from a PROPVARIANT structure of type VT_I2, VT_VECTOR | VT_I2, or VT_ARRAY | VT_I2.
helpviewer_keywords: ["PropVariantGetInt16Elem","PropVariantGetInt16Elem function [Windows Properties]","_shell_PropVariantGetInt16Elem","properties.PropVariantGetInt16Elem","propvarutil/PropVariantGetInt16Elem","shell.PropVariantGetInt16Elem"]
old-location: properties\PropVariantGetInt16Elem.htm
tech.root: properties
ms.assetid: 1dbb6887-81c9-411d-9fce-c9e2f3479a43
ms.date: 12/05/2018
ms.keywords: PropVariantGetInt16Elem, PropVariantGetInt16Elem function [Windows Properties], _shell_PropVariantGetInt16Elem, properties.PropVariantGetInt16Elem, propvarutil/PropVariantGetInt16Elem, shell.PropVariantGetInt16Elem
req.header: propvarutil.h
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
 - PropVariantGetInt16Elem
 - propvarutil/PropVariantGetInt16Elem
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
 - PropVariantGetInt16Elem
---

# PropVariantGetInt16Elem function


## -description

Extracts a single Int16 element from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure of type VT_I2, VT_VECTOR | VT_I2, or  VT_ARRAY | VT_I2.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param iElem [in]

Type: <b>ULONG</b>

The vector or array index; otherwise, this value must be 0.

### -param pnVal [out]

Type: <b>SHORT*</b>

When this function returns, contains the extracted Int32 element value.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This helper function works for <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structures of the following types.
                

<ul>
<li>VT_I2</li>
<li>VT_VECTOR | VT_I2</li>
<li>VT_ARRAY | VT_I2</li>
</ul>
If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type VT_I2, <i>iElem</i> must be 0. Otherwise, <i>iElem</i> must be less than the number of elements in the vector or array. You can use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetelementcount">PropVariantGetElementCount</a> to obtain the number of elements in the vector or array.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetint16elem">PropVariantGetInt16Elem</a> with an iteration statement to access the values in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// PROPVARIANT propvar;
    // Assume propvar is initialized and valid;
    
    if ((propvar.vt & VT_TYPEMASK) == VT_I2)
    {
        UINT cElem = PropVariantGetElementCount(propvar);
        HRESULT hr = <mark type="const">S_OK</mark>;
    
        for (UINT iElem = 0; SUCCEEDED(hr) && iElem < cElem; iElem ++)
        {
            SHORT nValue;
            hr = PropVariantGetInt16Elem(propvar, iElem, &nValue);
    
            if (SUCCEEDED(hr))
            {
                // nValue is valid now
            }
        }
    }
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetelem">PropVariantGetElem</a>