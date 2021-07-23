---
UID: NF:propvarutil.PropVariantGetBooleanElem
title: PropVariantGetBooleanElem function (propvarutil.h)
description: Extracts a single Boolean element from a PROPVARIANT structure of type VT_BOOL, VT_VECTOR | VT_BOOL, or VT_ARRAY | VT_BOOL.
helpviewer_keywords: ["PropVariantGetBooleanElem","PropVariantGetBooleanElem function [Windows Properties]","_shell_PropVariantGetBooleanElem","properties.PropVariantGetBooleanElem","propvarutil/PropVariantGetBooleanElem","shell.PropVariantGetBooleanElem"]
old-location: properties\PropVariantGetBooleanElem.htm
tech.root: properties
ms.assetid: 830dca70-1777-418d-b3ac-78028411700e
ms.date: 12/05/2018
ms.keywords: PropVariantGetBooleanElem, PropVariantGetBooleanElem function [Windows Properties], _shell_PropVariantGetBooleanElem, properties.PropVariantGetBooleanElem, propvarutil/PropVariantGetBooleanElem, shell.PropVariantGetBooleanElem
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
 - PropVariantGetBooleanElem
 - propvarutil/PropVariantGetBooleanElem
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
 - PropVariantGetBooleanElem
---

# PropVariantGetBooleanElem function


## -description

Extracts a single Boolean element from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure of type <code>VT_BOOL</code>, <code>VT_VECTOR | VT_BOOL</code>, or <code>VT_ARRAY | VT_BOOL</code>.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

A reference to the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param iElem [in]

Type: <b>ULONG</b>

Specifies the vector or array index; otherwise, <i>iElem</i> must be 0.

### -param pfVal [out]

Type: <b>BOOL*</b>

When this function returns, contains the extracted Boolean value.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure has type <code>VT_BOOL</code>, <i>iElem</i> must be 0. Otherwise <i>iElem</i> must be less than the number of elements in the vector or array. You can use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetelementcount">PropVariantGetElementCount</a> to obtain the number of elements in the vector or array.

The following example uses this function to loop through the values in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.


#### Examples


```cpp
// PROPVARIANT propvar;
// assume propvar is initialized and valid

if ((propvar.vt & VT_TYPEMASK) == VT_BOOL)
{
    UINT cElem = PropVariantGetElementCount(propvar);
    HRESULT hr = <mark type="const">S_OK</mark>;
    
    for (UINT iElem = 0; SUCCEEDED(hr) && iElem < cElem; iElem ++)
    {
        BOOL fValue;
        hr = PropVariantGetBooleanElem(propvar, iElem, &fValue);
    
        if (SUCCEEDED(hr))
        {
            // fValue is valid now
        }
    }
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetelem">PropVariantGetElem</a>