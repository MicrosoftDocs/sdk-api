---
UID: NF:propvarutil.InitVariantFromDouble
title: InitVariantFromDouble function (propvarutil.h)
description: Initializes a VARIANT structure with a value of type DOUBLE.
helpviewer_keywords: ["InitVariantFromDouble","InitVariantFromDouble function [Windows Properties]","_shell_InitVariantFromDouble","properties.InitVariantFromDouble","propvarutil/InitVariantFromDouble","shell.InitVariantFromDouble"]
old-location: properties\InitVariantFromDouble.htm
tech.root: properties
ms.assetid: a0a13843-e943-4fca-b4d4-5af1d2ff02e9
ms.date: 12/05/2018
ms.keywords: InitVariantFromDouble, InitVariantFromDouble function [Windows Properties], _shell_InitVariantFromDouble, properties.InitVariantFromDouble, propvarutil/InitVariantFromDouble, shell.InitVariantFromDouble
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
 - InitVariantFromDouble
 - propvarutil/InitVariantFromDouble
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
 - InitVariantFromDouble
---

# InitVariantFromDouble function


## -description

Initializes a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure with a value of type DOUBLE.

## -parameters

### -param dblVal [in]

Type: <b>DOUBLE</b>

Source value.

### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_R8 variant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromdouble">InitVariantFromDouble</a>.


```cpp
VARIANT var;

HRESULT hr = InitVariantFromDouble(3.1415, &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_R8.
    VariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromdouble">InitPropVariantFromDouble</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttodouble">VariantToDouble</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttodoublewithdefault">VariantToDoubleWithDefault</a>