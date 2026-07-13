---
UID: NF:propvarutil.PropVariantToBSTR
title: PropVariantToBSTR function (propvarutil.h)
description: Extracts the BSTR property value of a PROPVARIANT structure.
helpviewer_keywords: ["PropVariantToBSTR","PropVariantToBSTR function [Windows Properties]","_shell_PropVariantToBSTR","properties.PropVariantToBSTR","propvarutil/PropVariantToBSTR","shell.PropVariantToBSTR"]
old-location: properties\PropVariantToBSTR.htm
tech.root: properties
ms.assetid: a3aec16e-4fe3-4da4-a06d-f58412ac84b9
ms.date: 12/05/2018
ms.keywords: PropVariantToBSTR, PropVariantToBSTR function [Windows Properties], _shell_PropVariantToBSTR, properties.PropVariantToBSTR, propvarutil/PropVariantToBSTR, shell.PropVariantToBSTR
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
 - PropVariantToBSTR
 - propvarutil/PropVariantToBSTR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-propsys-l1-1-1.dll
 - Propsys.dll
 - Ext-MS-Win-shell-propsys-l1-1-0.dll
api_name:
 - PropVariantToBSTR
---

# PropVariantToBSTR function


## -description

Extracts the BSTR property value of a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param pbstrOut [out]

Type: <b><a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a>*</b>

Pointer to the extracted property value if one exists; otherwise, contains an empty string.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a string value.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type <b>VT_BSTR</b> or VT_LPWSTR, this function extracts the string as a <b>BSTR</b> value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a string. If a conversion is not possible, <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttobstr">PropVariantToBSTR</a> returns a failure code and sets <i>pbstrOut</i> to <b>NULL</b>. See <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a> for a list of possible conversions.

<b>VT_EMPTY</b> is successfully converted to an allocated BSTR containing "".

The calling application is responsible for using <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to release the <b>BSTR</b> pointed to by <i>pbstrOut</i> when it is no longer needed.

In addition to the conversions provided by <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a>, the following special cases apply to <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttobstr">PropVariantToBSTR</a>.
                

<ul>
<li>Vector-valued <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANTs</a> are converted to strings by separating each element with using "; ". For example, <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttobstr">PropVariantToBSTR</a> converts a vector of 3 integers, {3, 1, 4}, to the string "3; 1; 4". The semicolon is independent of the current locale.</li>
<li>VT_BLOB, VT_STREAM, VT_STREAMED_OBJECT, and VT_UNKNOWN values are converted to strings through an unsupported encoding. It is not possible to decode strings created in this way and the format may change in the future.</li>
</ul>

#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttobstr">PropVariantToBSTR</a> to access a string value in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// IPropertyStore *ppropstore;
// Assume the variable ppropstore is initialized and valid.
PROPVARIANT propvar = {0};

HRESULT hr = ppropstore->GetValue(PKEY_Title, &propvar);

if (SUCCEEDED(hr))
{
    // PKEY_Title is expected to produce a VT_LPWSTR or VT_EMPTY value.
    // PropVariantToBSTR will convert VT_EMPTY to "".
    BSTR bstrTitle;
    
    hr = PropVariantToBSTR(propvar, &bstrTitle);
    
    if (SUCCEEDED(hr))
    {
        // bstrTitle is now valid.
    }
    else
    {
        // bstrTitle is always NULL.
    }
    PropVariantClear(&propvar);
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromstring">InitPropVariantFromString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetstringelem">PropVariantGetStringElem</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostring">PropVariantToString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostringwithdefault">PropVariantToStringWithDefault</a>