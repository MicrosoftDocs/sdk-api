---
UID: NF:propvarutil.PropVariantToStringVectorAlloc
title: PropVariantToStringVectorAlloc function (propvarutil.h)
description: Extracts data from a PROPVARIANT structure into a newly allocated strings in a newly allocated vector.
helpviewer_keywords: ["PropVariantToStringVectorAlloc","PropVariantToStringVectorAlloc function [Windows Properties]","_shell_PropVariantToStringVectorAlloc","properties.PropVariantToStringVectorAlloc","propvarutil/PropVariantToStringVectorAlloc","shell.PropVariantToStringVectorAlloc"]
old-location: properties\PropVariantToStringVectorAlloc.htm
tech.root: properties
ms.assetid: bf2cacc9-89d5-4823-99da-9747636b3795
ms.date: 12/05/2018
ms.keywords: PropVariantToStringVectorAlloc, PropVariantToStringVectorAlloc function [Windows Properties], _shell_PropVariantToStringVectorAlloc, properties.PropVariantToStringVectorAlloc, propvarutil/PropVariantToStringVectorAlloc, shell.PropVariantToStringVectorAlloc
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
 - PropVariantToStringVectorAlloc
 - propvarutil/PropVariantToStringVectorAlloc
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
 - PropVariantToStringVectorAlloc
---

# PropVariantToStringVectorAlloc function


## -description

Extracts data from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure into a newly allocated strings in a newly allocated vector.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param pprgsz [out]

Type: <b>PWSTR**</b>

When this function returns, contains a pointer to a vector of strings extracted from source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param pcElem [out]

Type: <b>ULONG*</b>

When this function returns, contains the count of string elements extracted from source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

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

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a vector of string values.

This helper function works for the following<a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> types:
            

<ul>
<li>VT_VECTOR | VT_LPWSTR</li>
<li>VT_VECTOR | VT_BSTR</li>
<li>VT_ARRAY | VT_BSTR</li>
</ul>
If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has a supported type, this function extracts a vector of string values into a newly allocated vector of newly allocated strings. The calling application is responsible for using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to release both the strings contained in the output vector, and the output vector itself, when they are no longer needed.

If a <b>BSTR</b> in the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> is <b>NULL</b>, this function will place a newly allocated string containing "" into the output vector.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostringvectoralloc">PropVariantToStringVectorAlloc</a> to access a string vector value in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// IPropertyStore *ppropstore;
// Assume variable ppropstore is initialized and valid
PROPVARIANT propvar = {0};
HRESULT hr = ppropstore->GetValue(PKEY_Keywords, &propvar);
if (SUCCEEDED(hr))
{
         // PKEY_Keywords is expected to produce a VT_VECTOR | VT_LPWSTR, or VT_EMPTY
         // PropVariantToStringVectorAlloc will return an error for VT_EMPTY
         LPWSTR *prgKeywords;
         ULONG cElem;
         hr = PropVariantToStringVectorAlloc (propvar, &prgKeywords, &cElem);
         if (SUCCEEDED(hr))
         {
                 // prgKeywords contains cElem strings
                 for (ULONG i = 0; i < cElem; i++)
                 {
                          CoTaskMemFree(prgKeywords[i]);
                 }
                 CoTaskMemFree(prgKeywords);
         }
         else
         {
                 // propvar either is VT_EMPTY, or contains something other than a vector of  strings
         }
         PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromstringvector">InitPropVariantFromStringVector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetstringelem">PropVariantGetStringElem</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostring">PropVariantToString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostringvector">PropVariantToStringVector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttostringarray">VariantToStringArray</a>