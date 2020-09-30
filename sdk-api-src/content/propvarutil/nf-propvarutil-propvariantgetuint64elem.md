---
UID: NF:propvarutil.PropVariantGetUInt64Elem
title: PropVariantGetUInt64Elem function (propvarutil.h)
description: Extracts a single unsigned Int64 element from a PROPVARIANT structure of type VT_UI8, VT_VECTOR | VT_UI8, or VT_ARRAY | VT_UI8.
helpviewer_keywords: ["PropVariantGetUInt64Elem","PropVariantGetUInt64Elem function [Windows Properties]","_shell_PropVariantGetUInt64Elem","properties.PropVariantGetUInt64Elem","propvarutil/PropVariantGetUInt64Elem","shell.PropVariantGetUInt64Elem"]
old-location: properties\PropVariantGetUInt64Elem.htm
tech.root: properties
ms.assetid: 35955104-b567-4c4f-850a-0a4778673ce8
ms.date: 12/05/2018
ms.keywords: PropVariantGetUInt64Elem, PropVariantGetUInt64Elem function [Windows Properties], _shell_PropVariantGetUInt64Elem, properties.PropVariantGetUInt64Elem, propvarutil/PropVariantGetUInt64Elem, shell.PropVariantGetUInt64Elem
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
 - PropVariantGetUInt64Elem
 - propvarutil/PropVariantGetUInt64Elem
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
 - PropVariantGetUInt64Elem
---

# PropVariantGetUInt64Elem function


## -description

Extracts a single unsigned Int64 element from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure of type VT_UI8, VT_VECTOR | VT_UI8, or VT_ARRAY | VT_UI8.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

The source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param iElem [in]

Type: <b>ULONG</b>

The vector or array index; otherwise, <i>iElem</i> must be 0.

### -param pnVal [out]

Type: <b>ULONGLONG*</b>

When this function returns, contains the extracted Int64 value.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

## -remarks

This helper function works for <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structures of the following types: 

                

<ul>
<li>VT_UI8</li>
<li>VT_VECTOR | VT_UI8</li>
<li>VT_ARRAY | VT_UI8</li>
</ul>
If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type VT_UI8, <i>iElem</i> must be 0. Otherwise <i>iElem</i> must be less than the number of elements in the vector or array. You can use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetelementcount">PropVariantGetElementCount</a> to obtain the number of elements in the vector or array.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetuint64elem">PropVariantGetUInt64Elem</a> with an iteration statement to access the values in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid

if ((propvar.vt & VT_TYPEMASK) == VT_UI8)
{
    UINT cElem = PropVariantGetElementCount(propvar);
    HRESULT hr = <mark type="const">S_OK</mark>;

    for (UINT iElem = 0; SUCCEEDED(hr) && iElem < cElem; iElem ++)
    {
        ULONGLONG nValue;
        hr = PropVariantGetUInt64Elem(propvar, iElem, &nValue);

        if (SUCCEEDED(hr))
        {
            // nValue is valid now
        }
    }
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetelem">PropVariantGetElem</a>