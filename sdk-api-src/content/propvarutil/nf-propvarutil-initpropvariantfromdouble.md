---
UID: NF:propvarutil.InitPropVariantFromDouble
title: InitPropVariantFromDouble function (propvarutil.h)
description: Initializes a PROPVARIANT structure based on a specified double value.
helpviewer_keywords: ["InitPropVariantFromDouble","InitPropVariantFromDouble function [Windows Properties]","properties.InitPropVariantFromDouble","propvarutil/InitPropVariantFromDouble","shell.InitPropVariantFromDouble","shell_InitPropVariantFromDouble"]
old-location: properties\InitPropVariantFromDouble.htm
tech.root: properties
ms.assetid: aeae9091-3b1e-4112-8f50-79d77cb891c4
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromDouble, InitPropVariantFromDouble function [Windows Properties], properties.InitPropVariantFromDouble, propvarutil/InitPropVariantFromDouble, shell.InitPropVariantFromDouble, shell_InitPropVariantFromDouble
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
 - InitPropVariantFromDouble
 - propvarutil/InitPropVariantFromDouble
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
 - InitPropVariantFromDouble
---

# InitPropVariantFromDouble function


## -description

Initializes a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure based on a specified <b>double</b> value.

## -parameters

### -param dblVal [in]

Type: <b>DOUBLE</b>

The source <b>double</b> value.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_R8 propvariant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromdouble">InitPropVariantFromDouble</a>.


```cpp
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromDouble(3.1415, &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_R8.
 
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromdoublevector">InitPropVariantFromDoubleVector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromdouble">InitVariantFromDouble</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttodouble">PropVariantToDouble</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttodoublewithdefault">PropVariantToDoubleWithDefault</a>