---
UID: NF:propvarutil.InitPropVariantFromUInt64
title: InitPropVariantFromUInt64 function (propvarutil.h)
description: Initializes a PROPVARIANT structure with a 64-bit unsigned integer value.
helpviewer_keywords: ["InitPropVariantFromUInt64","InitPropVariantFromUInt64 function [Windows Properties]","properties.InitPropVariantFromUInt64","propvarutil/InitPropVariantFromUInt64","shell.InitPropVariantFromUInt64","shell_InitPropVariantFromUInt64"]
old-location: properties\InitPropVariantFromUInt64.htm
tech.root: properties
ms.assetid: c0dbc8d1-45ed-497b-a6ef-2beb4f031e4b
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromUInt64, InitPropVariantFromUInt64 function [Windows Properties], properties.InitPropVariantFromUInt64, propvarutil/InitPropVariantFromUInt64, shell.InitPropVariantFromUInt64, shell_InitPropVariantFromUInt64
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
 - InitPropVariantFromUInt64
 - propvarutil/InitPropVariantFromUInt64
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
 - InitPropVariantFromUInt64
---

# InitPropVariantFromUInt64 function


## -description

Initializes a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure with a 64-bit unsigned integer value.

## -parameters

### -param ullVal [in]

Type: <b>ULONGLONG</b>

Source <b>ULONGLONG</b> value.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_UI8 propvariant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromuint64">InitPropVariantFromUInt64</a>.


```cpp
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromUInt64(563, &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_UI8.
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromuint64">InitVariantFromUInt64</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint64">PropVariantToUInt64</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint64withdefault">PropVariantToUInt64WithDefault</a>