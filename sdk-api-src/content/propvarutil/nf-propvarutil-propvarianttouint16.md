---
UID: NF:propvarutil.PropVariantToUInt16
title: PropVariantToUInt16 function (propvarutil.h)
description: Extracts a unsigned short value from a PROPVARIANT structure. If no value can be extracted, then a default value is assigned.
helpviewer_keywords: ["PropVariantToUInt16","PropVariantToUInt16 function [Windows Properties]","properties.PropVariantToUInt16","propvarutil/PropVariantToUInt16","shell.PropVariantToUInt16","shell_PropVariantToUInt16"]
old-location: properties\PropVariantToUInt16.htm
tech.root: properties
ms.assetid: 4499842b-c802-4328-b463-f3cfb270e635
ms.date: 12/05/2018
ms.keywords: PropVariantToUInt16, PropVariantToUInt16 function [Windows Properties], properties.PropVariantToUInt16, propvarutil/PropVariantToUInt16, shell.PropVariantToUInt16, shell_PropVariantToUInt16
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
 - PropVariantToUInt16
 - propvarutil/PropVariantToUInt16
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
 - PropVariantToUInt16
---

# PropVariantToUInt16 function


## -description

Extracts a <b>unsigned short</b> value from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure. If no value can be extracted, then a default value is assigned.

## -parameters

### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param puiRet [out]

Type: <b>USHORT*</b>

When this function returns, contains the extracted property value if one exists; otherwise, 0.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a <b>unsigned short</b> value. For instance, an application obtaining values from a property store can use this to safely extract the <b>unsigned short</b> value for UInt16 properties.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type <b>VT_UI2</b>, this helper function extracts the <b>unsigned short</b> value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a USHORT. If a conversion is not possible, <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint16">PropVariantToUInt16</a> will return a failure code and set <i>puiRet</i> to 0. See <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a> for a list of possible conversions. Of note, VT_EMPTY is successfully converted to 0.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint16">PropVariantToUInt16</a> to access a <b>unsigned short</b> value in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// IPropertyStore *ppropstore;

// Assume variable ppropstore is initialized and valid

PROPVARIANT propvar = {0};

HRESULT hr = ppropstore->GetValue(PKEY_FlagColor, &propvar);

if (SUCCEEDED(hr))

{

     // PKEY_FlagColor is expected to produce a VT_UI2 or VT_EMPTY value.

     // PropVariantToUInt16 will convert VT_EMPTY to 0.

     USHORT uColor;

     hr = PropVariantToUInt16(propvar, & uColor);

     if (SUCCEEDED(hr))

     {

             // uColor is now valid

     }

     else

     {

             // uColor is always 0

     }

     PropVariantClear(&propvar);

}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromuint16">InitPropVariantFromUInt16</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint16vector">PropVariantToUInt16Vector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttouint16">VariantToUInt16</a>