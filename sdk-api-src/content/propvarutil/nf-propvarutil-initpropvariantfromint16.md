---
UID: NF:propvarutil.InitPropVariantFromInt16
title: InitPropVariantFromInt16 function (propvarutil.h)
description: Initializes a PROPVARIANT structure based on a 16-bit integer value.
helpviewer_keywords: ["InitPropVariantFromInt16","InitPropVariantFromInt16 function [Windows Properties]","properties.InitPropVariantFromInt16","propvarutil/InitPropVariantFromInt16","shell.InitPropVariantFromInt16","shell_InitPropVariantFromInt16"]
old-location: properties\InitPropVariantFromInt16.htm
tech.root: properties
ms.assetid: fb58c71c-f6ff-408e-9375-98654a41cf11
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromInt16, InitPropVariantFromInt16 function [Windows Properties], properties.InitPropVariantFromInt16, propvarutil/InitPropVariantFromInt16, shell.InitPropVariantFromInt16, shell_InitPropVariantFromInt16
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
 - InitPropVariantFromInt16
 - propvarutil/InitPropVariantFromInt16
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
 - InitPropVariantFromInt16
---

# InitPropVariantFromInt16 function


## -description

Initializes a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure based on a 16-bit integer value.

## -parameters

### -param nVal [in]

Type: <b>SHORT</b>

The source <b>SHORT</b> value.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function creates a VT_I2 propvariant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromint16">InitPropVariantFromInt16</a>.


```cpp
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromInt16(42, &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_I2.
 
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromint16vector">InitPropVariantFromInt16Vector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromint16">InitVariantFromInt16</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint16">PropVariantToInt16</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint16withdefault">PropVariantToInt16WithDefault</a>