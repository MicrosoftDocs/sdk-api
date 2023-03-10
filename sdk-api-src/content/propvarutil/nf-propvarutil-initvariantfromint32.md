---
UID: NF:propvarutil.InitVariantFromInt32
title: InitVariantFromInt32 function (propvarutil.h)
description: Initializes a VARIANT structure with a 32-bit integer value.
helpviewer_keywords: ["InitVariantFromInt32","InitVariantFromInt32 function [Windows Properties]","_shell_InitVariantFromInt32","properties.InitVariantFromInt32","propvarutil/InitVariantFromInt32","shell.InitVariantFromInt32"]
old-location: properties\InitVariantFromInt32.htm
tech.root: properties
ms.assetid: b754149e-09e3-4420-b0e6-6e14ccbd9cff
ms.date: 12/05/2018
ms.keywords: InitVariantFromInt32, InitVariantFromInt32 function [Windows Properties], _shell_InitVariantFromInt32, properties.InitVariantFromInt32, propvarutil/InitVariantFromInt32, shell.InitVariantFromInt32
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
 - InitVariantFromInt32
 - propvarutil/InitVariantFromInt32
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
 - InitVariantFromInt32
---

# InitVariantFromInt32 function


## -description

Initializes a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure with a 32-bit integer value.

## -parameters

### -param lVal [in]

Type: <b>LONG</b>

Source <b>LONG</b> value.

### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_I4 variant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromint32">InitVariantFromInt32</a>.


```cpp
VARIANT var;

HRESULT hr = InitVariantFromInt32(3, &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_I4.
    VariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromint32">InitPropVariantFromInt32</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttoint32">VariantToInt32</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttoint32withdefault">VariantToInt32WithDefault</a>