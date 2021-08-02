---
UID: NF:propvarutil.PropVariantToUInt64Vector
title: PropVariantToUInt64Vector function (propvarutil.h)
description: Extracts data from a PROPVARIANT structure into a ULONGLONG vector.
helpviewer_keywords: ["PropVariantToUInt64Vector","PropVariantToUInt64Vector function [Windows Properties]","_shell_PropVariantToUInt64Vector","properties.PropVariantToUInt64Vector","propvarutil/PropVariantToUInt64Vector","shell.PropVariantToUInt64Vector"]
old-location: properties\PropVariantToUInt64Vector.htm
tech.root: properties
ms.assetid: 596c7a35-6645-4f66-b924-b71278778776
ms.date: 12/05/2018
ms.keywords: PropVariantToUInt64Vector, PropVariantToUInt64Vector function [Windows Properties], _shell_PropVariantToUInt64Vector, properties.PropVariantToUInt64Vector, propvarutil/PropVariantToUInt64Vector, shell.PropVariantToUInt64Vector
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
 - PropVariantToUInt64Vector
 - propvarutil/PropVariantToUInt64Vector
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
 - PropVariantToUInt64Vector
---

# PropVariantToUInt64Vector function


## -description

Extracts data from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure into a <b>ULONGLONG</b> vector.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param prgn [out]

Type: <b>ULONGLONG*</b>

Points to a buffer containing <i>crgn</i>   <b>ULONGLONG</b> values. When this function returns, the buffer has been initialized with <i>pcElem</i>   <b>ULONGLONG</b> elements extracted from the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.

### -param crgn [in]

Type: <b>ULONG</b>

Size of the buffer pointed to by <i>prgn</i>, in elements.

### -param pcElem [out]

Type: <b>ULONG*</b>

When this function returns, contains the count of <b>ULONGLONG</b> values extracted from the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

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
<dt><b>TYPE_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> contained more than <i>crgn</i> values. The buffer pointed to by <i>prgn</i>.

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

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a vector of <b>ULONGLONG</b> values with a fixed number of elements.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type <b>VT_VECTOR</b> | <b>VT_UI8</b> or <b>VT_ARRAY</b> | <b>VT_UI8</b>, this helper function extracts up to <i>crgn</i>   <b>ULONGLONG</b> values and places them into the buffer pointed to by <i>prgn</i>. If the <b>PROPVARIANT</b> contains more elements than will fit into the <i>prgn</i> buffer, this function returns an error and sets <i>pcElem</i> to 0.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint64vector">PropVariantToUInt64Vector</a> to access a <b>ULONGLONG</b> vector value in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid
ULONGLONG rgLongs[4]; // The application is expecting propvar to hold 4 ULONGLONGs in a vector
ULONG cElems;
HRESULT hr = PropVariantToUInt64Vector(propvar, rgLongs, ARRAYSIZE(rgLongs), &cElems);
if (SUCCEEDED(hr))
{
     if (cElems == ARRAYSIZE(rgLongs))
     {
         // The application got 4 ULONGLONGs which are now stored in rgLongs
     }
     else
     {
         // The application got cElems which are stored in the first cElems elements of rgLongs
     }
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromuint64vector">InitPropVariantFromUInt64Vector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetuint64elem">PropVariantGetUInt64Elem</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint64">PropVariantToUInt64</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint64vectoralloc">PropVariantToUInt64VectorAlloc</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttouint64array">VariantToUInt64Array</a>