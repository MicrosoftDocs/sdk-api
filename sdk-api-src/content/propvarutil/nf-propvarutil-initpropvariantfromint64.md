---
UID: NF:propvarutil.InitPropVariantFromInt64
title: InitPropVariantFromInt64 function (propvarutil.h)
description: Initializes a PROPVARIANT structure based on a specified Int64 value.
helpviewer_keywords: ["InitPropVariantFromInt64","InitPropVariantFromInt64 function [Windows Properties]","properties.InitPropVariantFromInt64","propvarutil/InitPropVariantFromInt64","shell.InitPropVariantFromInt64","shell_InitPropVariantFromInt64"]
old-location: properties\InitPropVariantFromInt64.htm
tech.root: properties
ms.assetid: 2a2a5348-4d3d-475c-8039-097b4dacf7cb
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromInt64, InitPropVariantFromInt64 function [Windows Properties], properties.InitPropVariantFromInt64, propvarutil/InitPropVariantFromInt64, shell.InitPropVariantFromInt64, shell_InitPropVariantFromInt64
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
 - InitPropVariantFromInt64
 - propvarutil/InitPropVariantFromInt64
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
 - InitPropVariantFromInt64
---

# InitPropVariantFromInt64 function


## -description

Initializes a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure based on a specified <b>Int64</b> value.

## -parameters

### -param llVal [in]

Type: <b>LONGLONG</b>

The source <b>LONGLONG</b> value.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_I8 propvariant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromint64">InitPropVariantFromInt64</a>.


```cpp
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromInt64(4096, &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_I8.
 
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromint64">InitVariantFromInt64</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint64">PropVariantToInt64</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint64withdefault">PropVariantToInt64WithDefault</a>