---
UID: NF:propvarutil.InitPropVariantFromFileTimeVector
title: InitPropVariantFromFileTimeVector function (propvarutil.h)
description: Initializes a PROPVARIANT structure from a specified vector of FILETIME values.
helpviewer_keywords: ["InitPropVariantFromFileTimeVector","InitPropVariantFromFileTimeVector function [Windows Properties]","properties.InitPropVariantFromFileTimeVector","propvarutil/InitPropVariantFromFileTimeVector","shell.InitPropVariantFromFileTimeVector","shell_InitPropVariantFromFileTimeVector"]
old-location: properties\InitPropVariantFromFileTimeVector.htm
tech.root: properties
ms.assetid: 2f996f62-6605-405a-9cbb-6b41905eae29
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromFileTimeVector, InitPropVariantFromFileTimeVector function [Windows Properties], properties.InitPropVariantFromFileTimeVector, propvarutil/InitPropVariantFromFileTimeVector, shell.InitPropVariantFromFileTimeVector, shell_InitPropVariantFromFileTimeVector
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
 - InitPropVariantFromFileTimeVector
 - propvarutil/InitPropVariantFromFileTimeVector
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
 - InitPropVariantFromFileTimeVector
---

# InitPropVariantFromFileTimeVector function


## -description

Initializes a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure from a specified vector of <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> values.

## -parameters

### -param prgft [in, optional]

Type: <b>const FILETIME*</b>

Pointer to the date and time as a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> vector. If this value is <b>NULL</b>, the elements pointed to by the <b>cafiletime.pElems</b> structure member is initialized with (FILETIME)0.

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

Creates a VT_VECTOR | VT_FILETIME propvariant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromfiletimevector">InitPropVariantFromFileTimeVector</a>.


```cpp
// FILETIME rgFileTime[];
// Assume variable rgFileTime is initialized and valid.
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromFileTimeVector(rgFileTime, ARRAYSIZE(rgFileTime), &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_VECTOR | VT_FILETIME.
 
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromfiletime">InitPropVariantFromFileTime</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromfiletimearray">InitVariantFromFileTimeArray</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttofiletimevector">PropVariantToFileTimeVector</a>