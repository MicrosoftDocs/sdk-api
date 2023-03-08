---
UID: NF:propvarutil.PropVariantGetStringElem
title: PropVariantGetStringElem function (propvarutil.h)
description: Extracts a single Unicode string element from a PROPVARIANT structure of type VT_LPWSTR, VT_BSTR, VT_VECTOR | VT_LPWSTR, VT_VECTOR | VT_BSTR, or VT_ARRAY | VT_BSTR.
helpviewer_keywords: ["PropVariantGetStringElem","PropVariantGetStringElem function [Windows Properties]","_shell_PropVariantGetStringElem","properties.PropVariantGetStringElem","propvarutil/PropVariantGetStringElem","shell.PropVariantGetStringElem"]
old-location: properties\PropVariantGetStringElem.htm
tech.root: properties
ms.assetid: 6e803d93-5b55-4b73-8e23-a584f5f91969
ms.date: 12/05/2018
ms.keywords: PropVariantGetStringElem, PropVariantGetStringElem function [Windows Properties], _shell_PropVariantGetStringElem, properties.PropVariantGetStringElem, propvarutil/PropVariantGetStringElem, shell.PropVariantGetStringElem
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
 - PropVariantGetStringElem
 - propvarutil/PropVariantGetStringElem
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
 - PropVariantGetStringElem
---

# PropVariantGetStringElem function


## -description

Extracts a single Unicode string element from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure of type VT_LPWSTR, VT_BSTR, VT_VECTOR | VT_LPWSTR, VT_VECTOR | VT_BSTR, or VT_ARRAY | VT_BSTR.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param iElem [in]

Type: <b>ULONG</b>

The vector or array index; otherwise, <i>iElem</i> must be 0.

### -param ppszVal [out]

Type: <b>PWSTR*</b>

When this function returns, contains the extracted string value. The calling application is responsible for freeing this string by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> when it is no longer needed.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This helper function works for <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structures of the following types: 

                

<ul>
<li>VT_LPWSTR</li>
<li>VT_BSTR</li>
<li>VT_VECTOR | VT_LPWSTR</li>
<li>VT_VECTOR | VT_BSTR</li>
<li>VT_ARRAY | VT_BSTR</li>
</ul>
If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type VT_LPWSTR or VT_BSTR, <i>iElem</i> must be 0. Otherwise <i>iElem</i> must be less than the number of elements in the vector or array. You can use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetelementcount">PropVariantGetElementCount</a> to obtain the number of elements in the vector or array.

If a BSTR element has a <b>NULL</b> pointer, this function allocates an empty string.


#### Examples

The following code example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetstringelem">PropVariantGetStringElem</a> with an iteration statement to access the values in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid

if ((propvar.vt & VT_TYPEMASK) == VT_LPWSTR || (propvar.vt & VT_TYPEMASK) == VT_BSTR)
{
    UINT cElem = PropVariantGetElementCount(propvar);
    HRESULT hr = <mark type="const">S_OK</mark>;

    for (UINT iElem = 0; SUCCEEDED(hr) && iElem < cElem; iElem ++)
    {
        PWSTR pszValue;
        hr = PropVariantGetStringElem(propvar, iElem, &pszValue);

        if (SUCCEEDED(hr))
        {
            // pszValue is valid now
            CoTaskMemFree(pszValue);
        }
    }
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetelem">PropVariantGetElem</a>