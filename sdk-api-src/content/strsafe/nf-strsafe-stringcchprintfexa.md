---
UID: NF:strsafe.StringCchPrintfExA
title: StringCchPrintfExA function
author: windows-sdk-content
description: Writes formatted data to the specified string.
old-location: menurc\stringcchprintfex.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\stringcchprintfex.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: STRSAFE_FILL_BEHIND_NULL, STRSAFE_FILL_ON_FAILURE, STRSAFE_IGNORE_NULLS, STRSAFE_NO_TRUNCATION, STRSAFE_NULL_ON_FAILURE, StringCchPrintfEx, StringCchPrintfEx function [Menus and Other Resources], StringCchPrintfExA, StringCchPrintfExW, _shell_StringCchPrintfEx, _shell_stringcchprintfex_cpp, menurc.stringcchprintfex, strsafe/StringCchPrintfEx, strsafe/StringCchPrintfExA, strsafe/StringCchPrintfExW, winui._shell_stringcchprintfex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: strsafe.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StringCchPrintfExW (Unicode) and StringCchPrintfExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AM_DVD_RENDERSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Strsafe.h
api_name:
 - StringCchPrintfEx
 - StringCchPrintfExA
 - StringCchPrintfExW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# StringCchPrintfExA function


## -description


Writes formatted data to the specified string. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer.

<b>StringCchPrintfEx</b> adds to the functionality of <a href="https://msdn.microsoft.com/9eaafe87-04da-4273-babb-b16d26bfdf70">StringCchPrintf</a> by returning a pointer to the end of the destination string as well as the number of characters left unused in that string. Flags may also be passed to the function for additional control.

<b>StringCchPrintfEx</b> is a replacement for the following functions:
<ul>
<li><a href="http://go.microsoft.com/fwlink/p/?linkid=192497">sprintf, swprintf, _stprintf</a></li>
<li>
<a href="https://msdn.microsoft.com/5f373cb3-8cb9-4516-8a18-8971bb430d42">wsprintf</a>
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


### -param cchDest [in]

Type: <b>size_t</b>

The size of the destination buffer, in characters. This value must be sufficiently large to accommodate the final formatted string plus 1 to account for the terminating null character. The maximum number of characters allowed is <b>STRSAFE_MAX_CCH</b>.


### -param ppszDestEnd [out, optional]

Type: <b>LPTSTR*</b>

The address of a pointer to the end of <i>pszDest</i>. If <i>ppszDestEnd</i> is non-<b>NULL</b> and any data is copied into the destination buffer, this points to the terminating null character at the end of the string.


### -param pcchRemaining [out, optional]

Type: <b>size_t*</b>

The number of unused characters in <i>pszDest</i>, including the terminating null character. If <i>pcchRemaining</i> is <b>NULL</b>, the count is not kept or returned.


### -param dwFlags [in]

Type: <b>DWORD</b>

One or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STRSAFE_FILL_BEHIND_NULL"></a><a id="strsafe_fill_behind_null"></a><dl>
<dt><b>STRSAFE_FILL_BEHIND_NULL</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
If the function succeeds, the low byte of <i>dwFlags</i> (0) is used to fill the uninitialized portion of <i>pszDest</i> following the terminating null character.

</td>
</tr>
<tr>
<td width="40%"><a id="STRSAFE_IGNORE_NULLS"></a><a id="strsafe_ignore_nulls"></a><dl>
<dt><b>STRSAFE_IGNORE_NULLS</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Treat <b>NULL</b> string pointers like empty strings (TEXT("")).

</td>
</tr>
<tr>
<td width="40%"><a id="STRSAFE_FILL_ON_FAILURE"></a><a id="strsafe_fill_on_failure"></a><dl>
<dt><b>STRSAFE_FILL_ON_FAILURE</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
If the function fails, the low byte of <i>dwFlags</i> (0) is used to fill the entire <i>pszDest</i> buffer, and the buffer is null-terminated. In the case of a <b>STRSAFE_E_INSUFFICIENT_BUFFER</b> failure, any truncated string returned is overwritten.

</td>
</tr>
<tr>
<td width="40%"><a id="STRSAFE_NULL_ON_FAILURE"></a><a id="strsafe_null_on_failure"></a><dl>
<dt><b>STRSAFE_NULL_ON_FAILURE</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
If the function fails, <i>pszDest</i> is set to an empty string (TEXT("")). In the case of a <b>STRSAFE_E_INSUFFICIENT_BUFFER</b> failure, any truncated string is overwritten.

</td>
</tr>
<tr>
<td width="40%"><a id="STRSAFE_NO_TRUNCATION"></a><a id="strsafe_no_truncation"></a><dl>
<dt><b>STRSAFE_NO_TRUNCATION</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
As in the case of <b>STRSAFE_NULL_ON_FAILURE</b>, if the function fails, <i>pszDest</i> is set to an empty string (TEXT("")). In the case of a <b>STRSAFE_E_INSUFFICIENT_BUFFER</b> failure, any truncated string is overwritten.

</td>
</tr>
</table>
 


### -param pszFormat [in]

Type: <b>LPCTSTR</b>

The format string. This string must be null-terminated. For more information, see <a href="https://msdn.microsoft.com/en-us/library/56e442dc.aspx">Format Specification Syntax</a>.


### -param param [in]

The Arguments to be inserted into the <i>pszFormat</i> string.


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
There was sufficient space for the result to be copied to <i>pszDest</i> without truncation and the buffer is null-terminated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>cchDest</i> is either 0 or larger than <b>STRSAFE_MAX_CCH</b>, or the destination buffer is already full.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The copy operation failed due to insufficient buffer space. Depending on the value of <i>dwFlags</i>, the destination buffer may contain a truncated, null-terminated version of the intended result. In situations where truncation is acceptable, this may not necessarily be seen as a failure condition.

</td>
</tr>
</table>
 

Note that this function returns an <b>HRESULT</b> value, unlike the functions that it replaces.




## -remarks



Compared to  the functions it replaces, <b>StringCchPrintfEx</b> provides additional processing for proper buffer handling in your code. Poor buffer handling is implicated in many security issues that involve buffer overruns. <b>StringCchPrintfEx</b>always null-terminates a nonzero-length destination buffer.

Behavior is undefined if the strings pointed to by <i>pszDest</i>, <i>pszFormat</i>, or any argument strings overlap.

Neither <i>pszFormat</i> nor <i>pszDest</i> should be <b>NULL</b> unless the <b>STRSAFE_IGNORE_NULLS</b> flag is specified, in which case both may be <b>NULL</b>. However, an error due to insufficient space may still be returned even though <b>NULL</b> values are ignored.

<b>StringCchPrintfEx</b> can be used in its generic form, or in its more specific forms. The data type of the string determines the form of this function that you should use.

<table class="clsStd">
<tr>
<th>String Data Type</th>
<th>String Literal</th>
<th>Function</th>
</tr>
<tr>
<td><b>char</b></td>
<td>"string"</td>
<td><b>StringCchPrintfExA</b></td>
</tr>
<tr>
<td><b>TCHAR</b></td>
<td>TEXT("string")</td>
<td><b>StringCchPrintfEx</b></td>
</tr>
<tr>
<td><b>WCHAR</b></td>
<td>L"string"</td>
<td><b>StringCchPrintfExW</b></td>
</tr>
</table>
 




## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/525e1fb5-9dfd-4ec2-a4af-9b9e198b6e17">StringCbPrintfEx</a>



<a href="https://msdn.microsoft.com/9eaafe87-04da-4273-babb-b16d26bfdf70">StringCchPrintf</a>



<a href="https://msdn.microsoft.com/07b4eb68-2b50-4c66-af1a-13cc57144e3a">StringCchVPrintfEx</a>
 

 

