---
UID: NF:propvarutil.PropVariantToBooleanVectorAlloc
title: PropVariantToBooleanVectorAlloc function (propvarutil.h)
description: Extracts data from a PROPVARIANT structure into a newly allocated Boolean vector.
helpviewer_keywords: ["PropVariantToBooleanVectorAlloc","PropVariantToBooleanVectorAlloc function [Windows Properties]","_shell_PropVariantToBooleanVectorAlloc","properties.PropVariantToBooleanVectorAlloc","propvarutil/PropVariantToBooleanVectorAlloc","shell.PropVariantToBooleanVectorAlloc"]
old-location: properties\PropVariantToBooleanVectorAlloc.htm
tech.root: properties
ms.assetid: 241f43b6-5ff0-4ce6-b0a4-59dc9cb6cf8f
ms.date: 12/05/2018
ms.keywords: PropVariantToBooleanVectorAlloc, PropVariantToBooleanVectorAlloc function [Windows Properties], _shell_PropVariantToBooleanVectorAlloc, properties.PropVariantToBooleanVectorAlloc, propvarutil/PropVariantToBooleanVectorAlloc, shell.PropVariantToBooleanVectorAlloc
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
 - PropVariantToBooleanVectorAlloc
 - propvarutil/PropVariantToBooleanVectorAlloc
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
 - PropVariantToBooleanVectorAlloc
---

# PropVariantToBooleanVectorAlloc function


## -description

Extracts data from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure into a newly allocated Boolean vector.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param pprgf [out]

Type: <b>BOOL**</b>

When this function returns, contains a pointer to a vector of Boolean values extracted from the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param pcElem [out]

Type: <b>ULONG*</b>

When this function returns, contains the count of Boolean elements extracted from the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Returns <b>S_OK</b> if successful, or an error value otherwise.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The<a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> was not of the appropriate type.

</td>
</tr>
</table>

## -remarks

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a Boolean vector value.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type VT_VECTOR | VT_BOOL or VT_ARRAY | VT_BOOL, this function extracts a vector of Boolean values into a newly allocated vector of <b>BOOL</b> values. The calling application is responsible for using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to release the vector pointed to by <i>pprgf</i> when it is no longer needed.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttobooleanvectoralloc">PropVariantToBooleanVectorAlloc</a> to access a Boolean vector value in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid. The application is 
// expecting propvar to contain a vector of Boolean values.
BOOL *prgFlags;
ULONG cFlags;
HRESULT hr = PropVariantToBooleanVectorAlloc(propvar, &prgFlags, &cFlags);

if (SUCCEEDED(hr))
{
     // The prgFlags variable now points to a vector that contains a count
     // of cFlags flags.
     CoTaskMemFree(prgFlags);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfrombooleanvector">InitPropVariantFromBooleanVector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-ispropvariantvector">IsPropVariantVector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetbooleanelem">PropVariantGetBooleanElem</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttobooleanvector">PropVariantToBooleanVector</a>