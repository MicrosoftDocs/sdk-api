---
UID: NF:propvarutil.InitPropVariantFromInt16Vector
title: InitPropVariantFromInt16Vector function (propvarutil.h)
description: Initializes a PROPVARIANT structure based on a specified vector of 16-bit integer values.
helpviewer_keywords: ["InitPropVariantFromInt16Vector","InitPropVariantFromInt16Vector function [Windows Properties]","properties.InitPropVariantFromInt16Vector","propvarutil/InitPropVariantFromInt16Vector","shell.InitPropVariantFromInt16Vector","shell_InitPropVariantFromInt16Vector"]
old-location: properties\InitPropVariantFromInt16Vector.htm
tech.root: properties
ms.assetid: 487204af-152e-4e39-808f-492dae7cadee
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromInt16Vector, InitPropVariantFromInt16Vector function [Windows Properties], properties.InitPropVariantFromInt16Vector, propvarutil/InitPropVariantFromInt16Vector, shell.InitPropVariantFromInt16Vector, shell_InitPropVariantFromInt16Vector
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
 - InitPropVariantFromInt16Vector
 - propvarutil/InitPropVariantFromInt16Vector
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
 - InitPropVariantFromInt16Vector
---

# InitPropVariantFromInt16Vector function


## -description

Initializes a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure based on a specified vector of 16-bit integer values.

## -parameters

### -param prgn [in]

Type: <b>const SHORT*</b>

Pointer to a source vector of <b>SHORT</b> values. If this parameter is <b>NULL</b>, the vector is initialized with zeros.

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

Creates a VT_VECTOR | VT_I2 propvariant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromint16vector">InitPropVariantFromInt16Vector</a>.


```cpp
SHORT rgShorts[] = {3, 1, 4};
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromInt16Vector(rgShorts, ARRAYSIZE(rgShorts), &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_VECTOR | VT_I2.
 
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromint16">InitPropVariantFromInt16</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromint16">InitVariantFromInt16</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint16vector">PropVariantToInt16Vector</a>