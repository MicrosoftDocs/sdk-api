---
UID: NF:propvarutil.InitPropVariantFromInt32
title: InitPropVariantFromInt32 function (propvarutil.h)
description: Initializes a PROPVARIANT structure based on a 32-bit integer value.
helpviewer_keywords: ["InitPropVariantFromInt32","InitPropVariantFromInt32 function [Windows Properties]","properties.InitPropVariantFromInt32","propvarutil/InitPropVariantFromInt32","shell.InitPropVariantFromInt32","shell_InitPropVariantFromInt32"]
old-location: properties\InitPropVariantFromInt32.htm
tech.root: properties
ms.assetid: 923be4ac-5545-431b-ab69-3b7f366a1ec0
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromInt32, InitPropVariantFromInt32 function [Windows Properties], properties.InitPropVariantFromInt32, propvarutil/InitPropVariantFromInt32, shell.InitPropVariantFromInt32, shell_InitPropVariantFromInt32
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
 - InitPropVariantFromInt32
 - propvarutil/InitPropVariantFromInt32
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
 - InitPropVariantFromInt32
---

# InitPropVariantFromInt32 function


## -description

Initializes a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure based on a 32-bit integer value.

## -parameters

### -param lVal [in]

Type: <b>LONG</b>

The source <b>LONG</b> value.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_I4 propvariant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromint32">InitPropVariantFromInt32</a>.


```cpp
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromInt32(127, &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_I4.
 
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromint32">InitVariantFromInt32</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint32">PropVariantToInt32</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint32withdefault">PropVariantToInt32WithDefault</a>