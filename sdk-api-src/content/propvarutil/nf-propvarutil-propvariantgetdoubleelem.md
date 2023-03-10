---
UID: NF:propvarutil.PropVariantGetDoubleElem
title: PropVariantGetDoubleElem function (propvarutil.h)
description: Extracts a single double element from a PROPVARIANT structure of type VT_R8, VT_VECTOR | VT_R8, or VT_ARRAY | VT_R8.
helpviewer_keywords: ["PropVariantGetDoubleElem","PropVariantGetDoubleElem function [Windows Properties]","_shell_PropVariantGetDoubleElem","properties.PropVariantGetDoubleElem","propvarutil/PropVariantGetDoubleElem","shell.PropVariantGetDoubleElem"]
old-location: properties\PropVariantGetDoubleElem.htm
tech.root: properties
ms.assetid: 387e23df-bfbd-42c0-adef-dc53ba95a9f2
ms.date: 12/05/2018
ms.keywords: PropVariantGetDoubleElem, PropVariantGetDoubleElem function [Windows Properties], _shell_PropVariantGetDoubleElem, properties.PropVariantGetDoubleElem, propvarutil/PropVariantGetDoubleElem, shell.PropVariantGetDoubleElem
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
 - PropVariantGetDoubleElem
 - propvarutil/PropVariantGetDoubleElem
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
 - PropVariantGetDoubleElem
---

# PropVariantGetDoubleElem function


## -description

Extracts a single <b>double</b> element from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure of type <code>VT_R8</code>, <code>VT_VECTOR | VT_R8</code>, or <code>VT_ARRAY | VT_R8</code>.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param iElem [in]

Type: <b>ULONG</b>

Specifies vector or array index; otherwise, <i>iElem</i> must be 0.

### -param pnVal [out]

Type: <b>DOUBLE*</b>

When this function returns, contains the extracted double value.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type <code>VT_R8</code>, <i>iElem</i> must be 0. Otherwise <i>iElem</i> must be less than the number of elements in the vector or array. You can use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetelementcount">PropVariantGetElementCount</a> to obtain the number of elements in the vector or array.

The following example uses this function to loop through the values in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.


#### Examples


```cpp
// PROPVARIANT propvar;
// assume propvar is initialized and valid

if ((propvar.vt & VT_TYPEMASK) == VT_R8)
{
    UINT cElem = PropVariantGetElementCount(propvar);
    HRESULT hr = <mark type="const">S_OK</mark>;
    
    for (UINT iElem = 0; SUCCEEDED(hr) && iElem < cElem; iElem ++)
    {
        DOUBLE nValue;
        hr = PropVariantGetDoubleElem(propvar, iElem, &nValue);
    
        if (SUCCEEDED(hr))
        {
            // nValue is valid now
        }
    }
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetelem">PropVariantGetElem</a>