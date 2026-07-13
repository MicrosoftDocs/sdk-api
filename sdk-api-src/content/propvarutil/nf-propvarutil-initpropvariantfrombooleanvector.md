---
UID: NF:propvarutil.InitPropVariantFromBooleanVector
title: InitPropVariantFromBooleanVector function (propvarutil.h)
description: Initializes a PROPVARIANT structure from a specified Boolean vector.
helpviewer_keywords: ["InitPropVariantFromBooleanVector","InitPropVariantFromBooleanVector function [Windows Properties]","_shell_InitPropVariantFromBooleanVector","properties.InitPropVariantFromBooleanVector","propvarutil/InitPropVariantFromBooleanVector","shell.InitPropVariantFromBooleanVector"]
old-location: properties\InitPropVariantFromBooleanVector.htm
tech.root: properties
ms.assetid: d2e34efb-d5d9-4adf-b582-d3f82d04597f
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromBooleanVector, InitPropVariantFromBooleanVector function [Windows Properties], _shell_InitPropVariantFromBooleanVector, properties.InitPropVariantFromBooleanVector, propvarutil/InitPropVariantFromBooleanVector, shell.InitPropVariantFromBooleanVector
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
 - InitPropVariantFromBooleanVector
 - propvarutil/InitPropVariantFromBooleanVector
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
 - InitPropVariantFromBooleanVector
---

# InitPropVariantFromBooleanVector function


## -description

Initializes a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure from a specified Boolean vector.

## -parameters

### -param prgf [in, optional]

Type: <b>const BOOL*</b>

Pointer to the Boolean vector used to initialize the structure. If this parameter is <b>NULL</b>, the elements pointed to by the <b>cabool.pElems</b> structure member are initialized with VARIANT_FALSE.

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

This creates a <b>VT_BOOL</b> | <b>VT_VECTOR</b> propvariant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfrombooleanvector">InitPropVariantFromBooleanVector</a>



```cpp
PROPVARIANT propvar;
BOOL rgBool[2] = {TRUE, FALSE};

HRESULT hr = InitPropVariantFromBooleanVector(rgBool, ARRAYSIZE(rgBool), &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_VECTOR | VT_BOOL.
 
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromboolean">InitPropVariantFromBoolean</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromboolean">InitVariantFromBoolean</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttobooleanvector">PropVariantToBooleanVector</a>