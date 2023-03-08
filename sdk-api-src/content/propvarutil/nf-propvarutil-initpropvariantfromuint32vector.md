---
UID: NF:propvarutil.InitPropVariantFromUInt32Vector
title: InitPropVariantFromUInt32Vector function (propvarutil.h)
description: Initializes a PROPVARIANT structure based on a vector of 32-bit unsigned integer values.
helpviewer_keywords: ["InitPropVariantFromUInt32Vector","InitPropVariantFromUInt32Vector function [Windows Properties]","properties.InitPropVariantFromUInt32Vector","propvarutil/InitPropVariantFromUInt32Vector","shell.InitPropVariantFromUInt32Vector","shell_InitPropVariantFromUInt32Vector"]
old-location: properties\InitPropVariantFromUInt32Vector.htm
tech.root: properties
ms.assetid: 807793fc-c679-4749-816c-005a77a37f08
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromUInt32Vector, InitPropVariantFromUInt32Vector function [Windows Properties], properties.InitPropVariantFromUInt32Vector, propvarutil/InitPropVariantFromUInt32Vector, shell.InitPropVariantFromUInt32Vector, shell_InitPropVariantFromUInt32Vector
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
 - InitPropVariantFromUInt32Vector
 - propvarutil/InitPropVariantFromUInt32Vector
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
 - InitPropVariantFromUInt32Vector
---

# InitPropVariantFromUInt32Vector function


## -description

Initializes a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure based on a vector of 32-bit unsigned integer values.

## -parameters

### -param prgn [in]

Type: <b>const ULONG*</b>

Pointer to a source vector of <b>ULONG</b> values. If this parameter is <b>NULL</b>, the <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> is initialized with zeros.

### -param cElems [in]

Type: <b>ULONG</b>

Number of elements in the vector pointed to by <i>prgn</i>.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_VECTOR | VT_UI4 propvariant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromuint32vector">InitPropVariantFromUInt32Vector</a>.


```cpp
ULONG rgLongs[] = {4, 7};
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromUInt32Vector(rgLongs, ARRAYSIZE(rgLongs), &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_VECTOR | VT_UI4.
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromuint32">InitPropVariantFromUInt32</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromuint32array">InitVariantFromUInt32Array</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint32vector">PropVariantToUInt32Vector</a>