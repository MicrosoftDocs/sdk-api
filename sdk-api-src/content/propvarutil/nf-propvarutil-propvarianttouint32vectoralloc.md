---
UID: NF:propvarutil.PropVariantToUInt32VectorAlloc
title: PropVariantToUInt32VectorAlloc function (propvarutil.h)
description: Extracts data from a PROPVARIANT structure into a newly-allocated ULONG vector.
helpviewer_keywords: ["PropVariantToUInt32VectorAlloc","PropVariantToUInt32VectorAlloc function [Windows Properties]","_shell_PropVariantToUInt32VectorAlloc","properties.PropVariantToUInt32VectorAlloc","propvarutil/PropVariantToUInt32VectorAlloc","shell.PropVariantToUInt32VectorAlloc"]
old-location: properties\PropVariantToUInt32VectorAlloc.htm
tech.root: properties
ms.assetid: 8127b569-aa20-4a15-9da5-cc7c3a7c5243
ms.date: 12/05/2018
ms.keywords: PropVariantToUInt32VectorAlloc, PropVariantToUInt32VectorAlloc function [Windows Properties], _shell_PropVariantToUInt32VectorAlloc, properties.PropVariantToUInt32VectorAlloc, propvarutil/PropVariantToUInt32VectorAlloc, shell.PropVariantToUInt32VectorAlloc
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
 - PropVariantToUInt32VectorAlloc
 - propvarutil/PropVariantToUInt32VectorAlloc
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
 - PropVariantToUInt32VectorAlloc
---

# PropVariantToUInt32VectorAlloc function


## -description

Extracts data from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure into a newly-allocated <b>ULONG</b> vector.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param pprgn [out]

Type: <b>ULONG**</b>

When this function returns, contains a pointer to a vector of <b>ULONG</b> values extracted from the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param pcElem [out]

Type: <b>ULONG*</b>

When this function returns, contains the count of <b>ULONG</b> values extracted from the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

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
The <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> was not of the appropriate type.

</td>
</tr>
</table>

## -remarks

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a vector of <b>ULONG</b> values.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type <b>VT_VECTOR</b> | <b>VT_UI4</b> or <b>VT_ARRAY</b> | <b>VT_UI4</b>, this function extracts a vector of <b>ULONG</b> values into a newly allocated vector. The calling application is responsible for using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to release the vector pointed to by <i>pprgn</i> when it is no longer needed. 


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint32vectoralloc">PropVariantToUInt32VectorAlloc</a> to access a <b>ULONG</b> vector value in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid. The application is expecting propvar to contain a vector of ULONG values.
ULONG *prgLongs;
ULONG cElems;
HRESULT hr = PropVariantToUInt32VectorAlloc(propvar, &prgLongs, &cElems);
if (SUCCEEDED(hr))
{
     // prgLongs now points to a vector of cElems ULONG.
     CoTaskMemFree(prgLongs);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromuint32vector">InitPropVariantFromUInt32Vector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetuint32elem">PropVariantGetUInt32Elem</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint32">PropVariantToUInt32</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint32vector">PropVariantToUInt32Vector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttouint32array">VariantToUInt32Array</a>