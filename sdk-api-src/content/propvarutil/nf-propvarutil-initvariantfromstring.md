---
UID: NF:propvarutil.InitVariantFromString
title: InitVariantFromString function (propvarutil.h)
description: Initializes a VARIANT structure with a string.
helpviewer_keywords: ["InitVariantFromString","InitVariantFromString function [Windows Properties]","_shell_InitVariantFromString","properties.InitVariantFromString","propvarutil/InitVariantFromString","shell.InitVariantFromString"]
old-location: properties\InitVariantFromString.htm
tech.root: properties
ms.assetid: 2501399d-1d31-41ea-9943-f2a8042095c7
ms.date: 12/05/2018
ms.keywords: InitVariantFromString, InitVariantFromString function [Windows Properties], _shell_InitVariantFromString, properties.InitVariantFromString, propvarutil/InitVariantFromString, shell.InitVariantFromString
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
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - InitVariantFromString
 - propvarutil/InitVariantFromString
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
 - InitVariantFromString
---

# InitVariantFromString function


## -description

Initializes a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure with a string.

## -parameters

### -param psz [in]

Type: <b>PCWSTR</b>

Pointer to a buffer that contains the source Unicode string. If this value is <b>NULL</b>, the function initializes the <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> with a <b>NULL</b> <b>BSTR</b>.

### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_BSTR variant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromstring">InitVariantFromString</a>.


```cpp
VARIANT var;

HRESULT hr = InitVariantFromString(L"This is a test", &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_BSTR.
    VariantClear(&var);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromstring">InitPropVariantFromString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromstringarray">InitVariantFromStringArray</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttostring">VariantToString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttostringwithdefault">VariantToStringWithDefault</a>