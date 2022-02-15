---
UID: NF:propvarutil.InitPropVariantFromUInt32
title: InitPropVariantFromUInt32 function (propvarutil.h)
description: Initializes a PROPVARIANT structure based on a 32-bit unsigned integer value.
helpviewer_keywords: ["InitPropVariantFromUInt32","InitPropVariantFromUInt32 function [Windows Properties]","properties.InitPropVariantFromUInt32","propvarutil/InitPropVariantFromUInt32","shell.InitPropVariantFromUInt32","shell_InitPropVariantFromUInt32"]
old-location: properties\InitPropVariantFromUInt32.htm
tech.root: properties
ms.assetid: 38fb5226-7916-49b5-9e8e-bfd2f0cfd22a
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromUInt32, InitPropVariantFromUInt32 function [Windows Properties], properties.InitPropVariantFromUInt32, propvarutil/InitPropVariantFromUInt32, shell.InitPropVariantFromUInt32, shell_InitPropVariantFromUInt32
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
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - InitPropVariantFromUInt32
 - propvarutil/InitPropVariantFromUInt32
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
 - InitPropVariantFromUInt32
---

# InitPropVariantFromUInt32 function


## -description

Initializes a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure based on a 32-bit unsigned integer value.

## -parameters

### -param ulVal [in]

Type: <b>ULONG</b>

Source <b>ULONG</b> value.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_UI4 propvariant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromuint32">InitPropVariantFromUInt32</a>.


```cpp
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromUInt32(56, &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_UI4.
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromuint32">InitVariantFromUInt32</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint32">PropVariantToUInt32</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint32withdefault">PropVariantToUInt32WithDefault</a>