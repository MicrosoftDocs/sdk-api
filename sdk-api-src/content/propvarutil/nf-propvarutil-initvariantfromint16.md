---
UID: NF:propvarutil.InitVariantFromInt16
title: InitVariantFromInt16 function (propvarutil.h)
description: Initializes a VARIANT structure with a 16-bit integer value.
helpviewer_keywords: ["InitVariantFromInt16","InitVariantFromInt16 function [Windows Properties]","_shell_InitVariantFromInt16","properties.InitVariantFromInt16","propvarutil/InitVariantFromInt16","shell.InitVariantFromInt16"]
old-location: properties\InitVariantFromInt16.htm
tech.root: properties
ms.assetid: 8ccb09bf-a2d2-4637-b8b1-e7abe83b846d
ms.date: 12/05/2018
ms.keywords: InitVariantFromInt16, InitVariantFromInt16 function [Windows Properties], _shell_InitVariantFromInt16, properties.InitVariantFromInt16, propvarutil/InitVariantFromInt16, shell.InitVariantFromInt16
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
 - InitVariantFromInt16
 - propvarutil/InitVariantFromInt16
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
 - InitVariantFromInt16
---

# InitVariantFromInt16 function


## -description

Initializes a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure with a 16-bit integer value.

## -parameters

### -param iVal [in]

Type: <b>SHORT</b>

Source <b>SHORT</b> value.

### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_I2 variant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromint16">InitVariantFromInt16</a>.


```cpp
VARIANT var;

HRESULT hr = InitVariantFromInt16(3, &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_I2.
    VariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromint16">InitPropVariantFromInt16</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttoint16">VariantToInt16</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttoint16withdefault">VariantToInt16WithDefault</a>