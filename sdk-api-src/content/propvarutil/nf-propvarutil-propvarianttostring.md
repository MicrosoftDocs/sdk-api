---
UID: NF:propvarutil.PropVariantToString
title: PropVariantToString function (propvarutil.h)
description: Extracts a string value from a PROPVARIANT structure.
helpviewer_keywords: ["PropVariantToString","PropVariantToString function [Windows Properties]","properties.PropVariantToString","propvarutil/PropVariantToString","shell.PropVariantToString","shell_PropVariantToString"]
old-location: properties\PropVariantToString.htm
tech.root: properties
ms.assetid: d545dc12-a780-4d95-8660-13b3f65725f9
ms.date: 12/05/2018
ms.keywords: PropVariantToString, PropVariantToString function [Windows Properties], properties.PropVariantToString, propvarutil/PropVariantToString, shell.PropVariantToString, shell_PropVariantToString
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
 - PropVariantToString
 - propvarutil/PropVariantToString
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
 - PropVariantToString
---

# PropVariantToString function


## -description

Extracts a string value from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param psz [out]

Type: <b>PWSTR</b>

Points to a string buffer. When this function returns, the buffer is initialized with a <b>NULL</b> terminated Unicode string value.

### -param cch [in]

Type: <b>UINT</b>

Size of the buffer pointed to by <i>psz</i>, in characters.

## -returns

Type: <b>HRESULT</b>

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The value was extracted and the result buffer was <b>NULL</b> terminated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The copy operation failed due to insufficient buffer space. The destination buffer contains a truncated, null-terminated version of the intended result. In situations where truncation is acceptable, this may not necessarily be seen as a failure condition.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Some other error value</b></dt>
</dl>
</td>
<td width="60%">
The extraction failed for some other reason.

</td>
</tr>
</table>

## -remarks

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a string value. For instance, an application obtaining values from a property store can use this to safely extract a string value for string properties.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type VT_LPWSTR or <b>VT_BSTR</b>, this function extracts the string and places it into the provided buffer. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a string. If a conversion is not possible, <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostring">PropVariantToString</a> will return a failure code and set <i>psz</i> to '\0'. See <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a> for a list of possible conversions. Of note, <b>VT_EMPTY</b> is successfully converted to "".

In addition to the terminating <b>NULL</b>, at most <i>cch</i>-1 characters are written into the buffer pointed to by <i>psz</i>. If the value in the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> is longer than will fit into the buffer, a truncated <b>NULL</b> Terminated copy of the string is written to the buffer and this function returns <b>STRSAFE_E_INSUFFICIENT_BUFFER</b>. The resulting string will always be <b>NULL</b> terminated.

In addition to the conversions provided by <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a>, the following special cases apply to <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostring">PropVariantToString</a>. 
            

<ul>
<li>Vector-valued <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>s are converted to strings by separating each element with using "; ". For example, <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostring">PropVariantToString</a> converts a vector of 3 integers, {3, 1, 4}, to the string "3; 1; 4". The semicolon is independent of the current locale.</li>
<li>VT_BLOB, VT_STREAM, VT_STREAMED_OBJECT, and VT_UNKNOWN values are converted to strings using an unsupported encoding. It is not possible to decode strings created in this way and the format may change in the future.</li>
</ul>

#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostring">PropVariantToString</a> to access a string value in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// IPropertyStore *ppropstore;

// Assume variable ppropstore is initialized and valid

PROPVARIANT propvar = {0};

HRESULT hr = ppropstore->GetValue(PKEY_Title, &propvar);

if (SUCCEEDED(hr))

{

    // PKEY_Title is expected to produce a VT_LPWSTR or VT_EMPTY value.

    // PropVariantToString will convert VT_EMPTY to "".

    // The application decided that it only needs the first 127 characters of the title, so the buffer 

    // has size 128 to account for the terminating NULL.

    WCHAR szTitle[128];

    hr = PropVariantToString(propvar, szTitle, ARRAYSIZE(szTitle));

    if (SUCCEEDED(hr) || hr == STRSAFE_E_INSUFFICIENT_BUFFER)

    {

        // szTitle is now valid and contains up to 127 characters from propvar and a terminating NULL

    }

    else

    {

        // the extraction failed

    }

    PropVariantClear(&propvar);

}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromstring">InitPropVariantFromString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetstringelem">PropVariantGetStringElem</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttobstr">PropVariantToBSTR</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostringalloc">PropVariantToStringAlloc</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostringvector">PropVariantToStringVector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-varianttostring">VariantToString</a>