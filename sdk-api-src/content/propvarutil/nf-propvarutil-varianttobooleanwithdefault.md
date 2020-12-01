---
UID: NF:propvarutil.VariantToBooleanWithDefault
title: VariantToBooleanWithDefault function (propvarutil.h)
description: Extracts a BOOL value from a VARIANT structure. If no value exists, then the specified default value is returned.
helpviewer_keywords: ["VariantToBooleanWithDefault","VariantToBooleanWithDefault function [Windows Properties]","_shell_VariantToBooleanWithDefault","properties.VariantToBooleanWithDefault","propvarutil/VariantToBooleanWithDefault","shell.VariantToBooleanWithDefault"]
old-location: properties\VariantToBooleanWithDefault.htm
tech.root: properties
ms.assetid: 523c6e75-a51c-4ef7-928c-0d228ab0d337
ms.date: 12/05/2018
ms.keywords: VariantToBooleanWithDefault, VariantToBooleanWithDefault function [Windows Properties], _shell_VariantToBooleanWithDefault, properties.VariantToBooleanWithDefault, propvarutil/VariantToBooleanWithDefault, shell.VariantToBooleanWithDefault
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
 - VariantToBooleanWithDefault
 - propvarutil/VariantToBooleanWithDefault
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
 - VariantToBooleanWithDefault
---

# VariantToBooleanWithDefault function


## -description

Extracts a <b>BOOL</b> value from a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure. If no value exists, then the specified default value is returned.

## -parameters

### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.

### -param fDefault [in]

Type: <b>BOOL</b>

The default value for use where no extractable value exists.

## -returns

Type: <b>BOOL</b>

Returns the extracted <b>BOOL</b> value; otherwise, the default value specified in <i>fDefault</i>.

## -remarks

This helper function is used when the calling application expects a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> to hold a <b>BOOL</b> value and wants to use a default value if it does not.

If the source <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> is of type VT_BOOL, this helper extracts the <b>BOOL</b> value.

If the source <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> is not of type VT_BOOL, the function attempts to convert the value in the <b>VARIANT</b> into a <b>BOOL</b>.

If the source <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> is of type VT_EMPTY or a conversion is not possible, then <a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttobooleanwithdefault">VariantToBooleanWithDefault</a> returns the default value provided by <i>fDefault</i>. See <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a> for a list of possible conversions.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttobooleanwithdefault">VariantToBooleanWithDefault</a> to access a <b>BOOL</b> value stored in a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.


```cpp
// VARIANT var;
// Assume variable var is initialized and valid.  
// The application expects var to hold a BOOL value.
// The application treats VT_EMPTY as FALSE.

BOOL fValue = VariantToBooleanWithDefault(var, FALSE);

// fValue is now valid.
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromboolean">InitVariantFromBoolean</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoboolean">PropVariantToBoolean</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttoboolean">VariantToBoolean</a>