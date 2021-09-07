---
UID: NF:propvarutil.PropVariantToInt32
title: PropVariantToInt32 function (propvarutil.h)
description: Extracts the Int32 property value of a PROPVARIANT structure. If no value can be extracted, then a default value is assigned.
helpviewer_keywords: ["PropVariantToInt32","PropVariantToInt32 function [Windows Properties]","properties.PropVariantToInt32","propvarutil/PropVariantToInt32","shell.PropVariantToInt32","shell_PropVariantToInt32"]
old-location: properties\PropVariantToInt32.htm
tech.root: properties
ms.assetid: 937722d6-cabf-4c4d-8ca9-06d6ed91b77a
ms.date: 12/05/2018
ms.keywords: PropVariantToInt32, PropVariantToInt32 function [Windows Properties], properties.PropVariantToInt32, propvarutil/PropVariantToInt32, shell.PropVariantToInt32, shell_PropVariantToInt32
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
 - PropVariantToInt32
 - propvarutil/PropVariantToInt32
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
 - PropVariantToInt32
---

# PropVariantToInt32 function


## -description

Extracts the <b>Int32</b> property value of a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure. If no value can be extracted, then a default value is assigned.

## -parameters

### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param plRet [out]

Type: <b>LONG*</b>

When this function returns, contains the extracted value if one exists; otherwise, 0.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold an <b>Int32</b> value. For instance, an application obtaining values from a property store can use this to safely extract the <b>Int32</b> value for <b>Int32</b> properties.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type <b>VT_I4</b>, this helper function extracts the <b>long</b> value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a <b>long</b>. If a conversion is not possible, <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint32">PropVariantToInt32</a> will return a failure code and set <i>plRet</i> to 0. See <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a> for a list of possible conversions. Of note, <b>VT_EMPTY</b> is successfully converted to 0.


#### Examples


```cpp
// IPropertyStore *ppropstore;

// Assume variable ppropstore is initialized and valid

PROPVARIANT propvar = {0};

HRESULT hr = ppropstore->GetValue(PKEY_FlagStatus, &propvar);

if (SUCCEEDED(hr))

{

     // PKEY_FlagStatus is expected to produce a VT_I4 or VT_EMPTY value.

     // PropVariantToInt32 will convert VT_EMPTY to 0.

     INT32 iStatus;

     hr = PropVariantToInt32(propvar, &iStatus);

     if (SUCCEEDED(hr))

     {

             // iStatus is now valid

     }

     else

     {

             // iStatus is always 0

     }

     PropVariantClear(&propvar);

}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromint32">InitPropVariantFromInt32</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint32vector">PropVariantToInt32Vector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttoint32">VariantToInt32</a>