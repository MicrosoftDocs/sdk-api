---
UID: NF:propvarutil.PropVariantToStrRet
title: PropVariantToStrRet function (propvarutil.h)
description: Extracts a string from a PROPVARIANT structure and places it into a STRRET structure.
helpviewer_keywords: ["PropVariantToStrRet","PropVariantToStrRet function [Windows Properties]","_shell_PropVariantToStrRet","properties.PropVariantToStrRet","propvarutil/PropVariantToStrRet","shell.PropVariantToStrRet"]
old-location: properties\PropVariantToStrRet.htm
tech.root: properties
ms.assetid: a1a33606-172d-4ee7-98c9-ffec8eed98bf
ms.date: 12/05/2018
ms.keywords: PropVariantToStrRet, PropVariantToStrRet function [Windows Properties], _shell_PropVariantToStrRet, properties.PropVariantToStrRet, propvarutil/PropVariantToStrRet, shell.PropVariantToStrRet
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
 - PropVariantToStrRet
 - propvarutil/PropVariantToStrRet
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
 - PropVariantToStrRet
---

# PropVariantToStrRet function


## -description

Extracts a string from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure and places it into a <a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> structure.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param pstrret [out]

Type: <b><a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a>*</b>

Points to the <a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> structure. When this function returns, the structure has been initialized to contain a copy of the extracted string.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This helper function is used in applications that wish to convert a string value in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure into a <a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> structure. For instance, an application implementing <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof">IShellFolder::GetDisplayNameOf</a> may find this function useful.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type VT_LPWSTR or VT_BSTR, this function extracts the string and places it into the <a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> structure. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a string. If a conversion is not possible, <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostring">PropVariantToString</a> will return a failure code. See <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a> for a list of possible conversions. Of note, VT_EMPTY is successfully converted to "".

In addition to the conversions provided by <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a>, the following special cases apply to <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostring">PropVariantToString</a>. 
        

<ul>
<li>Vector-valued <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>s are converted to strings by separating each element with using "; ". For example, <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostring">PropVariantToString</a> converts a vector of 3 integers, {3, 1, 4}, to the string "3; 1; 4". The semicolon is independent of the current locale.</li>
<li>VT_BLOB, VT_STREAM, VT_STREAMED_OBJECT, and VT_UNKNOWN values are converted to strings using an unsupported encoding. It is not possible to decode strings created in this way and the format may change in the future.</li>
</ul>
If the extraction is successful, the function will initialize uType member of the <a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> structure with STRRET_WSTR and set the pOleStr member of that structure to point to an allocated copy of the string. The calling application is responsible for using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> or <a href="/windows/desktop/api/shlwapi/nf-shlwapi-strrettostra">StrRetToStr</a> to free this string when it is no longer needed. 


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostring">PropVariantToString</a> to access a string value in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// IPropertyStore *ppropstore;

// Assume variable ppropstore is initialized and valid

PROPVARIANT propvar = {0};

HRESULT hr = ppropstore->GetValue(PKEY_FileName, &propvar);

if (SUCCEEDED(hr))

{

    // PKEY_FileName is expected to produce a VT_LPWSTR or VT_EMPTY value.

    // PropVariantToStrRet will convert VT_EMPTY to "".

    // If this were an implementation of IShellFolder::GetDisplayNameOf, strName would be a parameter and the caller would free the memory associated with the STRRET

    STRRET strName;

    hr = PropVariantToStrRet(propvar, &strName);

    if (SUCCEEDED(hr))

    {

        // strName is now valid

 

        if (strName.uType == STRRET_WSTR)

        {

            CoTaskMemFree(strName.pOleStr);

        }

    }

    else

    {

        // the extraction failed

    }

    PropVariantClear(&propvar);

}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromstring">InitPropVariantFromString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetstringelem">PropVariantGetStringElem</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostring">PropVariantToString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostringalloc">PropVariantToStringAlloc</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostringvector">PropVariantToStringVector</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-strrettostra">StrRetToStr</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttostrret">VariantToStrRet</a>