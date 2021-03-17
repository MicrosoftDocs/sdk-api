---
UID: NF:propvarutil.PropVariantToUInt64WithDefault
title: PropVariantToUInt64WithDefault function (propvarutil.h)
description: Extracts ULONGLONG value from a PROPVARIANT structure. If no value exists, then the specified default value is returned.
helpviewer_keywords: ["PropVariantToUInt64WithDefault","PropVariantToUInt64WithDefault function [Windows Properties]","properties.PropVariantToUInt64WithDefault","propvarutil/PropVariantToUInt64WithDefault","shell.PropVariantToUInt64WithDefault","shell_PropVariantToUInt64WithDefault"]
old-location: properties\PropVariantToUInt64WithDefault.htm
tech.root: properties
ms.assetid: 8ca0e25e-6a3f-41ff-9a4a-7cca9a02d07c
ms.date: 12/05/2018
ms.keywords: PropVariantToUInt64WithDefault, PropVariantToUInt64WithDefault function [Windows Properties], properties.PropVariantToUInt64WithDefault, propvarutil/PropVariantToUInt64WithDefault, shell.PropVariantToUInt64WithDefault, shell_PropVariantToUInt64WithDefault
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
 - PropVariantToUInt64WithDefault
 - propvarutil/PropVariantToUInt64WithDefault
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
 - PropVariantToUInt64WithDefault
---

# PropVariantToUInt64WithDefault function


## -description

Extracts <b>ULONGLONG</b> value from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure. If no value exists, then the specified default value is returned.

## -parameters

### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param ullDefault [in]

Type: <b>ULONGLONG</b>

Specifies a default property value, for use where no value currently exists.

## -returns

Type: <b>ULONGLONG</b>

Returns the extracted unsigned <b>LONGLONG</b> value, or a default.

## -remarks

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a <b>ULONGLONG</b> value and would like to use a default value if it does not. For instance, an application obtaining values from a property store can use this to safely extract the <b>ULONGLONG</b> value for <b>UInt64</b> properties.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type <b>VT_UI8</b>, this helper function extracts the <b>ULONGLONG</b> value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a <b>ULONGLONG</b>. If the source <b>PROPVARIANT</b> has type <b>VT_EMPTY</b> or a conversion is not possible, then <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint64withdefault">PropVariantToUInt64WithDefault</a> will return the default provided by <i>ullDefault</i>. See <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a> for a list of possible conversions.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint64withdefault">PropVariantToUInt64WithDefault</a> to access a <b>ULONGLONG</b> value in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// IPropertyStore *ppropstore;
// Assume variable ppropstore is initialized and valid
PROPVARIANT propvar = {0};
HRESULT hr = ppropstore->GetValue(PKEY_Size, &propvar);
if (SUCCEEDED(hr))
{
     // PKEY_Size is expected to produce a VT_UI8 or VT_EMPTY value.
     // The application developer decided to treat VT_EMPTY or invalid values as 0
     ULONGLONG ullSize = PropVariantToUInt64WithDefault(propvar, 0);
     // ullSize is now valid.
     PropVariantClear(&propvar);
}
```