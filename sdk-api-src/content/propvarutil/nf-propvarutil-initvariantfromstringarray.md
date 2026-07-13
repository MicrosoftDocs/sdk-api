---
UID: NF:propvarutil.InitVariantFromStringArray
title: InitVariantFromStringArray function (propvarutil.h)
description: Initializes a VARIANT structure with an array of strings.
helpviewer_keywords: ["InitVariantFromStringArray","InitVariantFromStringArray function [Windows Properties]","_shell_InitVariantFromStringArray","properties.InitVariantFromStringArray","propvarutil/InitVariantFromStringArray","shell.InitVariantFromStringArray"]
old-location: properties\InitVariantFromStringArray.htm
tech.root: properties
ms.assetid: f46cfc71-9e27-4ba1-8a32-5b279b628732
ms.date: 12/05/2018
ms.keywords: InitVariantFromStringArray, InitVariantFromStringArray function [Windows Properties], _shell_InitVariantFromStringArray, properties.InitVariantFromStringArray, propvarutil/InitVariantFromStringArray, shell.InitVariantFromStringArray
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
 - InitVariantFromStringArray
 - propvarutil/InitVariantFromStringArray
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
 - InitVariantFromStringArray
---

# InitVariantFromStringArray function


## -description

Initializes a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure with an array of strings.

## -parameters

### -param prgsz [in]

Type: <b>PCWSTR*</b>

Pointer to an array of strings.

### -param cElems [in]

Type: <b>ULONG</b>

The number of elements in the array pointed to by <i>prgsz</i>.

### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_ARRAY | VT_BSTR variant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromstringarray">InitVariantFromStringArray</a>.


```cpp
PCWSTR rgStrings[] = {"dog", "cat"};
VARIANT var;

HRESULT hr = InitVariantFromStringArray(rgStrings, ARRAYSIZE(rgStrings), &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_ARRAY | VT_BSTR.
    VariantClear(&var);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromstring">InitPropVariantFromString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromstring">InitVariantFromString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttostringarray">VariantToStringArray</a>