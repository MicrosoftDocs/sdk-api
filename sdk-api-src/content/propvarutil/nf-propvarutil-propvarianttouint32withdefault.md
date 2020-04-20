---
UID: NF:propvarutil.PropVariantToUInt32WithDefault
title: PropVariantToUInt32WithDefault function (propvarutil.h)
description: Extracts a ULONG value from a PROPVARIANT structure. If no value exists, then a specified default value is returned.helpviewer_keywords: ["PropVariantToUInt32WithDefault","PropVariantToUInt32WithDefault function [Windows Properties]","properties.PropVariantToUInt32WithDefault","propvarutil/PropVariantToUInt32WithDefault","shell.PropVariantToUInt32WithDefault","shell_PropVariantToUInt32WithDefault"]
old-location: properties\PropVariantToUInt32WithDefault.htm
tech.root: properties
ms.assetid: 8ace8c3f-fea2-4b20-9e0b-3abfbd569b54
ms.date: 12/05/2018
ms.keywords: PropVariantToUInt32WithDefault, PropVariantToUInt32WithDefault function [Windows Properties], properties.PropVariantToUInt32WithDefault, propvarutil/PropVariantToUInt32WithDefault, shell.PropVariantToUInt32WithDefault, shell_PropVariantToUInt32WithDefault
f1_keywords:
- propvarutil/PropVariantToUInt32WithDefault
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Propsys.dll
api_name:
- PropVariantToUInt32WithDefault
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# PropVariantToUInt32WithDefault function


## -description


Extracts a <b>ULONG</b> value from a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure. If no value exists, then a specified default value is returned.


## -parameters




### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.


### -param ulDefault [in]

Type: <b>ULONG</b>

Specifies a default property value, for use where no value currently exists.


## -returns



Type: <b>ULONG</b>

Returns extracted <b>ULONG</b> value, or default.




## -remarks



This helper function is used in places where the calling application expects a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a <b>ULONG</b> value and would like to use a default value if it does not. For instance, an application obtaining values from a property store can use this to safely extract the <b>ULONG</b> value for <b>UInt32</b> properties.

If the source <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type <b>VT_UI4</b>, this helper function extracts the <b>ULONG</b> value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a <b>ULONG</b>. If the source <b>PROPVARIANT</b> has type <b>VT_EMPTY</b> or a conversion is not possible, then <a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint32withdefault">PropVariantToUInt32WithDefault</a> will return the default provided by <i>ulDefault</i>. See <a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a> for a list of possible conversions.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint32withdefault">PropVariantToUInt32WithDefault</a> to access a <b>ULONG</b> value in a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// IPropertyStore *ppropstore;
// Assume variable ppropstore is initialized and valid
PROPVARIANT propvar = {0};
HRESULT hr = ppropstore->GetValue(PKEY_Rating, &propvar);
if (SUCCEEDED(hr))
{
     // PKEY_Rating is expected to produce a VT_UI4 or VT_EMPTY value.
     // The application developer decided to treat VT_EMPTY or invalid values as 0
     ULONG uRating = PropVariantToUInt32WithDefault(propvar, 0);
     // uRating is now valid.
     PropVariantClear(&propvar);
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromuint32">InitPropVariantFromUInt32</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttouint32">PropVariantToUInt32</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-varianttouint32">VariantToUInt32</a>
 

 

