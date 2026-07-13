---
UID: NF:propvarutil.PropVariantToFileTimeVectorAlloc
title: PropVariantToFileTimeVectorAlloc function (propvarutil.h)
description: Extracts data from a PROPVARIANT structure into a newly-allocated FILETIME vector.
helpviewer_keywords: ["PropVariantToFileTimeVectorAlloc","PropVariantToFileTimeVectorAlloc function [Windows Properties]","_shell_PropVariantToFileTimeVectorAlloc","properties.PropVariantToFileTimeVectorAlloc","propvarutil/PropVariantToFileTimeVectorAlloc","shell.PropVariantToFileTimeVectorAlloc"]
old-location: properties\PropVariantToFileTimeVectorAlloc.htm
tech.root: properties
ms.assetid: 2d0125fe-f4af-451b-8dc7-d29a35cc927e
ms.date: 12/05/2018
ms.keywords: PropVariantToFileTimeVectorAlloc, PropVariantToFileTimeVectorAlloc function [Windows Properties], _shell_PropVariantToFileTimeVectorAlloc, properties.PropVariantToFileTimeVectorAlloc, propvarutil/PropVariantToFileTimeVectorAlloc, shell.PropVariantToFileTimeVectorAlloc
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
 - PropVariantToFileTimeVectorAlloc
 - propvarutil/PropVariantToFileTimeVectorAlloc
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
 - PropVariantToFileTimeVectorAlloc
---

# PropVariantToFileTimeVectorAlloc function


## -description

Extracts data from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure into a newly-allocated FILETIME vector.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param pprgft [out]

Type: <b>FILETIME**</b>

 When this function returns, contains a pointer to a vector of FILETIME values extracted from the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param pcElem [out]

Type: <b>ULONG*</b>

When this function returns, contains the count of FILETIME elements extracted from source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

Returns one of the following values.

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

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a FILETIME vector value.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type VT_VECTOR | VT_FILETIME, this function extracts a vector of FILETIMEs values into a newly allocated vector of FILETIME values. The calling application is responsible for using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to release the vector pointed to by <i>pprgft</i> when it is no longer needed.

The output FILETIMEs will use the same time zone as the source FILETIMEs.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttofiletimevectoralloc">PropVariantToFileTimeVectorAlloc</a> to access a FILETIME vector value in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid. 
// The application is expecting propvar to contain a vector of FILETIME values.
BOOL *prgTimes;
ULONG cTimes;
HRESULT hr = PropVariantToBooleanVectorAlloc(propvar, &prgTimes, &cTimes);
if (SUCCEEDED(hr))
{
     // prgTimes now points to a vector of cTimes file times.
     CoTaskMemFree(prgTimes);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromfiletimevector">InitPropVariantFromFileTimeVector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttofiletime">PropVariantToFileTime</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttofiletimevector">PropVariantToFileTimeVector</a>