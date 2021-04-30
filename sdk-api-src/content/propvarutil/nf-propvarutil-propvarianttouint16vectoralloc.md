---
UID: NF:propvarutil.PropVariantToUInt16VectorAlloc
title: PropVariantToUInt16VectorAlloc function (propvarutil.h)
description: Extracts data from a PROPVARIANT structure into a newly-allocated unsigned short vector.
helpviewer_keywords: ["PropVariantToUInt16VectorAlloc","PropVariantToUInt16VectorAlloc function [Windows Properties]","_shell_PropVariantToUInt16VectorAlloc","properties.PropVariantToUInt16VectorAlloc","propvarutil/PropVariantToUInt16VectorAlloc","shell.PropVariantToUInt16VectorAlloc"]
old-location: properties\PropVariantToUInt16VectorAlloc.htm
tech.root: properties
ms.assetid: e5af0f91-49c1-4ff3-8339-77fffc2102f8
ms.date: 12/05/2018
ms.keywords: PropVariantToUInt16VectorAlloc, PropVariantToUInt16VectorAlloc function [Windows Properties], _shell_PropVariantToUInt16VectorAlloc, properties.PropVariantToUInt16VectorAlloc, propvarutil/PropVariantToUInt16VectorAlloc, shell.PropVariantToUInt16VectorAlloc
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
 - PropVariantToUInt16VectorAlloc
 - propvarutil/PropVariantToUInt16VectorAlloc
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
 - PropVariantToUInt16VectorAlloc
---

# PropVariantToUInt16VectorAlloc function


## -description

Extracts data from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure into a newly-allocated <b>unsigned short</b> vector.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param pprgn [out]

Type: <b>USHORT**</b>

When this function returns, contains a pointer to a vector of <b>unsigned short</b> values extracted from the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param pcElem [out]

Type: <b>ULONG*</b>

 When this function returns, contains the count of <b>unsigned short</b> values extracted from the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

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
Returns <b>S_OK</b> if successful, or an error value otherwise

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

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a vector of <b>unsigned short</b> values.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type <b>VT_VECTOR</b> | <b>VT_UI2</b> or <b>VT_ARRAY</b> | <b>VT_UI2</b>, this function extracts a vector of <b>unsigned short</b> values into a newly allocated vector. The calling application is responsible for using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to release the vector pointed to by <i>pprgn</i> when it is no longer needed.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint16vectoralloc">PropVariantToUInt16VectorAlloc</a> to access a <b>unsigned short</b> vector value in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid. The application is expecting propvar to contain a vector of <dtype rid="ushort"/> values.
USHORT *prgShorts;
ULONG cElems;
HRESULT hr = PropVariantToUInt16VectorAlloc(propvar, & prgShorts, &cElems);
if (SUCCEEDED(hr))
{
     // prgShorts now points to a vector of cElems USHORTs.
     CoTaskMemFree(prgShorts);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromuint16vector">InitPropVariantFromUInt16Vector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetuint16elem">PropVariantGetUInt16Elem</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint16">PropVariantToUInt16</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint16vector">PropVariantToUInt16Vector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttouint16array">VariantToUInt16Array</a>