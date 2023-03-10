---
UID: NF:propvarutil.InitPropVariantFromBuffer
title: InitPropVariantFromBuffer function (propvarutil.h)
description: Initializes a PROPVARIANT structure using the contents of a buffer.
helpviewer_keywords: ["InitPropVariantFromBuffer","InitPropVariantFromBuffer function [Windows Properties]","properties.InitPropVariantFromBuffer","propvarutil/InitPropVariantFromBuffer","shell.InitPropVariantFromBuffer","shell_InitPropVariantFromBuffer"]
old-location: properties\InitPropVariantFromBuffer.htm
tech.root: properties
ms.assetid: a6780070-d8de-40f9-8163-e5306e2aa1cc
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromBuffer, InitPropVariantFromBuffer function [Windows Properties], properties.InitPropVariantFromBuffer, propvarutil/InitPropVariantFromBuffer, shell.InitPropVariantFromBuffer, shell_InitPropVariantFromBuffer
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
 - InitPropVariantFromBuffer
 - propvarutil/InitPropVariantFromBuffer
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
 - InitPropVariantFromBuffer
---

# InitPropVariantFromBuffer function


## -description

Initializes a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure using the contents of a buffer.

## -parameters

### -param pv [in]

Type: <b>const void*</b>

Pointer to the buffer.

### -param cb [in]

Type: <b>UINT</b>

The length of the buffer, in bytes.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_VECTOR | VT_UI1 propvariant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfrombuffer">InitPropVariantFromBuffer</a>.


```cpp
// void *pv;
// UINT cb;
// Assume variable pv and cb are initialized and valid. pv points to a buffer  
// and cb contains the size of the buffer in bytes.
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromBuffer(pv, cb, &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_VECTOR | VT_UI1.
 
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfrombuffer">InitVariantFromBuffer</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttobuffer">PropVariantToBuffer</a>