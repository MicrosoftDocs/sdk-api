---
UID: NF:propvarutil.VariantToBooleanArrayAlloc
title: VariantToBooleanArrayAlloc function (propvarutil.h)
description: Allocates an array of BOOL values then extracts data from a VARIANT structure into that array.
helpviewer_keywords: ["VariantToBooleanArrayAlloc","VariantToBooleanArrayAlloc function [Windows Properties]","_shell_VariantToBooleanArrayAlloc","properties.VariantToBooleanArrayAlloc","propvarutil/VariantToBooleanArrayAlloc","shell.VariantToBooleanArrayAlloc"]
old-location: properties\VariantToBooleanArrayAlloc.htm
tech.root: properties
ms.assetid: 6a623ee0-d99e-47db-82f9-9008c618a526
ms.date: 12/05/2018
ms.keywords: VariantToBooleanArrayAlloc, VariantToBooleanArrayAlloc function [Windows Properties], _shell_VariantToBooleanArrayAlloc, properties.VariantToBooleanArrayAlloc, propvarutil/VariantToBooleanArrayAlloc, shell.VariantToBooleanArrayAlloc
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
 - VariantToBooleanArrayAlloc
 - propvarutil/VariantToBooleanArrayAlloc
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
 - VariantToBooleanArrayAlloc
---

# VariantToBooleanArrayAlloc function


## -description

Allocates an array of <b>BOOL</b> values then extracts data from a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure into that array.

## -parameters

### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

### -param pprgf [out]

Type: <b>BOOL**</b>

When this function returns, contains a pointer to an array of <b>BOOL</b> values extracted from the source <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

### -param pcElem [out]

Type: <b>ULONG*</b>

When this function returns, contains a pointer to the count of elements extracted from the source <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This helper function is used when the calling application expects a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> to hold an array of <b>BOOL</b> values.

If the source <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> is of type VT_ARRAY | VT_BOOL, this function extracts an array of <b>BOOL</b> values into a newly allocated array. The calling application is responsible for using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to release the array pointed to by <i>pprgf</i> when it is no longer needed.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttobooleanarrayalloc">VariantToBooleanArrayAlloc</a> to access an array of <b>BOOL</b> values stored in a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.


```cpp
// VARIANT var;
// Assume variable var is initialized and valid. 
// The application expects var to contain an array of BOOL values.
BOOL *prgFlags;
ULONG cElems;

HRESULT hr = VariantToBooleanArrayAlloc(var, &prgFlags, &cElems);

if (SUCCEEDED(hr))
{
     // prgFlags now points to a vector of cElems BOOLs.
     CoTaskMemFree(prgFlags);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfrombooleanarray">InitVariantFromBooleanArray</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttobooleanvector">PropVariantToBooleanVector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttobooleanarray">VariantToBooleanArray</a>