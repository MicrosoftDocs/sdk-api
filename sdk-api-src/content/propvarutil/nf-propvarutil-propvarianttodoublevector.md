---
UID: NF:propvarutil.PropVariantToDoubleVector
title: PropVariantToDoubleVector function (propvarutil.h)
description: Extracts a vector of doubles from a PROPVARIANT structure.
helpviewer_keywords: ["PropVariantToDoubleVector","PropVariantToDoubleVector function [Windows Properties]","_shell_PropVariantToDoubleVector","properties.PropVariantToDoubleVector","propvarutil/PropVariantToDoubleVector","shell.PropVariantToDoubleVector"]
old-location: properties\PropVariantToDoubleVector.htm
tech.root: properties
ms.assetid: 2d90bf96-8a3f-4949-8480-bb75f0deeb2e
ms.date: 12/05/2018
ms.keywords: PropVariantToDoubleVector, PropVariantToDoubleVector function [Windows Properties], _shell_PropVariantToDoubleVector, properties.PropVariantToDoubleVector, propvarutil/PropVariantToDoubleVector, shell.PropVariantToDoubleVector
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
 - PropVariantToDoubleVector
 - propvarutil/PropVariantToDoubleVector
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
 - PropVariantToDoubleVector
---

# PropVariantToDoubleVector function


## -description

Extracts a vector of doubles from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param prgn [out]

Type: <b>DOUBLE*</b>

Points to a buffer containing <i>crgn</i> DOUBLE values. When this function returns, the buffer has been initialized with <i>pcElem</i> double elements extracted from the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param crgn [in]

Type: <b>ULONG</b>

Size in elements of the buffer pointed to by <i>prgn</i>.

### -param pcElem [out]

Type: <b>ULONG*</b>

When this function returns, contains the count of double elements extracted from the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a double vector value with a fixed number of elements.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type VT_VECTOR | VT_R8 or VT_ARRAY | VT_R8, this helper function extracts up to <i>crgn</i> double values and places them into the buffer pointed to by <i>prgn</i>. If the <b>PROPVARIANT</b> contains more elements than will fit into the <i>prgn</i> buffer, this function returns an error and sets <i>pcElem</i> to 0.


#### Examples


```cpp
// IPropertyStore *ppropstore;
// Assume variable ppropstore is initialized and valid
PROPVARIANT propvar = {0};
HRESULT hr = ppropstore->GetValue(PKEY_GPS_DestLongitude, &propvar);
if (SUCCEEDED(hr))
{
         // PKEY_GPS_DestLongitude is expected to produce a VT_VECTOR | VT_R8 with three values, or VT_EMPTY
         // PropVariantToDoubleVector will return an error for VT_EMPTY
         DOUBLE rgLongitude[3];
         ULONG cElem;
         hr = PropVariantToDoubleVector(propvar, &rgLongitude, ARRAYSIZE(rgLongitude), &cElem);
         if (SUCCEEDED(hr))
         {
                 if (cElem == ARRAYSIZE(rgLongitude))
                 {
                          // rgLongitude contains 3 doubles representing the degrees, minutes, and seconds of longitude
                 }
                 else
                 {
                          // The first cElem doubles from propvar are stored in the first 3 elements of rgLongitude
         }
         else
         {
                 // propvar either is VT_EMPTY, or contains something other than a vector of 3 doubles
         }
         PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromdoublevector">InitPropVariantFromDoubleVector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetdoubleelem">PropVariantGetDoubleElem</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttodouble">PropVariantToDouble</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttodoublevectoralloc">PropVariantToDoubleVectorAlloc</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttodoublearray">VariantToDoubleArray</a>