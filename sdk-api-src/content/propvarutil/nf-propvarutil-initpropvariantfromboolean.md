---
UID: NF:propvarutil.InitPropVariantFromBoolean
title: InitPropVariantFromBoolean function (propvarutil.h)
description: Initializes a given PROPVARIANT structure as a VT_BOOL using a specified Boolean value.
helpviewer_keywords: ["InitPropVariantFromBoolean","InitPropVariantFromBoolean function [Windows Properties]","properties.InitPropVariantFromBoolean","propvarutil/InitPropVariantFromBoolean","shell.InitPropVariantFromBoolean","shell_InitPropVariantFromBoolean"]
old-location: properties\InitPropVariantFromBoolean.htm
tech.root: properties
ms.assetid: aa23f7a2-1983-4a30-b2fc-601efa37e0ff
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromBoolean, InitPropVariantFromBoolean function [Windows Properties], properties.InitPropVariantFromBoolean, propvarutil/InitPropVariantFromBoolean, shell.InitPropVariantFromBoolean, shell_InitPropVariantFromBoolean
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
 - InitPropVariantFromBoolean
 - propvarutil/InitPropVariantFromBoolean
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
 - InitPropVariantFromBoolean
---

# InitPropVariantFromBoolean function


## -description

Initializes a given <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure as a <b>VT_BOOL</b> using a specified Boolean value.

## -parameters

### -param fVal [in]

Type: <b>BOOL</b>

Source <b>BOOL</b> value.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.

Note that the <i>boolVal</i> member specifically initialized by this function is of type <b>VARIANT_BOOL</b> and therefore can have values <b>VARIANT_TRUE</b> or <b>VARIANT_FALSE</b>. When working with this structure member directly, use these constants instead of <b>TRUE</b> or <b>FALSE</b> because <b>VARIANT_TRUE</b> is not equal to <b>TRUE</b> and sizeof(<b>VARIANT_TRUE</b>) is not the same as sizeof(<b>TRUE</b>).


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromboolean">InitPropVariantFromBoolean</a>.


```cpp
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromBoolean(TRUE, &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_BOOL.
 
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfrombooleanvector">InitPropVariantFromBooleanVector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromboolean">InitVariantFromBoolean</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoboolean">PropVariantToBoolean</a>