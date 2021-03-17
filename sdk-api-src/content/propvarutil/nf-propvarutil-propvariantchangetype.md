---
UID: NF:propvarutil.PropVariantChangeType
title: PropVariantChangeType function (propvarutil.h)
description: Coerces a value stored as a PROPVARIANT structure to an equivalent value of a different variant type.
helpviewer_keywords: ["PropVariantChangeType","PropVariantChangeType function [Windows Properties]","_shell_PropVariantChangeType","properties.PropVariantChangeType","propvarutil/PropVariantChangeType","shell.PropVariantChangeType"]
old-location: properties\PropVariantChangeType.htm
tech.root: properties
ms.assetid: cb64ae1d-7dcf-4e73-b6ab-18fc9f91192d
ms.date: 12/05/2018
ms.keywords: PropVariantChangeType, PropVariantChangeType function [Windows Properties], _shell_PropVariantChangeType, properties.PropVariantChangeType, propvarutil/PropVariantChangeType, shell.PropVariantChangeType
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
 - PropVariantChangeType
 - propvarutil/PropVariantChangeType
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
 - PropVariantChangeType
---

# PropVariantChangeType function


## -description

Coerces a value stored as a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure to an equivalent value of a different variant type.

## -parameters

### -param ppropvarDest [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

A pointer to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure that, when this function returns successfully, receives the coerced value and its new type.

### -param propvarSrc [in]

Type: <b>REFPROPVARIANT</b>

A reference to the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure that contains the value expressed as its original type.

### -param flags [in]

Type: <b>PROPVAR_CHANGE_FLAGS</b>

Reserved, must be 0.

### -param vt [in]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ms221127(v=vs.85)">VARTYPE</a></b>

Specifies the new type for the value. See the tables below for recognized type names.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, or a standard COM error value otherwise. If the requested coercion is not possible, an error is returned.

## -remarks

Note that the source and destination <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structures must be separate structures. You cannot overwrite the source <b>PROPVARIANT</b> data with the new destination data; attempting to do so will result in an error.


<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a> converts values between the following types as follows. Numbers refer to conditions explained after the tables.




<table class="clsStd">
<tr>
<th></th>
<th>VT_LPWSTR</th>
<th>VT_BSTR</th>
<th>VT_BOOL</th>
<th>VT_FILETIME</th>
<th>VT_DATE</th>
<th>VT_CLSID</th>
</tr>
<tr>
<th>VT_LPWSTR</th>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes (2)</td>
<td>Yes (2)</td>
<td>Yes</td>
</tr>
<tr>
<th>VT_BSTR</th>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes (2)</td>
<td>Yes (2)</td>
<td>Yes</td>
</tr>
<tr>
<th>VT_BOOL</th>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
<td>No</td>
<td>No</td>
</tr>
<tr>
<th>VT_I2</th>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
<td>No</td>
<td>No</td>
</tr>
<tr>
<th>VT_I4</th>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
<td>No</td>
<td>No</td>
</tr>
<tr>
<th>VT_I8</th>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
<td>No</td>
<td>No</td>
</tr>
<tr>
<th>VT_UI2</th>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
<td>No</td>
<td>No</td>
</tr>
<tr>
<th>VT_UI4</th>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
<td>No</td>
<td>No</td>
</tr>
<tr>
<th>VT_UI8</th>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
<td>No</td>
<td>No</td>
</tr>
<tr>
<th>VT_R8</th>
<td>Yes (3)</td>
<td>Yes (3)</td>
<td>Yes</td>
<td>No</td>
<td>No</td>
<td>No</td>
</tr>
<tr>
<th>VT_FILETIME</th>
<td>Yes (2)</td>
<td>Yes (2)</td>
<td>No</td>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
</tr>
<tr>
<th>VT_DATE</th>
<td>Yes (2)</td>
<td>Yes (2)</td>
<td>No</td>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
</tr>
<tr>
<th>VT_CLSID</th>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>Yes</td>
</tr>
</table>
 




<table class="clsStd">
<tr>
<th></th>
<th>VT_I2</th>
<th>VT_I4</th>
<th>VT_I8</th>
<th>VT_UI2</th>
<th>VT_UI4</th>
<th>VT_UI8</th>
<th>VT_R8</th>
</tr>
<tr>
<th>VT_LPWSTR</th>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes (3)</td>
</tr>
<tr>
<th>VT_BSTR</th>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes (3)</td>
</tr>
<tr>
<th>VT_BOOL</th>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
</tr>
<tr>
<th>VT_I2</th>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes (1)</td>
<td>Yes (1)</td>
<td>Yes (1)</td>
<td>Yes (1)</td>
</tr>
<tr>
<th>VT_I4</th>
<td>Yes (1)</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes (1)</td>
<td>Yes (1)</td>
<td>Yes (1)</td>
<td>Yes (1)</td>
</tr>
<tr>
<th>VT_I8</th>
<td>Yes (1)</td>
<td>Yes (1)</td>
<td>Yes</td>
<td>Yes (1)</td>
<td>Yes (1)</td>
<td>Yes (1)</td>
<td>Yes (1)</td>
</tr>
<tr>
<th>VT_UI2</th>
<td>Yes (1)</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes (1)</td>
</tr>
<tr>
<th>VT_UI4</th>
<td>Yes (1)</td>
<td>Yes (1)</td>
<td>Yes</td>
<td>Yes (1)</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes (1)</td>
</tr>
<tr>
<th>VT_UI8</th>
<td>Yes (1)</td>
<td>Yes (1)</td>
<td>Yes (1)</td>
<td>Yes (1)</td>
<td>Yes (1)</td>
<td>Yes</td>
<td>Yes (1)</td>
</tr>
<tr>
<th>VT_R8</th>
<td>Yes (1)</td>
<td>Yes (1)</td>
<td>Yes (1)</td>
<td>Yes (1)</td>
<td>Yes (1)</td>
<td>Yes (1)</td>
<td>Yes</td>
</tr>
<tr>
<th>VT_FILETIME</th>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
</tr>
<tr>
<th>VT_DATE</th>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
</tr>
<tr>
<th>VT_CLSID</th>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
</tr>
</table>
 



<h3><a id="Conditions"></a><a id="conditions"></a><a id="CONDITIONS"></a>Conditions</h3>
<ol>
<li>When converting between numeric types, out-of-range conversions fail. For instance, a negative signed value to an unsigned type, or a 4-byte unsigned value larger than 65535 to a 2-byte unsigned type.</li>
<li>When converting between strings and dates, a canonical string form is used rather than a localized or "human-readable" representation. The format is "yyyy/mm/dd:hh:mm:ss.fff" (year, month, date, hours, minutes, seconds, milliseconds). Note that this is less precision than is supported by the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> type, but it should be sufficient for most purposes.</li>
<li>When converting between floating point numbers and strings, the current locale's decimal separator is used. Note that this might cause problems when these values are saved in files that are moved between different locales.</li>
</ol>
<div class="alert"><b>Note</b>  Additional types might be supported in the future.</div>
<div> </div>
Converting between vectors (<b>VT_VECTOR</b>) and arrays (<b>VT_ARRAY</b>) is supported in some cases. When it is supported, the count of elements must be the same in each. A single-valued vector can be converted to a non-vector value, but a multi-valued vector cannot be converted to a non-vector type.

Coercion between types is performed without respect to property-specific information. Property-specific coercions should be performed using <a href="/windows/desktop/api/propsys/nf-propsys-pscoercetocanonicalvalue">PSCoerceToCanonicalValue</a>. Additionally, if the string form of a value is needed for UI purposes, <a href="/windows/desktop/api/propsys/nf-propsys-psformatfordisplay">PSFormatForDisplay</a> should be used to format the value according to locale- and property-specific information rather than using <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a> to coerce the value to a string.


#### Examples

The following code example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a> to initialize a <b>VT_FILETIME</b> value from a string.


```cpp
PROPVARIANT propvarString = {0};
                    
HRESULT hr = InitPropVariantFromString(L"2007/01/30:12:00:00.000", &propvarString);
if (SUCCEEDED(hr))
{
    PROPVARIANT propvarFiletime = {0};

    hr = PropVariantChangeType(&propvarFiletime, propvarString, 0, VT_FILETIME);
    if (SUCCEEDED(hr))
    {
        // propvarFiletime now contains the FILETIME representation 
        // of 1/30/2007 12:00 PM
        PropVariantClear(&propvarFiletime);
    }
    PropVariantClear(&propvarString);
}
```