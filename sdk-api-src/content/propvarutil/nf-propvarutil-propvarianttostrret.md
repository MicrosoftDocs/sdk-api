---
UID: NF:propvarutil.PropVariantToStrRet
title: PropVariantToStrRet function
author: windows-sdk-content
description: Extracts a string from a PROPVARIANT structure and places it into a STRRET structure.
old-location: properties\PropVariantToStrRet.htm
old-project: properties
ms.assetid: a1a33606-172d-4ee7-98c9-ffec8eed98bf
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PropVariantToStrRet, PropVariantToStrRet function [Windows Properties], _shell_PropVariantToStrRet, properties.PropVariantToStrRet, propvarutil/PropVariantToStrRet, shell.PropVariantToStrRet
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PropVariantToStrRet
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# PropVariantToStrRet function


## -description


Extracts a string from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure and places it into a <a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a> structure.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pstrret [out]

Type: <b><a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a>*</b>

Points to the <a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a> structure. When this function returns, the structure has been initialized to contain a copy of the extracted string.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function is used in applications that wish to convert a string value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure into a <a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a> structure. For instance, an application implementing <a href="https://msdn.microsoft.com/2164bbe6-e030-4a64-85db-9ee1cd3c136d">IShellFolder::GetDisplayNameOf</a> may find this function useful.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type VT_LPWSTR or VT_BSTR, this function extracts the string and places it into the <a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a> structure. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a string. If a conversion is not possible, <a href="https://msdn.microsoft.com/library/Bb776559(v=VS.85).aspx">PropVariantToString</a> will return a failure code. See <a href="https://msdn.microsoft.com/library/Bb776514(v=VS.85).aspx">PropVariantChangeType</a> for a list of possible conversions. Of note, VT_EMPTY is successfully converted to "".

In addition to the conversions provided by <a href="https://msdn.microsoft.com/library/Bb776514(v=VS.85).aspx">PropVariantChangeType</a>, the following special cases apply to <a href="https://msdn.microsoft.com/library/Bb776559(v=VS.85).aspx">PropVariantToString</a>. 
        

<ul>
<li>Vector-valued <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>s are converted to strings by separating each element with using "; ". For example, <a href="https://msdn.microsoft.com/library/Bb776559(v=VS.85).aspx">PropVariantToString</a> converts a vector of 3 integers, {3, 1, 4}, to the string "3; 1; 4". The semicolon is independent of the current locale.</li>
<li>VT_BLOB, VT_STREAM, VT_STREAMED_OBJECT, and VT_UNKNOWN values are converted to strings using an unsupported encoding. It is not possible to decode strings created in this way and the format may change in the future.</li>
</ul>
If the extraction is successful, the function will initialize uType member of the <a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a> structure with STRRET_WSTR and set the pOleStr member of that structure to point to an allocated copy of the string. The calling application is responsible for using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> or <a href="https://msdn.microsoft.com/03b0dffb-8ef7-41da-9773-81ed55275802">StrRetToStr</a> to free this string when it is no longer needed. 


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/library/Bb776559(v=VS.85).aspx">PropVariantToString</a> to access a string value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// IPropertyStore *ppropstore;

// Assume variable ppropstore is initialized and valid

PROPVARIANT propvar = {0};

HRESULT hr = ppropstore-&gt;GetValue(PKEY_FileName, &amp;propvar);

if (SUCCEEDED(hr))

{

    // PKEY_FileName is expected to produce a VT_LPWSTR or VT_EMPTY value.

    // PropVariantToStrRet will convert VT_EMPTY to "".

    // If this were an implementation of IShellFolder::GetDisplayNameOf, strName would be a parameter and the caller would free the memory associated with the STRRET

    STRRET strName;

    hr = PropVariantToStrRet(propvar, &amp;strName);

    if (SUCCEEDED(hr))

    {

        // strName is now valid

 

        if (strName.uType == STRRET_WSTR)

        {

            CoTaskMemFree(strName.pOleStr);

        }

    }

    else

    {

        // the extraction failed

    }

    PropVariantClear(&amp;propvar);

}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/Bb762305(v=VS.85).aspx">InitPropVariantFromString</a>



<a href="https://msdn.microsoft.com/library/Bb776514(v=VS.85).aspx">PropVariantChangeType</a>



<a href="https://msdn.microsoft.com/library/Bb776527(v=VS.85).aspx">PropVariantGetStringElem</a>



<a href="https://msdn.microsoft.com/library/Bb776559(v=VS.85).aspx">PropVariantToString</a>



<a href="https://msdn.microsoft.com/library/Bb776560(v=VS.85).aspx">PropVariantToStringAlloc</a>



<a href="https://msdn.microsoft.com/library/Bb776561(v=VS.85).aspx">PropVariantToStringVector</a>



<a href="https://msdn.microsoft.com/03b0dffb-8ef7-41da-9773-81ed55275802">StrRetToStr</a>



<a href="https://msdn.microsoft.com/library/Bb776622(v=VS.85).aspx">VariantToStrRet</a>
 

 

