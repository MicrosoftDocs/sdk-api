---
UID: NF:propvarutil.InitVariantFromUInt16Array
title: InitVariantFromUInt16Array function (propvarutil.h)
description: Initializes a VARIANT structure with an array of unsigned 16-bit integer values.
helpviewer_keywords: ["InitVariantFromUInt16Array","InitVariantFromUInt16Array function [Windows Properties]","_shell_InitVariantFromUInt16Array","properties.InitVariantFromUInt16Array","propvarutil/InitVariantFromUInt16Array","shell.InitVariantFromUInt16Array"]
old-location: properties\InitVariantFromUInt16Array.htm
tech.root: properties
ms.assetid: 57fe1dd2-48a5-486e-a2cb-53cf0b8f96b0
ms.date: 12/05/2018
ms.keywords: InitVariantFromUInt16Array, InitVariantFromUInt16Array function [Windows Properties], _shell_InitVariantFromUInt16Array, properties.InitVariantFromUInt16Array, propvarutil/InitVariantFromUInt16Array, shell.InitVariantFromUInt16Array
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
 - InitVariantFromUInt16Array
 - propvarutil/InitVariantFromUInt16Array
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
 - InitVariantFromUInt16Array
---

# InitVariantFromUInt16Array function


## -description

Initializes a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure with an array of unsigned 16-bit integer values.

## -parameters

### -param prgn [in]

Type: <b>const USHORT*</b>

Pointer to the source array of <b>USHORT</b> values.

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

Creates a VT_ARRAY | VT_UI2 variant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromuint16array">InitVariantFromUInt16Array</a>.


```cpp
USHORT rgShorts[] = {3, 1};
VARIANT var;

HRESULT hr = InitVariantFromUInt16Array(rgShorts, ARRAYSIZE(rgShorts), &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_ARRAY | VT_UI2.
    VariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromuint16vector">InitPropVariantFromUInt16Vector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromuint16">InitVariantFromUInt16</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttouint16array">VariantToUInt16Array</a>