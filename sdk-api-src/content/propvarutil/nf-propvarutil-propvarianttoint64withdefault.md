---
UID: NF:propvarutil.PropVariantToInt64WithDefault
title: PropVariantToInt64WithDefault function (propvarutil.h)
description: Extracts the Int64 property value of a PROPVARIANT structure. If no value exists, then specified default value is returned.
helpviewer_keywords: ["PropVariantToInt64WithDefault","PropVariantToInt64WithDefault function [Windows Properties]","properties.PropVariantToInt64WithDefault","propvarutil/PropVariantToInt64WithDefault","shell.PropVariantToInt64WithDefault","shell_PropVariantToInt64WithDefault"]
old-location: properties\PropVariantToInt64WithDefault.htm
tech.root: properties
ms.assetid: 6a051235-3e32-40d3-a17e-efc571592dae
ms.date: 12/05/2018
ms.keywords: PropVariantToInt64WithDefault, PropVariantToInt64WithDefault function [Windows Properties], properties.PropVariantToInt64WithDefault, propvarutil/PropVariantToInt64WithDefault, shell.PropVariantToInt64WithDefault, shell_PropVariantToInt64WithDefault
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
 - PropVariantToInt64WithDefault
 - propvarutil/PropVariantToInt64WithDefault
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
 - PropVariantToInt64WithDefault
---

# PropVariantToInt64WithDefault function


## -description

Extracts the <b>Int64</b> property value of a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure. If no value exists, then specified default value is returned.

## -parameters

### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param llDefault [in]

Type: <b>LONGLONG</b>

Specifies a default property value, for use where no value currently exists.

## -returns

Type: <b>LONGLONG</b>

Returns the extracted <b>LONGLONG</b> value, or default.

## -remarks

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a <b>LONGLONG</b> value and would like to use a default value if it does not. For instance, an application obtaining values from a property store can use this to safely extract the <b>LONGLONG</b> value for Int64 properties.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type <b>VT_I8</b>, this helper function extracts the <b>LONGLONG</b> value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a <b>LONGLONG</b>. If the source <b>PROPVARIANT</b> has type <b>VT_EMPTY</b> or a conversion is not possible, then <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint64withdefault">PropVariantToInt64WithDefault</a> will return the default provided by <i>llDefault</i>. See <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a> for a list of possible conversions.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint64withdefault">PropVariantToInt64WithDefault</a> to access a <b>LONGLONG</b> value in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid
// The application is expecting propvar to hold a VT_I8 value, but wishes to treat VT_EMPTY as -1.
LONGLONG llValue = PropVariantToInt64WithDefault(propvar, -1);
// llValue is valid
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromint64">InitPropVariantFromInt64</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint64">PropVariantToInt64</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttoint64">VariantToInt64</a>