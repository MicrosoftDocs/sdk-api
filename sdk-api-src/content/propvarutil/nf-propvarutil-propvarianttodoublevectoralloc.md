---
UID: NF:propvarutil.PropVariantToDoubleVectorAlloc
title: PropVariantToDoubleVectorAlloc function (propvarutil.h)
description: Extracts data from a PROPVARIANT structure into a newly-allocated double vector.
helpviewer_keywords: ["PropVariantToDoubleVectorAlloc","PropVariantToDoubleVectorAlloc function [Windows Properties]","_shell_PropVariantToDoubleVectorAlloc","properties.PropVariantToDoubleVectorAlloc","propvarutil/PropVariantToDoubleVectorAlloc","shell.PropVariantToDoubleVectorAlloc"]
old-location: properties\PropVariantToDoubleVectorAlloc.htm
tech.root: properties
ms.assetid: 80f05530-a92b-4877-80fa-efac8e999510
ms.date: 12/05/2018
ms.keywords: PropVariantToDoubleVectorAlloc, PropVariantToDoubleVectorAlloc function [Windows Properties], _shell_PropVariantToDoubleVectorAlloc, properties.PropVariantToDoubleVectorAlloc, propvarutil/PropVariantToDoubleVectorAlloc, shell.PropVariantToDoubleVectorAlloc
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
 - PropVariantToDoubleVectorAlloc
 - propvarutil/PropVariantToDoubleVectorAlloc
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
 - PropVariantToDoubleVectorAlloc
---

# PropVariantToDoubleVectorAlloc function


## -description

Extracts data from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure into a newly-allocated double vector.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param pprgn [out]

Type: <b>DOUBLE**</b>

When this function returns, contains a pointer to a vector of double values extracted from the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param pcElem [out]

Type: <b>ULONG*</b>

When this function returns, contains the count of double elements extracted from the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a double vector value.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type VT_VECTOR | VT_R8 or VT_ARRAY | VT_R8, this function extracts a vector of double values into a newly allocated vector of DOUBLE values. The calling application is responsible for using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to release the vector pointed to by <i>pprgn</i> when it is no longer needed.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttodoublevector">PropVariantToDoubleVector</a> to access a double vector value in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// IPropertyStore *ppropstore;
// Assume variable ppropstore is initialized and valid
PROPVARIANT propvar = {0};
HRESULT hr = ppropstore->GetValue(PKEY_GPS_DestLongitude, &propvar);
if (SUCCEEDED(hr))
{
     // PKEY_GPS_DestLongitude is expected to produce a VT_VECTOR | VT_R8 with three values, or VT_EMPTY
     // PropVariantToDoubleVectorAlloc will return an error for VT_EMPTY
     DOUBLE *rgLongitude;
     ULONG cElem;
     hr = PropVariantToDoubleVectorAlloc(propvar, &rgLongitude, &cElem);
     if (SUCCEEDED(hr))
     {
         if (cElem == 3)
         {
              // rgLongitude contains 3 doubles representing the degrees, minutes, and seconds of longitude
         }
         CoTaskMemFree(rgLongitude);
     }
     else
     {
          // propvar either is VT_EMPTY, or contains something other than a vector of  doubles
     }
     PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromdoublevector">InitPropVariantFromDoubleVector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetdoubleelem">PropVariantGetDoubleElem</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttodouble">PropVariantToDouble</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttodoublevector">PropVariantToDoubleVector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttodoublearray">VariantToDoubleArray</a>