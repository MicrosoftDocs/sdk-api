---
UID: NF:propvarutil.PropVariantToBooleanWithDefault
title: PropVariantToBooleanWithDefault function (propvarutil.h)
description: Extracts the Boolean property value of a PROPVARIANT structure. If no value exists, then the specified default value is returned.
helpviewer_keywords: ["PropVariantToBooleanWithDefault","PropVariantToBooleanWithDefault function [Windows Properties]","properties.PropVariantToBooleanWithDefault","propvarutil/PropVariantToBooleanWithDefault","shell.PropVariantToBooleanWithDefault","shell_PropVariantToBooleanWithDefault"]
old-location: properties\PropVariantToBooleanWithDefault.htm
tech.root: properties
ms.assetid: 223767a7-a4de-4e7e-ad8b-2a6bdcea0a47
ms.date: 12/05/2018
ms.keywords: PropVariantToBooleanWithDefault, PropVariantToBooleanWithDefault function [Windows Properties], properties.PropVariantToBooleanWithDefault, propvarutil/PropVariantToBooleanWithDefault, shell.PropVariantToBooleanWithDefault, shell_PropVariantToBooleanWithDefault
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
 - PropVariantToBooleanWithDefault
 - propvarutil/PropVariantToBooleanWithDefault
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
 - PropVariantToBooleanWithDefault
---

# PropVariantToBooleanWithDefault function


## -description

Extracts the Boolean property value of a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure. If no value exists, then the specified default value is returned.

## -parameters

### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param fDefault [in]

Type: <b>BOOL</b>

Specifies the default property value, for use where no value currently exists.

## -returns

Type: <b>BOOL</b>

The extracted Boolean value or the default value.

## -remarks

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a Boolean value and would like to use a default value if it does not. For instance, an application that obtains values from a property store can use this to safely extract the Boolean value for Boolean properties.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type <b>VT_BOOL</b>, this helper function extracts the Boolean value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a Boolean. If the source <b>PROPVARIANT</b> has type <b>VT_EMPTY</b> or a conversion is not possible, then <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttobooleanwithdefault">PropVariantToBooleanWithDefault</a> returns the default provided by <i>fDefault</i>. See <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a> for a list of possible conversions.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttobooleanwithdefault">PropVariantToBooleanWithDefault</a> to access a Boolean value in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// IPropertyStore *ppropstore;
// Assume the variable ppropstore is initialized and valid.
PROPVARIANT propvar = {0};
HRESULT hr = ppropstore->GetValue(PKEY_IsRead, &propvar);

if (SUCCEEDED(hr))
{
     // PKEY_IsRead is expected to produce a VT_BOOL or VT_EMPTY value.
     // The application developer decided to treat VT_EMPTY or invalid values as TRUE
     BOOL fShared = PropVariantToBooleanWithDefault(propvar, TRUE);
     
     // fShared is now valid.
     PropVariantClear(&propvar);
}
```