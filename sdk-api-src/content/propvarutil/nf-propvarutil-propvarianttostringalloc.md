---
UID: NF:propvarutil.PropVariantToStringAlloc
title: PropVariantToStringAlloc function (propvarutil.h)
description: Extracts a string property value from a PROPVARIANT structure.
helpviewer_keywords: ["PropVariantToStringAlloc","PropVariantToStringAlloc function [Windows Properties]","_shell_PropVariantToStringAlloc","properties.PropVariantToStringAlloc","propvarutil/PropVariantToStringAlloc","shell.PropVariantToStringAlloc"]
old-location: properties\PropVariantToStringAlloc.htm
tech.root: properties
ms.assetid: 5e47cc72-4179-4ebe-8700-87861146b3d7
ms.date: 12/05/2018
ms.keywords: PropVariantToStringAlloc, PropVariantToStringAlloc function [Windows Properties], _shell_PropVariantToStringAlloc, properties.PropVariantToStringAlloc, propvarutil/PropVariantToStringAlloc, shell.PropVariantToStringAlloc
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
 - PropVariantToStringAlloc
 - propvarutil/PropVariantToStringAlloc
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
 - PropVariantToStringAlloc
---

# PropVariantToStringAlloc function


## -description

Extracts a string property value from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param ppszOut [out]

Type: <b>PWSTR*</b>

When this function returns, contains a pointer to the extracted property value if one exists.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a string value.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type VT_LPWSTR or VT_BSTR, this function extracts the string into a newly allocated buffer. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a string. If a conversion is not possible, <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostringalloc">PropVariantToStringAlloc</a> will return a failure code and set <i>ppszOut</i> to <b>NULL</b>. See <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a> for a list of possible conversions. Of note, <b>VT_EMPTY</b> is successfully converted to an allocated buffer containing "".

The calling application is responsible for using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to release the string pointed to by <i>ppszOut</i> when it is no longer needed.

In addition to the conversions provided by <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a>, the following special cases apply to <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostringalloc">PropVariantToStringAlloc</a>. 
                

<ul>
<li>Vector-valued PROPVARIANTs are converted to strings by separating each element with using "; ". For example, <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostringalloc">PropVariantToStringAlloc</a> converts a vector of 3 integers, {3, 1, 4}, to the string "3; 1; 4". The semicolon is independent of the current locale.</li>
<li>VT_BLOB, VT_STREAM, VT_STREAMED_OBJECT, and VT_UNKNOWN values are converted to strings using an unsupported encoding. It is not possible to decode strings created in this way and the format may change in the future.</li>
</ul>

#### Examples


```cpp
// IPropertyStore *ppropstore;

// Assume variable ppropstore is initialized and valid

PROPVARIANT propvar = {0};

HRESULT hr = ppropstore->GetValue(PKEY_Title, &propvar);

if (SUCCEEDED(hr))

{

    // PKEY_Title is expected to produce a VT_LPWSTR or VT_EMPTY value.

    // PropVariantToStringAlloc will convert VT_EMPTY to "".

    LPWSTR pszTitle;

    hr = PropVariantToString(propvar, &pszTitle);

    if (SUCCEEDED(hr))

    {

        // pszTitle is now valid

    }

    else

    {

        // pszTitle is always NULL

    }

    PropVariantClear(&propvar);

}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromstring">InitPropVariantFromString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostring">PropVariantToString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostringvector">PropVariantToStringVector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttostring">VariantToString</a>