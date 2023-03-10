---
UID: NF:propvarutil.InitVariantFromInt64
title: InitVariantFromInt64 function (propvarutil.h)
description: Initializes a VARIANT structure with a 64-bit integer value.
helpviewer_keywords: ["InitVariantFromInt64","InitVariantFromInt64 function [Windows Properties]","_shell_InitVariantFromInt64","properties.InitVariantFromInt64","propvarutil/InitVariantFromInt64","shell.InitVariantFromInt64"]
old-location: properties\InitVariantFromInt64.htm
tech.root: properties
ms.assetid: 3c5254a6-b498-40b0-acd3-0ffa7fd93104
ms.date: 12/05/2018
ms.keywords: InitVariantFromInt64, InitVariantFromInt64 function [Windows Properties], _shell_InitVariantFromInt64, properties.InitVariantFromInt64, propvarutil/InitVariantFromInt64, shell.InitVariantFromInt64
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
 - InitVariantFromInt64
 - propvarutil/InitVariantFromInt64
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
 - InitVariantFromInt64
---

# InitVariantFromInt64 function


## -description

Initializes a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure with a 64-bit integer value.

## -parameters

### -param llVal [in]

Type: <b>LONGLONG</b>

Source <b>LONGLONG</b> value.

### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_I8 variant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromint64">InitVariantFromInt64</a>.


```cpp
VARIANT var;

HRESULT hr = InitVariantFromInt64(3176, &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_I8.
    VariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromint64">InitPropVariantFromInt64</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttoint64">VariantToInt64</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttoint64withdefault">VariantToInt64WithDefault</a>