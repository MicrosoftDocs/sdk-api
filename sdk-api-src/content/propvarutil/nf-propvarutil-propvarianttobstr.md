---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PropVariantToBSTR function


## -description


Extracts the BSTR property value of a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pbstrOut [out]

Type: <b><a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a>*</b>

Pointer to the extracted property value if one exists; otherwise, contains an empty string.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold a string value.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type <b>VT_BSTR</b> or VT_LPWSTR, this function extracts the string as a <b>BSTR</b> value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a string. If a conversion is not possible, <a href="shell.PropVariantToBSTR">PropVariantToBSTR</a> returns a failure code and sets <i>pbstrOut</i> to <b>NULL</b>. See <a href="shell.PropVariantChangeType">PropVariantChangeType</a> for a list of possible conversions.

<b>VT_EMPTY</b> is successfully converted to an allocated BSTR containing "".

The calling application is responsible for using <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to release the <b>BSTR</b> pointed to by <i>pbstrOut</i> when it is no longer needed.

In addition to the conversions provided by <a href="shell.PropVariantChangeType">PropVariantChangeType</a>, the following special cases apply to <a href="shell.PropVariantToBSTR">PropVariantToBSTR</a>.
                

<ul>
<li>Vector-valued <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANTs</a> are converted to strings by separating each element with using "; ". For example, <a href="shell.PropVariantToBSTR">PropVariantToBSTR</a> converts a vector of 3 integers, {3, 1, 4}, to the string "3; 1; 4". The semicolon is independent of the current locale.</li>
<li>VT_BLOB, VT_STREAM, VT_STREAMED_OBJECT, and VT_UNKNOWN values are converted to strings through an unsupported encoding. It is not possible to decode strings created in this way and the format may change in the future.</li>
</ul>

#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PropVariantToBSTR">PropVariantToBSTR</a> to access a string value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.

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




<a href="shell.InitPropVariantFromString">InitPropVariantFromString</a>



<a href="shell.PropVariantGetStringElem">PropVariantGetStringElem</a>



<a href="shell.PropVariantToString">PropVariantToString</a>



<a href="shell.PropVariantToStringWithDefault">PropVariantToStringWithDefault</a>
 

 

