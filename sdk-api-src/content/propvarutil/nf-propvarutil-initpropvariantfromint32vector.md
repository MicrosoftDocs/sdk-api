---
UID: NF:propvarutil.InitPropVariantFromInt32Vector
title: InitPropVariantFromInt32Vector function (propvarutil.h)
description: Initializes a PROPVARIANT structure based on a vector of 32-bit integer values.
helpviewer_keywords: ["InitPropVariantFromInt32Vector","InitPropVariantFromInt32Vector function [Windows Properties]","properties.InitPropVariantFromInt32Vector","propvarutil/InitPropVariantFromInt32Vector","shell.InitPropVariantFromInt32Vector","shell_InitPropVariantFromInt32Vector"]
old-location: properties\InitPropVariantFromInt32Vector.htm
tech.root: properties
ms.assetid: 67173750-7b76-47fc-aec3-7e4e39a73532
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromInt32Vector, InitPropVariantFromInt32Vector function [Windows Properties], properties.InitPropVariantFromInt32Vector, propvarutil/InitPropVariantFromInt32Vector, shell.InitPropVariantFromInt32Vector, shell_InitPropVariantFromInt32Vector
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
 - InitPropVariantFromInt32Vector
 - propvarutil/InitPropVariantFromInt32Vector
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
 - InitPropVariantFromInt32Vector
---

# InitPropVariantFromInt32Vector function


## -description

Initializes a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure based on a vector of 32-bit integer values.

## -parameters

### -param prgn [in]

Type: <b>const LONG*</b>

Pointer to a source vector of <b>LONG</b> values. If this parameter is <b>NULL</b>, the vector is initialized with zeros.

### -param cElems [in]

Type: <b>ULONG</b>

The number of vector elements.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_VECTOR | VT_I4 propvariant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromint32vector">InitPropVariantFromInt32Vector</a>.


```cpp
LONG rgLongs[] = {1, 2, 7};
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromInt32Vector(rgLongs, ARRAYSIZE(rgLongs), &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_VECTOR | VT_I4.
 
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromint32">InitPropVariantFromInt32</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromint32">InitVariantFromInt32</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint32vector">PropVariantToInt32Vector</a>