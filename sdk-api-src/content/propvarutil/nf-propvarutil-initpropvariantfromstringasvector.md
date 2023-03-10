---
UID: NF:propvarutil.InitPropVariantFromStringAsVector
title: InitPropVariantFromStringAsVector function (propvarutil.h)
description: Initializes a PROPVARIANT structure from a specified string. The string is parsed as a semi-colon delimited list (for example:\_&quot;A;B;C&quot;).
helpviewer_keywords: ["InitPropVariantFromStringAsVector","InitPropVariantFromStringAsVector function [Windows Properties]","properties.InitPropVariantFromStringAsVector","propvarutil/InitPropVariantFromStringAsVector","shell.InitPropVariantFromStringAsVector","shell_InitPropVariantFromStringAsVector"]
old-location: properties\InitPropVariantFromStringAsVector.htm
tech.root: properties
ms.assetid: fc48f2e0-ce4a-4f48-a624-202def4bcff0
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromStringAsVector, InitPropVariantFromStringAsVector function [Windows Properties], properties.InitPropVariantFromStringAsVector, propvarutil/InitPropVariantFromStringAsVector, shell.InitPropVariantFromStringAsVector, shell_InitPropVariantFromStringAsVector
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
 - InitPropVariantFromStringAsVector
 - propvarutil/InitPropVariantFromStringAsVector
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
 - InitPropVariantFromStringAsVector
---

# InitPropVariantFromStringAsVector function


## -description

Initializes a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure from a specified string. The string is parsed as a semi-colon delimited list (for example: "A;B;C").

## -parameters

### -param psz [in]

Type: <b>PCWSTR</b>

Pointer to a buffer that contains the source Unicode string.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_VECTOR | VT_LPWSTR propvariant. It parses the source string as a semicolon list of values. The string "a; b; c" creates a vector with three values. Leading and trailing whitespace are removed, and empty values are omitted.

If <i>psz</i> is <b>NULL</b> or contains no values, the <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure is initialized as VT_EMPTY.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromstringasvector">InitPropVariantFromStringAsVector</a>.


```cpp
PROPVARIANT propvar;
HRESULT hr = InitPropVariantFromStringAsVector(L"a; b; c", &propvar);

if (SUCCEEDED(hr))
{
    // propvar now has type VT_VECTOR | VT_LPWSTR and contains {"a", "b", "c"}.
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromstring">InitPropVariantFromString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromstringvector">InitPropVariantFromStringVector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromstringarray">InitVariantFromStringArray</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostringvector">PropVariantToStringVector</a>