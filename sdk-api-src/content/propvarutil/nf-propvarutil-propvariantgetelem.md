---
UID: NF:propvarutil.PropVariantGetElem
title: PropVariantGetElem function (propvarutil.h)
description: Initializes a PROPVARIANT structure based on a specified element in another PROPVARIANT structure.
helpviewer_keywords: ["PropVariantGetElem","PropVariantGetElem function [Windows Properties]","_shell_PropVariantGetElem","properties.PropVariantGetElem","propvarutil/PropVariantGetElem","shell.PropVariantGetElem"]
old-location: properties\PropVariantGetElem.htm
tech.root: properties
ms.assetid: 462eca81-1010-4518-ba55-0ac144297798
ms.date: 12/05/2018
ms.keywords: PropVariantGetElem, PropVariantGetElem function [Windows Properties], _shell_PropVariantGetElem, properties.PropVariantGetElem, propvarutil/PropVariantGetElem, shell.PropVariantGetElem
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - PropVariantGetElem
 - propvarutil/PropVariantGetElem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propvarutil.h
api_name:
 - PropVariantGetElem
---

# PropVariantGetElem function


## -description

Initializes a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure based on a specified element in another <b>PROPVARIANT</b> structure.

## -parameters

### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param iElem [in]

Type: <b>ULONG</b>

Index of a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure element in <i>propvarIn</i>.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this function returns, contains a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> with the value specified from the source <b>PROPVARIANT</b> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This helper function works for <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structures of the following types:
           
                

<ul>
<li>VT_LPWSTR</li>
<li>VT_BSTR</li>
<li>VT_BOOL</li>
<li>VT_I2</li>
<li>VT_I4</li>
<li>VT_I8</li>
<li>VT_U12</li>
<li>VT_U14</li>
<li>VT_U18</li>
<li>VT_FILETIME</li>
<li>VT_VECTOR | (any one of VT_LPWSTR, VT_BSTR, VT_BOOL, VT_I2, VT_I4, VT_I8, VT_U12, VT_U14, VT_U18, VT_FILETIME)</li>
<li>VT_ARRAY | (any one of  VT_BSTR, VT_BOOL, VT_I2, VT_I4, VT_I8, VT_U12, VT_U14, VT_U18)</li>
</ul>
Additional types may be supported in the future.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.

This function extracts a single value from the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure and uses that value to initialize the output <b>PROPVARIANT</b> structure. The calling application must use <a href="/previous-versions/windows/desktop/oe/oe-imimeallocator-propvariantclear">PropVariantClear</a> to free the <b>PROPVARIANT</b> referred to by <i>ppropvar</i> when it is no longer needed.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> is a vector or array, <i>iElem</i> must be less than the number of elements in the vector or array.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has only a single value, <i>iElem</i> must be 0.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> is empty, this function always returns an error code.

<div class="alert"><b>Note</b>  You can use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetelementcount">PropVariantGetElementCount</a> to obtain the number of elements in the vector or array.</div>
<div> </div>

#### Examples

The following code example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetelem">PropVariantGetElem</a> in an iteration statement to access the values in <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// PROPVARIANT propvar;
// Assume propvar is initialized and valid.

UINT cElem = PropVariantGetElementCount(propvar);
HRESULT hr = <mark type="const">S_OK</mark>;

for (UINT iElem = 0; SUCCEEDED(hr) && iElem < cElem; iElem ++)
{
   <xref rid="_stg_propvariant"/>propvarElem = {0};
    
    hr = PropVariantGetElem(propvar, iElem, &propvarElem);

    if (SUCCEEDED(hr))
    {
        // propvarElem is valid now.
        PropVariantClear(&propvarElem);
    }
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfrompropvariantvectorelem">InitPropVariantFromPropVariantVectorElem</a>