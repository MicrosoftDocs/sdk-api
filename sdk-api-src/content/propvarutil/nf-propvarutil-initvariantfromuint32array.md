---
UID: NF:propvarutil.InitVariantFromUInt32Array
title: InitVariantFromUInt32Array function (propvarutil.h)
description: Initializes a VARIANT structure with an array of unsigned 32-bit integer values.
helpviewer_keywords: ["InitVariantFromUInt32Array","InitVariantFromUInt32Array function [Windows Properties]","_shell_InitVariantFromUInt32Array","properties.InitVariantFromUInt32Array","propvarutil/InitVariantFromUInt32Array","shell.InitVariantFromUInt32Array"]
old-location: properties\InitVariantFromUInt32Array.htm
tech.root: properties
ms.assetid: b08e61bc-8b76-4baf-acf7-9eb97e521b65
ms.date: 12/05/2018
ms.keywords: InitVariantFromUInt32Array, InitVariantFromUInt32Array function [Windows Properties], _shell_InitVariantFromUInt32Array, properties.InitVariantFromUInt32Array, propvarutil/InitVariantFromUInt32Array, shell.InitVariantFromUInt32Array
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
 - InitVariantFromUInt32Array
 - propvarutil/InitVariantFromUInt32Array
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
 - InitVariantFromUInt32Array
---

# InitVariantFromUInt32Array function


## -description

Initializes a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure with an array of unsigned 32-bit integer values.

## -parameters

### -param prgn [in]

Type: <b>const ULONG*</b>

Pointer to the source array of <b>ULONG</b> values.

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

Creates a VT_ARRAY | VT_UI4 variant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromuint32array">InitVariantFromUInt32Array</a>.


```cpp
ULONG rgLongs[] = {4, 2};
VARIANT var;

HRESULT hr = InitVariantFromUInt32Array(rgLongs, ARRAYSIZE(rgLongs), &var);

if (SUCCEEDED(hr))                            
{
    // var now is valid and has type VT_ARRAY | VT_UI4.
    VariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromuint32vector">InitPropVariantFromUInt32Vector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromuint32">InitVariantFromUInt32</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttouint32array">VariantToUInt32Array</a>