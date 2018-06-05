---
UID: NF:propvarutil.PropVariantToStringAlloc
title: PropVariantToStringAlloc function
author: windows-sdk-content
description: Extracts a string property value from a PROPVARIANT structure.
old-location: properties\PropVariantToStringAlloc.htm
old-project: properties
ms.assetid: 5e47cc72-4179-4ebe-8700-87861146b3d7
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PropVariantToStringAlloc, PropVariantToStringAlloc function [Windows Properties], _shell_PropVariantToStringAlloc, properties.PropVariantToStringAlloc, propvarutil/PropVariantToStringAlloc, shell.PropVariantToStringAlloc
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	PropVariantToStringAlloc
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PropVariantToStringAlloc function


## -description


Extracts a string property value from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param ppszOut [out]

Type: <b>PWSTR*</b>

When this function returns, contains a pointer to the extracted property value if one exists.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold a string value.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type VT_LPWSTR or VT_BSTR, this function extracts the string into a newly allocated buffer. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a string. If a conversion is not possible, <a href="shell.PropVariantToStringAlloc">PropVariantToStringAlloc</a> will return a failure code and set <i>ppszOut</i> to <b>NULL</b>. See <a href="shell.PropVariantChangeType">PropVariantChangeType</a> for a list of possible conversions. Of note, <b>VT_EMPTY</b> is successfully converted to an allocated buffer containing "".

The calling application is responsible for using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> to release the string pointed to by <i>ppszOut</i> when it is no longer needed.

In addition to the conversions provided by <a href="shell.PropVariantChangeType">PropVariantChangeType</a>, the following special cases apply to <a href="shell.PropVariantToStringAlloc">PropVariantToStringAlloc</a>. 
                

<ul>
<li>Vector-valued PROPVARIANTs are converted to strings by separating each element with using "; ". For example, <a href="shell.PropVariantToStringAlloc">PropVariantToStringAlloc</a> converts a vector of 3 integers, {3, 1, 4}, to the string "3; 1; 4". The semicolon is independent of the current locale.</li>
<li>VT_BLOB, VT_STREAM, VT_STREAMED_OBJECT, and VT_UNKNOWN values are converted to strings using an unsupported encoding. It is not possible to decode strings created in this way and the format may change in the future.</li>
</ul>

#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// IPropertyStore *ppropstore;

// Assume variable ppropstore is initialized and valid

PROPVARIANT propvar = {0};

HRESULT hr = ppropstore-&gt;GetValue(PKEY_Title, &amp;propvar);

if (SUCCEEDED(hr))

{

    // PKEY_Title is expected to produce a VT_LPWSTR or VT_EMPTY value.

    // PropVariantToStringAlloc will convert VT_EMPTY to "".

    LPWSTR pszTitle;

    hr = PropVariantToString(propvar, &amp;pszTitle);

    if (SUCCEEDED(hr))

    {

        // pszTitle is now valid

    }

    else

    {

        // pszTitle is always NULL

    }

    PropVariantClear(&amp;propvar);

}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromString">InitPropVariantFromString</a>



<a href="shell.PropVariantChangeType">PropVariantChangeType</a>



<a href="shell.PropVariantToString">PropVariantToString</a>



<a href="shell.PropVariantToStringVector">PropVariantToStringVector</a>



<a href="shell.VariantToString">VariantToString</a>
 

 

