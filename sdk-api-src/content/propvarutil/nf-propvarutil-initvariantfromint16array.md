---
UID: NF:propvarutil.InitVariantFromInt16Array
title: InitVariantFromInt16Array function (propvarutil.h)
description: Initializes a VARIANT structure with an array of 16-bit integer values.
helpviewer_keywords: ["InitVariantFromInt16Array","InitVariantFromInt16Array function [Windows Properties]","_shell_InitVariantFromInt16Array","properties.InitVariantFromInt16Array","propvarutil/InitVariantFromInt16Array","shell.InitVariantFromInt16Array"]
old-location: properties\InitVariantFromInt16Array.htm
tech.root: properties
ms.assetid: 6aeca46e-96b5-42cb-b5db-2c1e3152d629
ms.date: 12/05/2018
ms.keywords: InitVariantFromInt16Array, InitVariantFromInt16Array function [Windows Properties], _shell_InitVariantFromInt16Array, properties.InitVariantFromInt16Array, propvarutil/InitVariantFromInt16Array, shell.InitVariantFromInt16Array
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
 - InitVariantFromInt16Array
 - propvarutil/InitVariantFromInt16Array
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
 - InitVariantFromInt16Array
---

# InitVariantFromInt16Array function


## -description

Initializes a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure with an array of 16-bit integer values.

## -parameters

### -param prgn [in]

Type: <b>const SHORT*</b>

Pointer to the source array of <b>SHORT</b> values.

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

Creates a VT_ARRAY | VT_I2 variant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromint16array">InitVariantFromInt16Array</a>.


```cpp
SHORT rgShorts[] = {3, 1};
VARIANT var;

HRESULT hr = InitVariantFromInt16Array(rgShorts, ARRAYSIZE(rgShorts), &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_ARRAY | VT_I2.
    VariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromint16vector">InitPropVariantFromInt16Vector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromint16">InitVariantFromInt16</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttoint16array">VariantToInt16Array</a>