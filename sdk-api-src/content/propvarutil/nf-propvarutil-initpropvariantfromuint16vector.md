---
UID: NF:propvarutil.InitPropVariantFromUInt16Vector
title: InitPropVariantFromUInt16Vector function (propvarutil.h)
description: Initializes a PROPVARIANT structure based on a vector of 16-bit unsigned integer values.
helpviewer_keywords: ["InitPropVariantFromUInt16Vector","InitPropVariantFromUInt16Vector function [Windows Properties]","properties.InitPropVariantFromUInt16Vector","propvarutil/InitPropVariantFromUInt16Vector","shell.InitPropVariantFromUInt16Vector","shell_InitPropVariantFromUInt16Vector"]
old-location: properties\InitPropVariantFromUInt16Vector.htm
tech.root: properties
ms.assetid: 2e0eebd9-c246-42a7-90a8-d27fff6a2eab
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromUInt16Vector, InitPropVariantFromUInt16Vector function [Windows Properties], properties.InitPropVariantFromUInt16Vector, propvarutil/InitPropVariantFromUInt16Vector, shell.InitPropVariantFromUInt16Vector, shell_InitPropVariantFromUInt16Vector
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
 - InitPropVariantFromUInt16Vector
 - propvarutil/InitPropVariantFromUInt16Vector
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
 - InitPropVariantFromUInt16Vector
---

# InitPropVariantFromUInt16Vector function


## -description

Initializes a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure based on a vector of 16-bit unsigned integer values.

## -parameters

### -param prgn [in]

Type: <b>const USHORT*</b>

Pointer to a source vector of <b>USHORT</b> values. If this parameter is <b>NULL</b>, the <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> is initialized with zeros.

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

Creates a VT_VECTOR | VT_UI2 propvariant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromuint16vector">InitPropVariantFromUInt16Vector</a>.


```cpp
USHORT rgShorts[] = {4, 7};
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromUInt16Vector(rgShorts, ARRAYSIZE(rgShorts), &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_VECTOR | VT_UI2.
     PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromuint16">InitPropVariantFromUInt16</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromuint16">InitVariantFromUInt16</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint16vector">PropVariantToUInt16Vector</a>