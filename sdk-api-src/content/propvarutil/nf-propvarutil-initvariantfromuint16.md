---
UID: NF:propvarutil.InitVariantFromUInt16
title: InitVariantFromUInt16 function (propvarutil.h)
description: Initializes a VARIANT structure with an unsigned 16-bit integer value.
helpviewer_keywords: ["InitVariantFromUInt16","InitVariantFromUInt16 function [Windows Properties]","_shell_InitVariantFromUInt16","properties.InitVariantFromUInt16","propvarutil/InitVariantFromUInt16","shell.InitVariantFromUInt16"]
old-location: properties\InitVariantFromUInt16.htm
tech.root: properties
ms.assetid: ec919626-6af3-4e33-85a5-134274220c67
ms.date: 12/05/2018
ms.keywords: InitVariantFromUInt16, InitVariantFromUInt16 function [Windows Properties], _shell_InitVariantFromUInt16, properties.InitVariantFromUInt16, propvarutil/InitVariantFromUInt16, shell.InitVariantFromUInt16
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
 - InitVariantFromUInt16
 - propvarutil/InitVariantFromUInt16
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
 - InitVariantFromUInt16
---

# InitVariantFromUInt16 function


## -description

Initializes a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure with an unsigned 16-bit integer value.

## -parameters

### -param uiVal [in]

Type: <b>USHORT</b>

Source <b>USHORT</b> value.

### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_UI2 variant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromuint16">InitVariantFromUInt16</a>.


```cpp
VARIANT var;

HRESULT hr = InitVariantFromUInt16(3, &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_UI2.
    VariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromuint16">InitPropVariantFromUInt16</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttouint16">VariantToUInt16</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttouint16withdefault">VariantToUInt16WithDefault</a>