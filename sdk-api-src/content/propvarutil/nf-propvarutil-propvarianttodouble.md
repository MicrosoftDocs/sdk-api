---
UID: NF:propvarutil.PropVariantToDouble
title: PropVariantToDouble function (propvarutil.h)
description: Extracts double value from a PROPVARIANT structure.
helpviewer_keywords: ["PropVariantToDouble","PropVariantToDouble function [Windows Properties]","properties.PropVariantToDouble","propvarutil/PropVariantToDouble","shell.PropVariantToDouble","shell_PropVariantToDouble"]
old-location: properties\PropVariantToDouble.htm
tech.root: properties
ms.assetid: 346b3f37-1279-4719-b1cd-50adf4d070f0
ms.date: 12/05/2018
ms.keywords: PropVariantToDouble, PropVariantToDouble function [Windows Properties], properties.PropVariantToDouble, propvarutil/PropVariantToDouble, shell.PropVariantToDouble, shell_PropVariantToDouble
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
 - PropVariantToDouble
 - propvarutil/PropVariantToDouble
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
 - PropVariantToDouble
---

# PropVariantToDouble function


## -description

Extracts double value from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -parameters

### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param pdblRet [out]

Type: <b>DOUBLE*</b>

When this function returns, contains the extracted property value if one exists; otherwise, contains 0.0.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a single double floating point value. For instance, an application obtaining values from a property store can use this to safely extract a double value for double properties.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type <b>VT_R8</b>, this helper function extracts the double value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a double. If a conversion is not possible, <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttodouble">PropVariantToDouble</a> will return a failure code and set <i>pdblRet</i> to 0.0. See <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a> for a list of possible conversions. Of note, <b>VT_EMPTY</b> is successfully converted to 0.0.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use PropVariantToDouble to access a double value in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// IPropertyStore *ppropstore;
// Assume variable ppropstore is initialized and valid
PROPVARIANT propvar = {0};
HRESULT hr = ppropstore->GetValue(PKEY_Image_HorizontalResolution, &propvar);
if (SUCCEEDED(hr))
{
     // PKEY_Image_HorizontalResolution is expected to produce a VT_R8 or VT_EMPTY value.
     // PropVariantToDouble will successfully convert VT_EMPTY to a 0.0.
     DOUBLE dblHorzResolution;
     hr = PropVariantToDouble(propvar, &dblHorzResolution);
     if (SUCCEEDED(hr))
     {
        // dblHorzResolution is now valid
     }
     else
     {
        // dblHorzResolution contains 0.0
     }
     PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromdouble">InitPropVariantFromDouble</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetdoubleelem">PropVariantGetDoubleElem</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttodoublewithdefault">PropVariantToDoubleWithDefault</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttodouble">VariantToDouble</a>