---
UID: NF:propvarutil.PropVariantGetUInt16Elem
title: PropVariantGetUInt16Elem function (propvarutil.h)
description: Extracts a single unsigned Int16 element from a PROPVARIANT structure of type VT_U12, VT_VECTOR | VT_U12, or VT_ARRAY | VT_U12.
helpviewer_keywords: ["PropVariantGetUInt16Elem","PropVariantGetUInt16Elem function [Windows Properties]","_shell_PropVariantGetUInt16Elem","properties.PropVariantGetUInt16Elem","propvarutil/PropVariantGetUInt16Elem","shell.PropVariantGetUInt16Elem"]
old-location: properties\PropVariantGetUInt16Elem.htm
tech.root: properties
ms.assetid: da50e35b-f17f-4de6-b2e7-5a885e2149e5
ms.date: 12/05/2018
ms.keywords: PropVariantGetUInt16Elem, PropVariantGetUInt16Elem function [Windows Properties], _shell_PropVariantGetUInt16Elem, properties.PropVariantGetUInt16Elem, propvarutil/PropVariantGetUInt16Elem, shell.PropVariantGetUInt16Elem
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
 - PropVariantGetUInt16Elem
 - propvarutil/PropVariantGetUInt16Elem
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
 - PropVariantGetUInt16Elem
---

# PropVariantGetUInt16Elem function


## -description

Extracts a single unsigned Int16 element from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure of type VT_U12, VT_VECTOR | VT_U12, or VT_ARRAY | VT_U12.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param iElem [in]

Type: <b>ULONG</b>

The vector or array index; otherwise, <i>iElem</i> must be 0.

### -param pnVal [out]

Type: <b>USHORT*</b>

When this function returns, contains the extracted element value.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This helper function works for <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structures of the following types: 
            
                

<ul>
<li>VT_UI2</li>
<li>VT_VECTOR | VT_UI2</li>
<li>VT_ARRAY | VT_UI2</li>
</ul>
If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type VT_UI2, iElem must be 0. Otherwise iElem must be less than the number of elements in the vector or array. You can use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetelementcount">PropVariantGetElementCount</a> to obtain the number of elements in the vector or array.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetuint16elem">PropVariantGetUInt16Elem</a> with an iteration statement to access the values in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// PROPVARIANT propvar;
// Assume propvar is initialized and valid;

if ((propvar.vt & VT_TYPEMASK) == VT_UI2)
{
    UINT cElem = PropVariantGetElementCount(propvar);
    HRESULT hr = <mark type="const">S_OK</mark>;

    for (UINT iElem = 0; SUCCEEDED(hr) && iElem < cElem; iElem ++)
    {
        USHORT nValue;
        hr = PropVariantGetUInt16Elem(propvar, iElem, &nValue);

        if (SUCCEEDED(hr))
        {
            // nValue is valid now
        }
    }
}
```