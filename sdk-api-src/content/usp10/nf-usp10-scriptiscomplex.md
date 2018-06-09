---
UID: NF:usp10.ScriptIsComplex
title: ScriptIsComplex function
author: windows-sdk-content
description: Determines whether a Unicode string requires complex script processing.
old-location: intl\scriptiscomplex.htm
old-project: Intl
ms.assetid: 4f8c5494-1887-45f8-92f2-1a767a7d00da
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: SIC_ASCIIDIGIT, SIC_COMPLEX, SIC_NEUTRAL, ScriptIsComplex, ScriptIsComplex function [Internationalization for Windows Applications], _win32_ScriptIsComplex, intl.scriptiscomplex, usp10/ScriptIsComplex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: usp10.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: SCRIPT_JUSTIFY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - usp10.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptIsComplex
product: Windows
targetos: Windows
req.lib: Usp10.lib
req.dll: Usp10.dll
req.irql: 
req.product: Windows UI
---

# ScriptIsComplex function


## -description


Determines whether a Unicode string requires complex script processing.


## -parameters




### -param pwcInChars [in]

Pointer to the string to test.


### -param cInChars [in]

Length of the input string, in characters.


### -param dwFlags [in]

Flags specifying testing details. This parameter can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SIC_ASCIIDIGIT"></a><a id="sic_asciidigit"></a><dl>
<dt><b>SIC_ASCIIDIGIT</b></dt>
</dl>
</td>
<td width="60%">
Treat digits U+0030 to U+0039 as complex. The application sets this flag if the string is displayed with digit substitution enabled. If the application is following the user's National Language Support (NLS) settings using the <a href="https://msdn.microsoft.com/2c8c33d5-5cd6-4734-bf44-af7d4b578672">ScriptRecordDigitSubstitution</a> function, it can pass a <a href="https://msdn.microsoft.com/e96bf8b4-7456-4e16-a623-48320104dd66">SCRIPT_DIGITSUBSTITUTE</a> structure with the <b>DigitSubstitute</b> member set to SCRIPT_DIGITSUBSTITUTE_NONE.

</td>
</tr>
<tr>
<td width="40%"><a id="SIC_COMPLEX"></a><a id="sic_complex"></a><dl>
<dt><b>SIC_COMPLEX</b></dt>
</dl>
</td>
<td width="60%">
Treat complex script letters as complex. This flag should normally be set.

</td>
</tr>
<tr>
<td width="40%"><a id="SIC_NEUTRAL"></a><a id="sic_neutral"></a><dl>
<dt><b>SIC_NEUTRAL</b></dt>
</dl>
</td>
<td width="60%">
Treat neutrals as complex. The application sets this flag to display the string with right-to-left reading order.

</td>
</tr>
</table>
 


## -returns



Returns S_OK if the string requires complex script processing. The function returns S_FALSE if the string can be handled by standard API function calls, that is, it contains only characters laid out side-by-side and left-to-right. The function returns a nonzero HRESULT value if it does not succeed.




## -remarks



See <a href="https://msdn.microsoft.com/e1adc567-0445-4deb-8634-25653f82127c">Displaying Text with Uniscribe</a> for a discussion of the context in which this function is normally called.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/e1adc567-0445-4deb-8634-25653f82127c">Displaying Text with Uniscribe</a>



<a href="https://msdn.microsoft.com/e96bf8b4-7456-4e16-a623-48320104dd66">SCRIPT_DIGITSUBSTITUTE</a>



<a href="https://msdn.microsoft.com/2c8c33d5-5cd6-4734-bf44-af7d4b578672">ScriptRecordDigitSubstitution</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/876e36f5-a91c-490b-87bd-b7cb4993f8c4">Uniscribe Functions</a>
 

 

