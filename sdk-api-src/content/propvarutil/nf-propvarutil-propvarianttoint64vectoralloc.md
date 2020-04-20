---
UID: NF:propvarutil.PropVariantToInt64VectorAlloc
title: PropVariantToInt64VectorAlloc function (propvarutil.h)
description: Extracts data from a PROPVARIANT structure into a newly-allocated LONGLONG vector.helpviewer_keywords: ["PropVariantToInt64VectorAlloc","PropVariantToInt64VectorAlloc function [Windows Properties]","_shell_PropVariantToInt64VectorAlloc","properties.PropVariantToInt64VectorAlloc","propvarutil/PropVariantToInt64VectorAlloc","shell.PropVariantToInt64VectorAlloc"]
old-location: properties\PropVariantToInt64VectorAlloc.htm
tech.root: properties
ms.assetid: 06f82bf5-5009-4c8b-9f99-4325328bc2e2
ms.date: 12/05/2018
ms.keywords: PropVariantToInt64VectorAlloc, PropVariantToInt64VectorAlloc function [Windows Properties], _shell_PropVariantToInt64VectorAlloc, properties.PropVariantToInt64VectorAlloc, propvarutil/PropVariantToInt64VectorAlloc, shell.PropVariantToInt64VectorAlloc
f1_keywords:
- propvarutil/PropVariantToInt64VectorAlloc
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Propsys.dll
api_name:
- PropVariantToInt64VectorAlloc
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# PropVariantToInt64VectorAlloc function


## -description


Extracts data from a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure into a newly-allocated <b>LONGLONG</b> vector.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.


### -param pprgn [out]

Type: <b>LONGLONG**</b>

When this function returns, contains a pointer to a vector of <b>LONGLONG</b> values extracted from the source <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.


### -param pcElem [out]

Type: <b>ULONG*</b>

When this function returns, contains the count of <b>LONGLONG</b> values extracted from source <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.


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
The<a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>was not of the appropriate type.

</td>
</tr>
</table>
 




## -remarks



This helper function is used in places where the calling application expects a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a vector of <b>LONGLONG</b> values.

If the source <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type <b>VT_VECTOR</b> | <b>VT_I8</b> or <b>VT_ARRAY</b> | <b>VT_I8</b>, this function extracts a vector of <b>LONGLONG</b> values into a newly allocated vector. The calling application is responsible for using <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to release the vector pointed to by <i>pprgn</i> when it is no longer needed. 


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint64vectoralloc">PropVariantToInt64VectorAlloc</a> to access a <b>LONGLONG</b> vector value in a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid. The application is expecting propvar to contain a vector of LONGLONG values.
LONGLONG *prgLongs;
ULONG cElems;
HRESULT hr = PropVariantToInt64VectorAlloc(propvar, &prgLongs, &cElems);
if (SUCCEEDED(hr))
{
     // prgLongs now points to a vector of cElems LONGLONGs.
     CoTaskMemFree(prgLongs);
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromint64vector">InitPropVariantFromInt64Vector</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetint64elem">PropVariantGetInt64Elem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint64">PropVariantToInt64</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint64vector">PropVariantToInt64Vector</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-varianttoint64array">VariantToInt64Array</a>
 

 

