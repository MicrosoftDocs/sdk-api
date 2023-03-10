---
UID: NF:propvarutil.InitVariantFromFileTimeArray
title: InitVariantFromFileTimeArray function (propvarutil.h)
description: Initializes a VARIANT structure with an array of FILETIME structures.
helpviewer_keywords: ["InitVariantFromFileTimeArray","InitVariantFromFileTimeArray function [Windows Properties]","_shell_InitVariantFromFileTimeArray","properties.InitVariantFromFileTimeArray","propvarutil/InitVariantFromFileTimeArray","shell.InitVariantFromFileTimeArray"]
old-location: properties\InitVariantFromFileTimeArray.htm
tech.root: properties
ms.assetid: d1b25aec-f302-4d39-93c1-0fcb2d7dbf45
ms.date: 12/05/2018
ms.keywords: InitVariantFromFileTimeArray, InitVariantFromFileTimeArray function [Windows Properties], _shell_InitVariantFromFileTimeArray, properties.InitVariantFromFileTimeArray, propvarutil/InitVariantFromFileTimeArray, shell.InitVariantFromFileTimeArray
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
 - InitVariantFromFileTimeArray
 - propvarutil/InitVariantFromFileTimeArray
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
 - InitVariantFromFileTimeArray
---

# InitVariantFromFileTimeArray function


## -description

Initializes a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure with an array of <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structures.

## -parameters

### -param prgft [in]

Type: <b>const FILETIME*</b>

Pointer to an array of <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structures.

### -param cElems [in]

Type: <b>ULONG</b>

The number of elements in the array pointed to by <i>prgft</i>.

### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creates a VT_ARRAY | VT_DATE variant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromfiletimearray">InitVariantFromFileTimeArray</a>.


```cpp
// FILETIME rgFileTimes[3];
// Assume variable rgFileTimes is initialized and valid.
VARIANT var;

HRESULT hr = InitVariantFromFileTimeArray(rgFileTimes, ARRAYSIZE(rgFileTimes), &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_ARRAY | VT_DATE.
    VariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromfiletimevector">InitPropVariantFromFileTimeVector</a>