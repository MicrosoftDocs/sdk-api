---
UID: NF:strsafe.StringCbPrintfW
title: StringCbPrintfW function
author: windows-sdk-content
description: Writes formatted data to the specified string.
old-location: menurc\stringcbprintf.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\stringcbprintf.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: StringCbPrintf, StringCbPrintf function [Menus and Other Resources], StringCbPrintfA, StringCbPrintfW, _shell_StringCbPrintf, _shell_stringcbprintf_cpp, menurc.stringcbprintf, strsafe/StringCbPrintf, strsafe/StringCbPrintfA, strsafe/StringCbPrintfW, winui._shell_stringcbprintf
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: strsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StringCbPrintfW (Unicode) and StringCbPrintfA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Strsafe.h
api_name:
 - StringCbPrintf
 - StringCbPrintfA
 - StringCbPrintfW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StringCbPrintfW function


## -description


Writes formatted data to the specified string. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer.

<b>StringCbPrintf</b> is a replacement for the following functions:
				
<ul>
<li><a href="http://go.microsoft.com/fwlink/p/?linkid=192497">sprintf, swprintf, _stprintf</a></li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms647550(v=VS.85).aspx">wsprintf</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1d2b472b-6b34-4867-897c-eca60921d414">wnsprintf</a>
</li>
<li><a href="http://go.microsoft.com/fwlink/p/?linkid=192507">_snprintf, _snwprintf, _sntprintf</a></li>
</ul>

## -parameters




### -param pszDest [out]

Type: <b>LPTSTR</b>

The destination buffer, which receives the formatted, null-terminated string created from <i>pszFormat</i> and its arguments.


### -param cbDest [in]

Type: <b>size_t</b>

The size of the destination buffer, in bytes. This value must be sufficiently large to accommodate the final formatted string plus the terminating null character. The maximum number of bytes allowed is <code>STRSAFE_MAX_CCH * sizeof(TCHAR)</code>.


### -param pszFormat [in]

Type: <b>LPCTSTR</b>

The format string. This string must be null-terminated. For more information, see <a href="https://msdn.microsoft.com/en-us/library/56e442dc.aspx">Format Specification Syntax</a>.


### -param arg1 [in]

The arguments to be inserted into the <i>pszFormat</i> string.


## -returns



Type: <b>HRESULT</b>

This function can return one of the following values. It is strongly recommended that you use the <a href="https://msdn.microsoft.com/7a258b0b-d214-46c5-be0a-6493cd14a0e5">SUCCEEDED</a> and <a href="https://msdn.microsoft.com/d9c4ff73-c255-4a82-b901-23bd5b41ee6c">FAILED</a> macros to test the return value of this function.

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
There was sufficient space for the result to be copied to <i>pszDest</i> without truncation, and the buffer is null-terminated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>cbDest</i> is either 0 or larger than <code>STRSAFE_MAX_CCH * sizeof(TCHAR)</code>.

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
</table>
 

Note that this function returns an <b>HRESULT</b> value, unlike the functions that it replaces.




## -remarks



Compared to  the functions it replaces, <b>StringCbPrintf</b> provides additional processing for proper buffer handling in your code. Poor buffer handling is implicated in many security issues that involve buffer overruns. <b>StringCbPrintf</b>always null-terminates a nonzero-length destination buffer.

Behavior is undefined if the strings pointed to by <i>pszDest</i>, <i>pszFormat</i>, or any argument strings overlap.

Neither <i>pszFormat</i> nor <i>pszDest</i> should be <b>NULL</b>. See <a href="https://msdn.microsoft.com/en-us/library/ms647513(v=VS.85).aspx">StringCbPrintfEx</a> if you require the handling of null string pointer values.

<b>StringCbPrintf</b> can be used in its generic form, or in its more specific forms. The data type of the string determines the form of this function that you should use.

<table class="clsStd">
<tr>
<th>String Data Type</th>
<th>String Literal</th>
<th>Function</th>
</tr>
<tr>
<td><b>char</b></td>
<td>"string"</td>
<td><b>StringCbPrintfA</b></td>
</tr>
<tr>
<td><b>TCHAR</b></td>
<td>TEXT("string")</td>
<td><b>StringCbPrintf</b></td>
</tr>
<tr>
<td><b>WCHAR</b></td>
<td>L"string"</td>
<td><b>StringCbPrintfW</b></td>
</tr>
</table>
 


#### Examples

The following example shows a basic use of <b>StringCbPrintf</b>, using four arguments.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>int const arraysize = 30;
TCHAR pszDest[arraysize]; 
size_t cbDest = arraysize * sizeof(TCHAR);

LPCTSTR pszFormat = TEXT("%s %d + %d = %d.");
TCHAR* pszTxt = TEXT("The answer is");

HRESULT hr = StringCbPrintf(pszDest, cbDest, pszFormat, pszTxt, 1, 2, 3);

// The resultant string at pszDest is "The answer is 1 + 2 = 3."</pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms647513(v=VS.85).aspx">StringCbPrintfEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647514(v=VS.85).aspx">StringCbVPrintf</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647541(v=VS.85).aspx">StringCchPrintf</a>
 

 

