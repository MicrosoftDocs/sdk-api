---
UID: NF:strsafe.StringCchVPrintfExW
title: StringCchVPrintfExW function (strsafe.h)
description: Writes formatted data to the specified string using a pointer to a list of arguments.helpviewer_keywords: ["STRSAFE_FILL_BEHIND_NULL","STRSAFE_FILL_ON_FAILURE","STRSAFE_IGNORE_NULLS","STRSAFE_NO_TRUNCATION","STRSAFE_NULL_ON_FAILURE","StringCchVPrintfEx","StringCchVPrintfEx function [Menus and Other Resources]","StringCchVPrintfExA","StringCchVPrintfExW","_shell_StringCchVPrintfEx","_shell_stringcchvprintfex_cpp","menurc.stringcchvprintfex","strsafe/StringCchVPrintfEx","strsafe/StringCchVPrintfExA","strsafe/StringCchVPrintfExW","winui._shell_stringcchvprintfex"]
old-location: menurc\stringcchvprintfex.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\stringcchvprintfex.htm
ms.date: 12/05/2018
ms.keywords: STRSAFE_FILL_BEHIND_NULL, STRSAFE_FILL_ON_FAILURE, STRSAFE_IGNORE_NULLS, STRSAFE_NO_TRUNCATION, STRSAFE_NULL_ON_FAILURE, StringCchVPrintfEx, StringCchVPrintfEx function [Menus and Other Resources], StringCchVPrintfExA, StringCchVPrintfExW, _shell_StringCchVPrintfEx, _shell_stringcchvprintfex_cpp, menurc.stringcchvprintfex, strsafe/StringCchVPrintfEx, strsafe/StringCchVPrintfExA, strsafe/StringCchVPrintfExW, winui._shell_stringcchvprintfex
f1_keywords:
- strsafe/StringCchVPrintfEx
dev_langs:
- c++
req.header: strsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StringCchVPrintfExW (Unicode) and StringCchVPrintfExA (ANSI)
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
- StringCchVPrintfEx
- StringCchVPrintfExA
- StringCchVPrintfExW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# StringCchVPrintfExW function


## -description


Writes formatted data to the specified string using a pointer to a list of arguments. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer.

<b>StringCchVPrintfEx</b> adds to the functionality of <a href="https://docs.microsoft.com/windows/desktop/api/strsafe/nf-strsafe-stringcchvprintfa">StringCchVPrintf</a> by returning a pointer to the end of the destination string as well as the number of characters left unused in that string. Flags may also be passed to the function for additional control.

<b>StringCchVPrintfEx</b> is a replacement for the following functions:
<ul>
<li><a href="https://msdn.microsoft.com/library/28d5ce15.aspx">vsprintf, vswprintf, _vstprintf</a></li>
<li><a href="https://msdn.microsoft.com/library/1kt27hek.aspx">vsnprintf, _vsnwprintf, _vsntprintf</a></li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-wvsprintfa">wvsprintf</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-wvnsprintfa">wvnsprintf</a>
</li>
</ul>

## -parameters




### -param pszDest [out]

Type: <b>LPTSTR</b>

The destination buffer, which receives the formatted, null-terminated string created from <i>pszFormat</i> and <i>argList</i>.


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

The format string. This string must be null-terminated. For more information, see <a href="https://docs.microsoft.com/cpp/c-runtime-library/format-specification-syntax-printf-and-wprintf-functions">Format Specification Syntax</a>.


### -param argList [in]

Type: <b>va_list</b>

The arguments to be inserted into the <i>pszFormat</i> string.


## -returns



Type: <b>HRESULT</b>

This function can return one of the following values. It is strongly recommended that you use the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-succeeded">SUCCEEDED</a> and <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-failed">FAILED</a> macros to test the return value of this function.

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



<b>StringCchVPrintfEx</b> provides additional processing for proper buffer handling in your code. Poor buffer handling is implicated in many security issues that involve buffer overruns. <b>StringCchVPrintfEx</b>always null-terminates a nonzero-length destination buffer.

For more information on va_lists, see the conventions defined in Stdarg.h.

Behavior is undefined if the strings pointed to by <i>pszDest</i>, <i>pszFormat</i>, or any argument strings overlap.

Neither <i>pszFormat</i> nor <i>pszDest</i> should be <b>NULL</b> unless the <b>STRSAFE_IGNORE_NULLS</b> flag is specified, in which case both may be <b>NULL</b>. However, an error due to insufficient space may still be returned even though <b>NULL</b> values are ignored.

<b>StringCchVPrintfEx</b> can be used in its generic form, or in its more specific forms. The data type of the string determines the form of this function that you should use, as shown in the following table.

<table class="clsStd">
<tr>
<th>String Data Type</th>
<th>String Literal</th>
<th>Function</th>
</tr>
<tr>
<td><b>char</b></td>
<td>"string"</td>
<td><b>StringCchVPrintfExA</b></td>
</tr>
<tr>
<td><b>TCHAR</b></td>
<td>TEXT("string")</td>
<td><b>StringCchVPrintfEx</b></td>
</tr>
<tr>
<td><b>WCHAR</b></td>
<td>L"string"</td>
<td><b>StringCchVPrintfExW</b></td>
</tr>
</table>
 




## -see-also




<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/strsafe/nf-strsafe-stringcbvprintfexa">StringCbVPrintfEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfexa">StringCchPrintfEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strsafe/nf-strsafe-stringcchvprintfa">StringCchVPrintf</a>
 

 

