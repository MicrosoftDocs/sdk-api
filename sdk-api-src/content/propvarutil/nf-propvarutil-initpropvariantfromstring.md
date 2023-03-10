---
UID: NF:propvarutil.InitPropVariantFromString
title: InitPropVariantFromString function (propvarutil.h)
description: Initializes a PROPVARIANT structure based on a specified string.
helpviewer_keywords: ["InitPropVariantFromString","InitPropVariantFromString function [Windows Properties]","properties.InitPropVariantFromString","propvarutil/InitPropVariantFromString","shell.InitPropVariantFromString","shell_InitPropVariantFromString"]
old-location: properties\InitPropVariantFromString.htm
tech.root: properties
ms.assetid: eeb1002c-d06b-4f7f-b850-4c33f6e0d7aa
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromString, InitPropVariantFromString function [Windows Properties], properties.InitPropVariantFromString, propvarutil/InitPropVariantFromString, shell.InitPropVariantFromString, shell_InitPropVariantFromString
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - InitPropVariantFromString
 - propvarutil/InitPropVariantFromString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propvarutil.h
api_name:
 - InitPropVariantFromString
---

# InitPropVariantFromString function


## -description

Initializes a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure based on a specified string.

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

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromstring">InitPropVariantFromString</a>.


```cpp
PROPVARIANT propvar;
HRESULT hr = InitPropVariantFromString(L"Hello World", &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_LPWSTR.
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromstringasvector">InitPropVariantFromStringAsVector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromstringvector">InitPropVariantFromStringVector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromstring">InitVariantFromString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostring">PropVariantToString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostringwithdefault">PropVariantToStringWithDefault</a>