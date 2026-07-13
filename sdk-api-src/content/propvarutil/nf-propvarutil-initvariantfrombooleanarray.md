---
UID: NF:propvarutil.InitVariantFromBooleanArray
title: InitVariantFromBooleanArray function (propvarutil.h)
description: Initializes a VARIANT structure from an array of Boolean values.
helpviewer_keywords: ["InitVariantFromBooleanArray","InitVariantFromBooleanArray function [Windows Properties]","_shell_InitVariantFromBooleanArray","properties.InitVariantFromBooleanArray","propvarutil/InitVariantFromBooleanArray","shell.InitVariantFromBooleanArray"]
old-location: properties\InitVariantFromBooleanArray.htm
tech.root: properties
ms.assetid: 50780131-c0ed-443b-86e8-deb996a5c98e
ms.date: 12/05/2018
ms.keywords: InitVariantFromBooleanArray, InitVariantFromBooleanArray function [Windows Properties], _shell_InitVariantFromBooleanArray, properties.InitVariantFromBooleanArray, propvarutil/InitVariantFromBooleanArray, shell.InitVariantFromBooleanArray
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
 - InitVariantFromBooleanArray
 - propvarutil/InitVariantFromBooleanArray
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
 - InitVariantFromBooleanArray
---

# InitVariantFromBooleanArray function


## -description

Initializes a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure from an array of Boolean values.

## -parameters

### -param prgf [in]

Type: <b>const BOOL*</b>

Pointer to source array of Boolean values.

### -param cElems [in]

Type: <b>ULONG</b>

The number of elements in the array.

### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_ARRAY | VT_BOOL variant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfrombooleanarray">InitVariantFromBooleanArray</a>.


```cpp
BOOL rgFlags[] = {TRUE, FALSE};
VARIANT var;

HRESULT hr = InitVariantFromBooleanArray(rgFlags, ARRAYSIZE(rgFlags), &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_ARRAY | VT_BOOL.
    VariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfrombooleanvector">InitPropVariantFromBooleanVector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttobooleanarray">VariantToBooleanArray</a>