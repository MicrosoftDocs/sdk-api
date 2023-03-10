---
UID: NF:propvarutil.InitPropVariantFromUInt16
title: InitPropVariantFromUInt16 function (propvarutil.h)
description: Initializes a PROPVARIANT structure based on a 16-bit unsigned integer value.
helpviewer_keywords: ["InitPropVariantFromUInt16","InitPropVariantFromUInt16 function [Windows Properties]","properties.InitPropVariantFromUInt16","propvarutil/InitPropVariantFromUInt16","shell.InitPropVariantFromUInt16","shell_InitPropVariantFromUInt16"]
old-location: properties\InitPropVariantFromUInt16.htm
tech.root: properties
ms.assetid: 2f4b0c6b-2d68-4ea6-a7fb-7884071dcfbe
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromUInt16, InitPropVariantFromUInt16 function [Windows Properties], properties.InitPropVariantFromUInt16, propvarutil/InitPropVariantFromUInt16, shell.InitPropVariantFromUInt16, shell_InitPropVariantFromUInt16
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
 - InitPropVariantFromUInt16
 - propvarutil/InitPropVariantFromUInt16
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
 - InitPropVariantFromUInt16
---

# InitPropVariantFromUInt16 function


## -description

Initializes a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure based on a 16-bit unsigned integer value.

## -parameters

### -param uiVal [in]

Type: <b>USHORT</b>

Source value.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_UI2 propvariant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromuint16">InitPropVariantFromUInt16</a>.


```cpp
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromUInt16(5, &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_UI2.
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromuint16">InitVariantFromUInt16</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint16">PropVariantToUInt16</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint16withdefault">PropVariantToUInt16WithDefault</a>