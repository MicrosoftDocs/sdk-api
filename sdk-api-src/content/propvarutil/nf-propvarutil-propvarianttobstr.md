---
UID: NF:propvarutil.PropVariantToBSTR
title: PropVariantToBSTR function
author: windows-sdk-content
description: Extracts the BSTR property value of a PROPVARIANT structure.
old-location: properties\PropVariantToBSTR.htm
tech.root: properties
ms.assetid: a3aec16e-4fe3-4da4-a06d-f58412ac84b9
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: PropVariantToBSTR, PropVariantToBSTR function [Windows Properties], _shell_PropVariantToBSTR, properties.PropVariantToBSTR, propvarutil/PropVariantToBSTR, shell.PropVariantToBSTR
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - Ext-MS-Win-shell-propsys-l1-1-0.dll
api_name:
 - PropVariantToBSTR
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# PropVariantToBSTR function


## -description


Extracts the BSTR property value of a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pbstrOut [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms221069(v=VS.85).aspx">BSTR</a>*</b>

Pointer to the extracted property value if one exists; otherwise, contains an empty string.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold a string value.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type <b>VT_BSTR</b> or VT_LPWSTR, this function extracts the string as a <b>BSTR</b> value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a string. If a conversion is not possible, <a href="https://msdn.microsoft.com/en-us/library/Bb776535(v=VS.85).aspx">PropVariantToBSTR</a> returns a failure code and sets <i>pbstrOut</i> to <b>NULL</b>. See <a href="https://msdn.microsoft.com/en-us/library/Bb776514(v=VS.85).aspx">PropVariantChangeType</a> for a list of possible conversions.

<b>VT_EMPTY</b> is successfully converted to an allocated BSTR containing "".

The calling application is responsible for using <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> to release the <b>BSTR</b> pointed to by <i>pbstrOut</i> when it is no longer needed.

In addition to the conversions provided by <a href="https://msdn.microsoft.com/en-us/library/Bb776514(v=VS.85).aspx">PropVariantChangeType</a>, the following special cases apply to <a href="https://msdn.microsoft.com/en-us/library/Bb776535(v=VS.85).aspx">PropVariantToBSTR</a>.
                

<ul>
<li>Vector-valued <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANTs</a> are converted to strings by separating each element with using "; ". For example, <a href="https://msdn.microsoft.com/en-us/library/Bb776535(v=VS.85).aspx">PropVariantToBSTR</a> converts a vector of 3 integers, {3, 1, 4}, to the string "3; 1; 4". The semicolon is independent of the current locale.</li>
<li>VT_BLOB, VT_STREAM, VT_STREAMED_OBJECT, and VT_UNKNOWN values are converted to strings through an unsupported encoding. It is not possible to decode strings created in this way and the format may change in the future.</li>
</ul>

#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb776535(v=VS.85).aspx">PropVariantToBSTR</a> to access a string value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// IPropertyStore *ppropstore;
// Assume the variable ppropstore is initialized and valid.
PROPVARIANT propvar = {0};

HRESULT hr = ppropstore-&gt;GetValue(PKEY_Title, &amp;propvar);

if (SUCCEEDED(hr))
{
    // PKEY_Title is expected to produce a VT_LPWSTR or VT_EMPTY value.
    // PropVariantToBSTR will convert VT_EMPTY to "".
    BSTR bstrTitle;
    
    hr = PropVariantToBSTR(propvar, &amp;bstrTitle);
    
    if (SUCCEEDED(hr))
    {
        // bstrTitle is now valid.
    }
    else
    {
        // bstrTitle is always NULL.
    }
    PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb762305(v=VS.85).aspx">InitPropVariantFromString</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776527(v=VS.85).aspx">PropVariantGetStringElem</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776559(v=VS.85).aspx">PropVariantToString</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776563(v=VS.85).aspx">PropVariantToStringWithDefault</a>
 

 

