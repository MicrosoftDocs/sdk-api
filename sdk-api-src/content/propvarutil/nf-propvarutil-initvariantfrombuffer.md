---
UID: NF:propvarutil.InitVariantFromBuffer
title: InitVariantFromBuffer function (propvarutil.h)
description: Initializes a VARIANT structure with the contents of a buffer.
helpviewer_keywords: ["InitVariantFromBuffer","InitVariantFromBuffer function [Windows Properties]","_shell_InitVariantFromBuffer","properties.InitVariantFromBuffer","propvarutil/InitVariantFromBuffer","shell.InitVariantFromBuffer"]
old-location: properties\InitVariantFromBuffer.htm
tech.root: properties
ms.assetid: 4dd28a13-2161-4258-a32f-57e5bd8ce091
ms.date: 12/05/2018
ms.keywords: InitVariantFromBuffer, InitVariantFromBuffer function [Windows Properties], _shell_InitVariantFromBuffer, properties.InitVariantFromBuffer, propvarutil/InitVariantFromBuffer, shell.InitVariantFromBuffer
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
 - InitVariantFromBuffer
 - propvarutil/InitVariantFromBuffer
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
 - InitVariantFromBuffer
---

# InitVariantFromBuffer function


## -description

Initializes a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure with the contents of a buffer.

## -parameters

### -param pv [in]

Type: <b>const VOID*</b>

Pointer to the source buffer.

### -param cb [in]

Type: <b>UINT</b>

The length of the buffer, in bytes.

### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_ARRAY | VT_UI1 variant..


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfrombuffer">InitVariantFromBuffer</a>.


```cpp
// void *pv;
// UINT cb;
// Assume variable pv and cb are initialized and valid. pv points to a 
// buffer and cb contains the size of the buffer in bytes.
VARIANT var;

HRESULT hr = InitVariantFromBuffer(pv, cb, & var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_ARRAY | VT_UI1.
    VariantClear(&var);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfrombuffer">InitPropVariantFromBuffer</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttobuffer">VariantToBuffer</a>