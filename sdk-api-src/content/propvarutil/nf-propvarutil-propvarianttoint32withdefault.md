---
UID: NF:propvarutil.PropVariantToInt32WithDefault
title: PropVariantToInt32WithDefault function (propvarutil.h)
description: Extracts an Int32 value from a PROPVARIANT structure. If no value currently exists, then the specified default value is returned.
helpviewer_keywords: ["PropVariantToInt32WithDefault","PropVariantToInt32WithDefault function [Windows Properties]","properties.PropVariantToInt32WithDefault","propvarutil/PropVariantToInt32WithDefault","shell.PropVariantToInt32WithDefault","shell_PropVariantToInt32WithDefault"]
old-location: properties\PropVariantToInt32WithDefault.htm
tech.root: properties
ms.assetid: 1d014cad-a9a5-4a58-855e-21c6d3ba6dcd
ms.date: 12/05/2018
ms.keywords: PropVariantToInt32WithDefault, PropVariantToInt32WithDefault function [Windows Properties], properties.PropVariantToInt32WithDefault, propvarutil/PropVariantToInt32WithDefault, shell.PropVariantToInt32WithDefault, shell_PropVariantToInt32WithDefault
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
 - PropVariantToInt32WithDefault
 - propvarutil/PropVariantToInt32WithDefault
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
 - PropVariantToInt32WithDefault
---

# PropVariantToInt32WithDefault function


## -description

Extracts an <b>Int32</b> value from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure. If no value currently exists, then the specified default value is returned.

## -parameters

### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param lDefault [in]

Type: <b>LONG</b>

Specifies a default property value, for use where no value currently exists.

## -returns

Type: <b>LONG</b>

Returns extracted <b>LONG</b> value, or default.

## -remarks

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a <b>LONG</b> value and would like to use a default value if it does not. For instance, an application obtaining values from a property store can use this to safely extract the <b>LONG</b> value for <b>Int32</b> properties.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type <b>VT_I4</b>, this helper function extracts the <b>LONG</b> value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a <b>LONG</b>. If the source <b>PROPVARIANT</b> has type <b>VT_EMPTY</b> or a conversion is not possible, then <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint32withdefault">PropVariantToInt32WithDefault</a> will return the default provided by <i>lDefault</i>. See <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a> for a list of possible conversions.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint32withdefault">PropVariantToInt32WithDefault</a> to access a <b>LONG</b> value in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// IPropertyStore *ppropstore;
// Assume variable ppropstore is initialized and valid
PROPVARIANT propvar = {0};
HRESULT hr = ppropstore->GetValue(PKEY_FlagStatus, &propvar);
if (SUCCEEDED(hr))
{
     // PKEY_FlagStatus is expected to produce a VT_I4 or VT_EMPTY value.
     // The application developer decided to treat VT_EMPTY or invalid values as 0
     LONG iStatus = PropVariantToInt32WithDefault(propvar, 0);
     // iStatus is now valid.
     PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromint32">InitPropVariantFromInt32</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint32">PropVariantToInt32</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttoint32">VariantToInt32</a>