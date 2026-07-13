---
UID: NF:propvarutil.InitPropVariantFromInt64Vector
title: InitPropVariantFromInt64Vector function (propvarutil.h)
description: Initializes a PROPVARIANT structure based on a vector of Int64 values.
helpviewer_keywords: ["InitPropVariantFromInt64Vector","InitPropVariantFromInt64Vector function [Windows Properties]","properties.InitPropVariantFromInt64Vector","propvarutil/InitPropVariantFromInt64Vector","shell.InitPropVariantFromInt64Vector","shell_InitPropVariantFromInt64Vector"]
old-location: properties\InitPropVariantFromInt64Vector.htm
tech.root: properties
ms.assetid: a2375776-ba9e-4d59-8924-86ac087b99d7
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromInt64Vector, InitPropVariantFromInt64Vector function [Windows Properties], properties.InitPropVariantFromInt64Vector, propvarutil/InitPropVariantFromInt64Vector, shell.InitPropVariantFromInt64Vector, shell_InitPropVariantFromInt64Vector
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
 - InitPropVariantFromInt64Vector
 - propvarutil/InitPropVariantFromInt64Vector
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
 - InitPropVariantFromInt64Vector
---

# InitPropVariantFromInt64Vector function


## -description

Initializes a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure based on a vector of <b>Int64</b> values.

## -parameters

### -param prgn [in]

Type: <b>const LONGLONG*</b>

Pointer to a source vector of <b>LONGLONG</b> values. If this parameter is <b>NULL</b>, the vector is initialized with zeros.

### -param cElems [in]

Type: <b>ULONG</b>

The number of elements in the vector.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_VECTOR | VT_I8 propvariant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromint64vector">InitPropVariantFromInt64Vector</a>.


```cpp
LONGLONG rgLongLongs[] = {4, 7};
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromInt64Vector(rgLongLongs, ARRAYSIZE(rgLongLongs), &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_VECTOR | VT_I8.
 
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromint64">InitPropVariantFromInt64</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromint64">InitVariantFromInt64</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint64vector">PropVariantToInt64Vector</a>