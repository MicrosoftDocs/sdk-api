---
UID: NF:propvarutil.PropVariantToBoolean
title: PropVariantToBoolean function (propvarutil.h)
description: Extracts a Boolean property value of a PROPVARIANT structure. If no value can be extracted, then a default value is assigned.
helpviewer_keywords: ["PropVariantToBoolean","PropVariantToBoolean function [Windows Properties]","properties.PropVariantToBoolean","propvarutil/PropVariantToBoolean","shell.PropVariantToBoolean","shell_PropVariantToBoolean"]
old-location: properties\PropVariantToBoolean.htm
tech.root: properties
ms.assetid: 74b9a388-8342-46e3-ac5e-b7c99e8f8f00
ms.date: 12/05/2018
ms.keywords: PropVariantToBoolean, PropVariantToBoolean function [Windows Properties], properties.PropVariantToBoolean, propvarutil/PropVariantToBoolean, shell.PropVariantToBoolean, shell_PropVariantToBoolean
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
 - PropVariantToBoolean
 - propvarutil/PropVariantToBoolean
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
 - PropVariantToBoolean
---

# PropVariantToBoolean function


## -description

Extracts a Boolean property value of a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure. If no value can be extracted, then a default value is assigned.

## -parameters

### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param pfRet [out]

Type: <b>BOOL*</b>

When this function returns, contains the extracted property value if one exists; otherwise, contains <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a Boolean value. For instance, an application obtaining values from a property store can use this to safely extract the Boolean value for Boolean properties.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type <b>VT_BOOL</b>, this helper function extracts the Boolean value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a Boolean. If a conversion is not possible, <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoboolean">PropVariantToBoolean</a> will return a failure code and set <i>pfRet</i> to <b>FALSE</b>. See <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a> for a list of possible conversions. Of note, <b>VT_EMPTY</b> is successfully converted to <b>FALSE</b>.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoboolean">PropVariantToBoolean</a> access a Boolean value in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// IPropertyStore *ppropstore;
// Assume variable ppropstore is initialized and valid
PROPVARIANT propvar = {0};

HRESULT hr = ppropstore->GetValue(PKEY_IsShared, &propvar);
if (SUCCEEDED(hr))
{
     // PKEY_IsShared is expected to produce a VT_BOOL or VT_EMPTY value.
     // PropVariantToBoolean will convert VT_EMPTY to FALSE.
     BOOL fShared;
     
     hr = PropVariantToBoolean(propvar, &fShared);
     if (SUCCEEDED(hr))
     {
         // fShared is now valid
     }
     else
     {
         // fShared is always FALSE
     }
     
     PropVariantClear(&propvar);
}

                    
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromboolean">InitPropVariantFromBoolean</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetbooleanelem">PropVariantGetBooleanElem</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttobooleanwithdefault">PropVariantToBooleanWithDefault</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttoboolean">VariantToBoolean</a>