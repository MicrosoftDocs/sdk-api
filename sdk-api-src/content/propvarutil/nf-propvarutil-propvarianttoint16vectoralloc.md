---
UID: NF:propvarutil.PropVariantToInt16VectorAlloc
title: PropVariantToInt16VectorAlloc function (propvarutil.h)
description: Extracts data from a PROPVARIANT structure into a newly allocated Int16 vector.
helpviewer_keywords: ["PropVariantToInt16VectorAlloc","PropVariantToInt16VectorAlloc function [Windows Properties]","_shell_PropVariantToInt16VectorAlloc","properties.PropVariantToInt16VectorAlloc","propvarutil/PropVariantToInt16VectorAlloc","shell.PropVariantToInt16VectorAlloc"]
old-location: properties\PropVariantToInt16VectorAlloc.htm
tech.root: properties
ms.assetid: 489aff33-2faa-480a-a146-67f6ef4b8b93
ms.date: 12/05/2018
ms.keywords: PropVariantToInt16VectorAlloc, PropVariantToInt16VectorAlloc function [Windows Properties], _shell_PropVariantToInt16VectorAlloc, properties.PropVariantToInt16VectorAlloc, propvarutil/PropVariantToInt16VectorAlloc, shell.PropVariantToInt16VectorAlloc
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
 - PropVariantToInt16VectorAlloc
 - propvarutil/PropVariantToInt16VectorAlloc
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
 - PropVariantToInt16VectorAlloc
---

# PropVariantToInt16VectorAlloc function


## -description

Extracts data from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure into a newly allocated <b>Int16</b> vector.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param pprgn [out]

Type: <b>SHORT**</b>

When this function returns, contains a pointer to a vector of <b>Int16</b> values extracted from the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param pcElem [out]

Type: <b>ULONG*</b>

 When this function returns, contains the count of <b>Int16</b> elements extracted from source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

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

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold an <b>Int16</b> vector value.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type VT_VECTOR | VT_I2 or VT_ARRAY | VT_I2, this function extracts a vector of <b>Int16</b> values into a newly allocated vector of SHORT values. The calling application is responsible for using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to release the vector pointed to by <i>pprgn</i> when it is no longer needed.


#### Examples

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold an Int16 vector value.


```cpp
// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid. The application is expecting propvar to contain a vector of Int16 values.
SHORT *prgShorts;
ULONG cElems;
HRESULT hr = PropVariantToBooleanVectorAlloc(propvar, & prgShorts, &cElems);
if (SUCCEEDED(hr))
{
     // prgShorts now points to a vector of cElems SHORTs.
     CoTaskMemFree(prgShorts);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromint16vector">InitPropVariantFromInt16Vector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetint16elem">PropVariantGetInt16Elem</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint16">PropVariantToInt16</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint16vector">PropVariantToInt16Vector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttoint16array">VariantToInt16Array</a>