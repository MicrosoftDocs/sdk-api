---
UID: NF:propvarutil.InitPropVariantFromString
title: InitPropVariantFromString function
author: windows-sdk-content
description: Initializes a PROPVARIANT structure based on a specified string.
old-location: properties\InitPropVariantFromString.htm
old-project: properties
ms.assetid: eeb1002c-d06b-4f7f-b850-4c33f6e0d7aa
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: InitPropVariantFromString, InitPropVariantFromString function [Windows Properties], properties.InitPropVariantFromString, propvarutil/InitPropVariantFromString, shell.InitPropVariantFromString, shell_InitPropVariantFromString
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
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Propvarutil.h
api_name:
-	InitPropVariantFromString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# InitPropVariantFromString function


## -description


Initializes a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure based on a specified string.


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



This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitPropVariantFromString">InitPropVariantFromString</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>PROPVARIANT propvar;
HRESULT hr = InitPropVariantFromString(L"Hello World", &amp;propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_LPWSTR.
    PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromStringAsVector">InitPropVariantFromStringAsVector</a>



<a href="shell.InitPropVariantFromStringVector">InitPropVariantFromStringVector</a>



<a href="shell.InitVariantFromString">InitVariantFromString</a>



<a href="shell.PropVariantToString">PropVariantToString</a>



<a href="shell.PropVariantToStringWithDefault">PropVariantToStringWithDefault</a>
 

 

