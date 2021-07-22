---
UID: NF:propvarutil.InitVariantFromInt64Array
title: InitVariantFromInt64Array function (propvarutil.h)
description: Initializes a VARIANT structure with an array of 64-bit integer values.
helpviewer_keywords: ["InitVariantFromInt64Array","InitVariantFromInt64Array function [Windows Properties]","_shell_InitVariantFromInt64Array","properties.InitVariantFromInt64Array","propvarutil/InitVariantFromInt64Array","shell.InitVariantFromInt64Array"]
old-location: properties\InitVariantFromInt64Array.htm
tech.root: properties
ms.assetid: 18e9c804-b5e4-4abe-adcd-eaa402c6c94a
ms.date: 12/05/2018
ms.keywords: InitVariantFromInt64Array, InitVariantFromInt64Array function [Windows Properties], _shell_InitVariantFromInt64Array, properties.InitVariantFromInt64Array, propvarutil/InitVariantFromInt64Array, shell.InitVariantFromInt64Array
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
 - InitVariantFromInt64Array
 - propvarutil/InitVariantFromInt64Array
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
 - InitVariantFromInt64Array
---

# InitVariantFromInt64Array function


## -description

Initializes a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure with an array of 64-bit integer values.

## -parameters

### -param prgn [in]

Type: <b>const LONGLONG*</b>

Pointer to the source array of <b>LONGLONG</b> values.

### -param cElems [in]

Type: <b>ULONG</b>

The number of elements in the array pointed to by <i>prgn</i>.

The number of array elements.

### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_ARRAY | VT_I8 variant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromint64array">InitVariantFromInt64Array</a>.


```cpp
LONGLONG rgLongs[] = {4, 2};
VARIANT var;

HRESULT hr = InitVariantFromInt64Array(rgLongs, ARRAYSIZE(rgLongs), &var);

if (SUCCEEDED(hr))                            
{
    // var now is valid and has type VT_ARRAY | VT_I8.
    VariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromint64vector">InitPropVariantFromInt64Vector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromint64">InitVariantFromInt64</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttoint64array">VariantToInt64Array</a>