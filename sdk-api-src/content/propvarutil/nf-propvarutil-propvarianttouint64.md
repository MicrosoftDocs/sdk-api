---
UID: NF:propvarutil.PropVariantToUInt64
title: PropVariantToUInt64 function (propvarutil.h)
description: Extracts a UInt64 value from a PROPVARIANT structure. If no value can be extracted, then a default value is assigned.
helpviewer_keywords: ["PropVariantToUInt64","PropVariantToUInt64 function [Windows Properties]","properties.PropVariantToUInt64","propvarutil/PropVariantToUInt64","shell.PropVariantToUInt64","shell_PropVariantToUInt64"]
old-location: properties\PropVariantToUInt64.htm
tech.root: properties
ms.assetid: 3a6bdfb0-eae1-40e7-85c1-234732a4bc3f
ms.date: 12/05/2018
ms.keywords: PropVariantToUInt64, PropVariantToUInt64 function [Windows Properties], properties.PropVariantToUInt64, propvarutil/PropVariantToUInt64, shell.PropVariantToUInt64, shell_PropVariantToUInt64
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
 - PropVariantToUInt64
 - propvarutil/PropVariantToUInt64
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
 - PropVariantToUInt64
---

# PropVariantToUInt64 function


## -description

Extracts a <b>UInt64</b> value from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure. If no value can be extracted, then a default value is assigned.

## -parameters

### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param pullRet [out]

Type: <b>ULONGLONG*</b>

When this function returns, contains the extracted property value if one exists; otherwise, 0.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a <b>ULONGLONG</b> value. For instance, an application obtaining values from a property store can use this to safely extract the <b>ULONGLONG</b>  value for <b>UInt64</b> properties.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type <b>VT_UI8</b>, this helper function extracts the <b>ULONGLONG</b>  value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a <b>ULONGLONG</b>. If a conversion is not possible, <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint64">PropVariantToUInt64</a> will return a failure code and set <i>pullRet</i> to 0. See <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a> for a list of possible conversions. Of note, <b>VT_EMPTY</b> is successfully converted to 0.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint64">PropVariantToUInt64</a> to access a <b>ULONGLONG</b> value in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// IPropertyStore *ppropstore;

// Assume variable ppropstore is initialized and valid

PROPVARIANT propvar = {0};

HRESULT hr = ppropstore->GetValue(PKEY_Size, &propvar);

if (SUCCEEDED(hr))

{

     // PKEY_Size is expected to produce a VT_UI8 or VT_EMPTY value.

     // PropVariantToUInt64 will convert VT_EMPTY to 0.

     ULONGLONG ullSize;

     hr = PropVariantToUInt64(propvar, &ullSize);

     if (SUCCEEDED(hr))

     {

             // ullSize is now valid

     }

     else

     {

             // ullSize is always 0

     }

     PropVariantClear(&propvar);

}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromuint64">InitPropVariantFromUInt64</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint64vector">PropVariantToUInt64Vector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttouint64">VariantToUInt64</a>