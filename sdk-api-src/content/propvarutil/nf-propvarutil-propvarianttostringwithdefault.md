---
UID: NF:propvarutil.PropVariantToStringWithDefault
title: PropVariantToStringWithDefault function
author: windows-sdk-content
description: Extracts the string property value of a PROPVARIANT structure. If no value exists, then the specified default value is returned.
old-location: properties\PropVariantToStringWithDefault.htm
old-project: properties
ms.assetid: a5f50a32-033f-4bda-87db-c0a8515b6451
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PropVariantToStringWithDefault, PropVariantToStringWithDefault function [Windows Properties], _shell_PropVariantToStringWithDefault, properties.PropVariantToStringWithDefault, propvarutil/PropVariantToStringWithDefault, shell.PropVariantToStringWithDefault
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
 - PropVariantToStringWithDefault
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PropVariantToStringWithDefault function


## -description


Extracts the string property value of a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. If no value exists, then the specified default value is returned.


## -parameters




### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pszDefault [in]

Type: <b>LPCWSTR</b>

Pointer to a default Unicode string value, for use where no value currently exists. May be <b>NULL</b>.


## -returns



Type: <b>PCWSTR</b>

Returns string value or default, or the default.




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold a string value and would like to use a default value if it does not. For instance, an application obtaining values from a property store can use this to safely extract the string value for string properties.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type VT_LPWSTR or VT_BSTR, this helper function returns a pointer to the value in the source <b>PROPVARIANT</b>. If the source <b>PROPVARIANT</b> has type VT_EMPTY or a conversion is not possible, then <a href="shell.PropVariantToStringWithDefault">PropVariantToStringWithDefault</a> will return the default provided by <i>pszDefault</i>. 

Note that this function will return pointers to data supplied in the parameters. Thus the application must ensure that the data supplied to the parameters remains valid until the result is no longer in use.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PropVariantToStringWithDefault">PropVariantToStringWithDefault</a> to access a string value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.

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
     // The application developer decided to treat VT_EMPTY or invalid values as ""
     PCWSTR pszTitle = PropVariantToStringWithDefault(propvar, L"");
     // pszTitle is now valid.
     PropVariantClear(&amp;propvar);
}
// ... later in the program ...
hr = ppropstore-&gt;GetValue(PKEY_Comment, &amp;propvar);
if (SUCCEEDED(hr))
{
         // PKEY_Comment is expected to produce a VT_LPWSTR or VT_EMPTY value.
         // The application developer decided to treat VT_EMPTY as NULL
         PCWSTR pszComment = PropVariantToStringWithDefault(propvar, NULL);
         if (pszComment)
         {
                 // pszComment is valid
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



<a href="shell.PropVariantToStringAlloc">PropVariantToStringAlloc</a>



<a href="shell.VariantToString">VariantToString</a>
 

 

