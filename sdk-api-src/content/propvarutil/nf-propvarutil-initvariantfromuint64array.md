---
UID: NF:propvarutil.InitVariantFromUInt64Array
title: InitVariantFromUInt64Array function (propvarutil.h)
description: Initializes a VARIANT structure with an array of unsigned 64-bit integer values.
helpviewer_keywords: ["InitVariantFromUInt64Array","InitVariantFromUInt64Array function [Windows Properties]","_shell_InitVariantFromUInt64Array","properties.InitVariantFromUInt64Array","propvarutil/InitVariantFromUInt64Array","shell.InitVariantFromUInt64Array"]
old-location: properties\InitVariantFromUInt64Array.htm
tech.root: properties
ms.assetid: 67886e29-c3dd-4bfd-b53f-761c16daaf63
ms.date: 12/05/2018
ms.keywords: InitVariantFromUInt64Array, InitVariantFromUInt64Array function [Windows Properties], _shell_InitVariantFromUInt64Array, properties.InitVariantFromUInt64Array, propvarutil/InitVariantFromUInt64Array, shell.InitVariantFromUInt64Array
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
 - InitVariantFromUInt64Array
 - propvarutil/InitVariantFromUInt64Array
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
 - InitVariantFromUInt64Array
---

# InitVariantFromUInt64Array function


## -description

Initializes a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure with an array of unsigned 64-bit integer values.

## -parameters

### -param prgn [in]

Type: <b>const ULONGLONG*</b>

Pointer to the source array of <b>ULONGLONG</b> values.

### -param cElems [in]

Type: <b>ULONG</b>

The number of elements in the array pointed to by <i>prgn</i>.

### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_ARRAY | VT_UI8 variant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromuint64array">InitVariantFromUInt64Array</a>.


```cpp
ULONGLONG rgLongs[] = {4, 2};
VARIANT var;

HRESULT hr = InitVariantFromUInt64Array(rgLongs, ARRAYSIZE(rgLongs), &var);

if (SUCCEEDED(hr))                            
{
    // var now is valid and has type VT_ARRAY | VT_UI8.
    VariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromuint64vector">InitPropVariantFromUInt64Vector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromuint64">InitVariantFromUInt64</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttouint64array">VariantToUInt64Array</a>