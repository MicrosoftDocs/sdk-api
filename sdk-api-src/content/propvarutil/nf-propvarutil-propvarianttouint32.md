---
UID: NF:propvarutil.PropVariantToUInt32
title: PropVariantToUInt32 function (propvarutil.h)
description: Extracts an ULONG value from a PROPVARIANT structure. If no value can be extracted, then a default value is assigned.
helpviewer_keywords: ["PropVariantToUInt32","PropVariantToUInt32 function [Windows Properties]","properties.PropVariantToUInt32","propvarutil/PropVariantToUInt32","shell.PropVariantToUInt32","shell_PropVariantToUInt32"]
old-location: properties\PropVariantToUInt32.htm
tech.root: properties
ms.assetid: ce1d8d07-2532-48bd-be8b-7650230dbe0d
ms.date: 12/05/2018
ms.keywords: PropVariantToUInt32, PropVariantToUInt32 function [Windows Properties], properties.PropVariantToUInt32, propvarutil/PropVariantToUInt32, shell.PropVariantToUInt32, shell_PropVariantToUInt32
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
 - PropVariantToUInt32
 - propvarutil/PropVariantToUInt32
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
 - PropVariantToUInt32
---

# PropVariantToUInt32 function


## -description

Extracts an <b>ULONG</b> value from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure. If no value can be extracted, then a default value is assigned.

## -parameters

### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

A reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param pulRet [out]

Type: <b>ULONG*</b>

When this function returns, contains the extracted property value if one exists; otherwise, 0.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a <b>ULONG</b> value. For instance, an application obtaining values from a property store can use this to safely extract the <b>ULONG</b>  value for UInt32 properties.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type <b>VT_UI4</b>, this helper function extracts the <b>ULONG</b> value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a <b>ULONG</b>. If a conversion is not possible, <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint32">PropVariantToUInt32</a> will return a failure code and set <i>pulRet</i> to 0. See <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a> for a list of possible conversions. Of note, <b>VT_EMPTY</b> is successfully converted to 0.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint32">PropVariantToUInt32</a> to access a <b>ULONG</b> value in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// IPropertyStore *ppropstore;

// Assume variable ppropstore is initialized and valid

PROPVARIANT propvar = {0};

HRESULT hr = ppropstore->GetValue(PKEY_Rating, &propvar);

if (SUCCEEDED(hr))

{

     // PKEY_Rating is expected to produce a VT_UI4 or VT_EMPTY value.

     // PropVariantToUInt32 will convert VT_EMPTY to 0.

     ULONG uRating;

     hr = PropVariantToUInt32(propvar, &uRating);

     if (SUCCEEDED(hr))

     {

             // uRating is now valid

     }

     else

     {

             // uRating is always 0

     }

     PropVariantClear(&propvar);

}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromuint32">InitPropVariantFromUInt32</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint32vector">PropVariantToUInt32Vector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttouint32">VariantToUInt32</a>