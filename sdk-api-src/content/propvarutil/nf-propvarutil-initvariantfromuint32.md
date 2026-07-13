---
UID: NF:propvarutil.InitVariantFromUInt32
title: InitVariantFromUInt32 function (propvarutil.h)
description: Initializes a VARIANT structure with an unsigned 32-bit integer value.
helpviewer_keywords: ["InitVariantFromUInt32","InitVariantFromUInt32 function [Windows Properties]","_shell_InitVariantFromUInt32","properties.InitVariantFromUInt32","propvarutil/InitVariantFromUInt32","shell.InitVariantFromUInt32"]
old-location: properties\InitVariantFromUInt32.htm
tech.root: properties
ms.assetid: df260524-188d-4c2a-8996-ce22ddda41e7
ms.date: 12/05/2018
ms.keywords: InitVariantFromUInt32, InitVariantFromUInt32 function [Windows Properties], _shell_InitVariantFromUInt32, properties.InitVariantFromUInt32, propvarutil/InitVariantFromUInt32, shell.InitVariantFromUInt32
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
 - InitVariantFromUInt32
 - propvarutil/InitVariantFromUInt32
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
 - InitVariantFromUInt32
---

# InitVariantFromUInt32 function


## -description

Initializes a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure with an unsigned 32-bit integer value.

## -parameters

### -param ulVal [in]

Type: <b>ULONG</b>

Source <b>ULONG</b> value.

### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_UI4 variant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromuint32">InitVariantFromUInt32</a>.


```cpp
VARIANT var;

HRESULT hr = InitVariantFromUInt32(3, &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_UI4.
 
    VariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromuint32">InitPropVariantFromUInt32</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttouint32">VariantToUInt32</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttouint32withdefault">VariantToUInt32WithDefault</a>