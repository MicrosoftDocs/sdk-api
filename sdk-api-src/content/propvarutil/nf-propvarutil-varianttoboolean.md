---
UID: NF:propvarutil.VariantToBoolean
title: VariantToBoolean function (propvarutil.h)
description: Extracts the value of a Boolean property from a VARIANT structure. If no value can be extracted, then a default value is assigned.
helpviewer_keywords: ["VariantToBoolean","VariantToBoolean function [Windows Properties]","_shell_VariantToBoolean","properties.VariantToBoolean","propvarutil/VariantToBoolean","shell.VariantToBoolean"]
old-location: properties\VariantToBoolean.htm
tech.root: properties
ms.assetid: 3ad12c41-e124-45f1-99f1-92790121ad93
ms.date: 12/05/2018
ms.keywords: VariantToBoolean, VariantToBoolean function [Windows Properties], _shell_VariantToBoolean, properties.VariantToBoolean, propvarutil/VariantToBoolean, shell.VariantToBoolean
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
 - VariantToBoolean
 - propvarutil/VariantToBoolean
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
 - VariantToBoolean
---

# VariantToBoolean function


## -description

Extracts the value of a Boolean property from a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure. If no value can be extracted, then a default value is assigned.

## -parameters

### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

### -param pfRet [out]

Type: <b>BOOL*</b>

When this function returns, contains the extracted value if one exists; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This helper function is used when the calling application expects a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> to hold a Boolean value. For instance, an application that obtains values from a Shell folder can use this function to safely extract the value from one of the folder's Boolean properties.

If the source <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> is of type VT_BOOL, this function extracts the <b>BOOL</b> value.

If the source <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> is not of type VT_BOOL, this function attempts to convert the value in the <b>VARIANT</b> structure into a <b>BOOL</b>. If a conversion is not possible, <a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttoboolean">VariantToBoolean</a> returns a failure code and sets <i>pfRet</i> to <b>FALSE</b>. See <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a> for a list of possible conversions. Of note, VT_EMPTY is successfully converted to <b>FALSE</b>.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttoboolean">VariantToBoolean</a> to access a <b>BOOL</b> value in a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a>.


```cpp
// VARIANT var;
// Assume variable var is initialize and valid. 
// The application expects it to hold a VT_BOOL value.
BOOL fValue;

HRESULT hr = VariantToBoolean(var, &fValue);

if (SUCCEEDED(hr))
{
    // fValue is now valid.
}
else
{
    // fValue is always FALSE.
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromboolean">InitVariantFromBoolean</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoboolean">PropVariantToBoolean</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttobooleanarray">VariantToBooleanArray</a>