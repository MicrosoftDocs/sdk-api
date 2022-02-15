---
UID: NF:propvarutil.PropVariantToInt16Vector
title: PropVariantToInt16Vector function (propvarutil.h)
description: Extracts a vector of Int16 values from a PROPVARIANT structure.
helpviewer_keywords: ["PropVariantToInt16Vector","PropVariantToInt16Vector function [Windows Properties]","_shell_PropVariantToInt16Vector","properties.PropVariantToInt16Vector","propvarutil/PropVariantToInt16Vector","shell.PropVariantToInt16Vector"]
old-location: properties\PropVariantToInt16Vector.htm
tech.root: properties
ms.assetid: 33240552-7caa-4114-aad6-7341551b1fbe
ms.date: 12/05/2018
ms.keywords: PropVariantToInt16Vector, PropVariantToInt16Vector function [Windows Properties], _shell_PropVariantToInt16Vector, properties.PropVariantToInt16Vector, propvarutil/PropVariantToInt16Vector, shell.PropVariantToInt16Vector
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
 - PropVariantToInt16Vector
 - propvarutil/PropVariantToInt16Vector
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
 - PropVariantToInt16Vector
---

# PropVariantToInt16Vector function


## -description

Extracts a vector of <b>Int16</b> values from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param prgn [out]

Type: <b>SHORT*</b>

 Points to a buffer containing <i>crgn</i> SHORT values. When this function returns, the buffer has been initialized with <i>pcElem</i> SHORT elements extracted from the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param crgn [in]

Type: <b>ULONG</b>

Size of the buffer pointed to by <i>prgn</i> in elements.

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
The<a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> was not of the appropriate type.

</td>
</tr>
</table>

## -remarks

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold an <b>Int16</b> vector value with a fixed number of elements.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type VT_VECTOR | VT_I2 or VT_ARRAY | VT_I2, this helper function extracts up to <i>crgn</i> Int16 values and places them into the buffer pointed to by <i>prgn</i>. If the <b>PROPVARIANT</b> contains more elements than will fit into the <i>prgn</i> buffer, this function returns an error and sets <i>pcElem</i> to 0.


#### Examples


```cpp
// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid
SHORT rgShorts[4]; // The application is expecting propvar to hold 4 Int16s in a vector
ULONG cElems;
HRESULT hr = PropVariantToInt16Vector(propvar, rgShorts, ARRAYSIZE(rgShorts), &cElems);
if (SUCCEEDED(hr))
{
     if (cElems == ARRAYSIZE(rgShorts))
     {
         // The application got 4 Int16s which are now stored in rgShorts
     }
     else
     {
         // The application got cElems which are stored in the first cElems elements of rgShorts
     }
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromint16vector">InitPropVariantFromInt16Vector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetint16elem">PropVariantGetInt16Elem</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint16">PropVariantToInt16</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint16vectoralloc">PropVariantToInt16VectorAlloc</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttoint16array">VariantToInt16Array</a>