---
UID: NF:propvarutil.InitPropVariantFromStringAsVector
title: InitPropVariantFromStringAsVector function
author: windows-sdk-content
description: Initializes a PROPVARIANT structure from a specified string. The string is parsed as a semi-colon delimited list (for example:\_&#0034;A;B;C&#0034;).
old-location: properties\InitPropVariantFromStringAsVector.htm
old-project: properties
ms.assetid: fc48f2e0-ce4a-4f48-a624-202def4bcff0
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: InitPropVariantFromStringAsVector, InitPropVariantFromStringAsVector function [Windows Properties], properties.InitPropVariantFromStringAsVector, propvarutil/InitPropVariantFromStringAsVector, shell.InitPropVariantFromStringAsVector, shell_InitPropVariantFromStringAsVector
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
 - InitPropVariantFromStringAsVector
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# InitPropVariantFromStringAsVector function


## -description


Initializes a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure from a specified string. The string is parsed as a semi-colon delimited list (for example: "A;B;C").


## -parameters




### -param psz [in]

Type: <b>PCWSTR</b>

Pointer to a buffer that contains the source Unicode string.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_VECTOR | VT_LPWSTR propvariant. It parses the source string as a semicolon list of values. The string "a; b; c" creates a vector with three values. Leading and trailing whitespace are removed, and empty values are omitted.

If <i>psz</i> is <b>NULL</b> or contains no values, the <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure is initialized as VT_EMPTY.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitPropVariantFromStringAsVector">InitPropVariantFromStringAsVector</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>PROPVARIANT propvar;
HRESULT hr = InitPropVariantFromStringAsVector(L"a; b; c", &amp;propvar);

if (SUCCEEDED(hr))
{
    // propvar now has type VT_VECTOR | VT_LPWSTR and contains {"a", "b", "c"}.
    PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromString">InitPropVariantFromString</a>



<a href="shell.InitPropVariantFromStringVector">InitPropVariantFromStringVector</a>



<a href="shell.InitVariantFromStringArray">InitVariantFromStringArray</a>



<a href="shell.PropVariantToStringVector">PropVariantToStringVector</a>
 

 

