---
UID: NF:strsafe.StringCchGetsExA
title: StringCchGetsExA function (strsafe.h)
description: Gets one line of text from stdin, up to and including the newline character ('\n'). (StringCchGetsExA)
helpviewer_keywords: ["STRSAFE_FILL_BEHIND_NULL", "STRSAFE_FILL_ON_FAILURE", "STRSAFE_IGNORE_NULLS", "STRSAFE_NO_TRUNCATION", "STRSAFE_NULL_ON_FAILURE", "StringCchGetsExA", "strsafe/StringCchGetsExA"]
old-location: menurc\stringcchgetsex.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\stringcchgetsex.htm
ms.date: 12/05/2018
ms.keywords: STRSAFE_FILL_BEHIND_NULL, STRSAFE_FILL_ON_FAILURE, STRSAFE_IGNORE_NULLS, STRSAFE_NO_TRUNCATION, STRSAFE_NULL_ON_FAILURE, StringCchGetsEx, StringCchGetsEx function [Menus and Other Resources], StringCchGetsExA, StringCchGetsExW, _shell_StringCchGetsEx, _shell_stringcchgetsex_cpp, menurc.stringcchgetsex, strsafe/StringCchGetsEx, strsafe/StringCchGetsExA, strsafe/StringCchGetsExW, winui._shell_stringcchgetsex
req.header: strsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StringCchGetsExW (Unicode) and StringCchGetsExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StringCchGetsExA
 - strsafe/StringCchGetsExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Strsafe.h
api_name:
 - StringCchGetsEx
 - StringCchGetsExA
 - StringCchGetsExW
---

# StringCchGetsExA function


## -description

Gets one line of text from stdin, up to and including the newline character ('\n'). The line of text is copied to the destination buffer, and the newline character  is replaced with a null character. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer.
<div class="alert"><b>Note</b>  This function can only be used inline.</div><div> </div><b>StringCchGetsEx</b> adds to the functionality of <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchgetsa">StringCchGets</a> by returning a pointer to the end of the destination string as well as the number of characters left unused in that string. Flags may also be passed to the function for additional control.

<b>StringCchGetsEx</b> is a replacement for the following functions:
<ul>
<li><a href="/cpp/c-runtime-library/gets-getws">gets, _getws, _getts</a></li>
</ul><b>StringCchGetsEx</b> is not a replacement for <b>fgets</b>, which does not replace newline characters with a terminating null character.

## -parameters

### -param pszDest [out]

Type: <b>LPTSTR</b>

The destination buffer, which receives the copied characters.

### -param cchDest [in]

Type: <b>size_t</b>

The size of the destination buffer, in characters. This value must be at least 2 for the function to succeed. The maximum number of characters allowed, including the terminating null character, is <b>STRSAFE_MAX_CCH</b>. If <i>cchDest</i> is too small to hold the full line of text, the data is truncated.

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
Treat <b>NULL</b> string pointers like empty strings (TEXT("")). This flag is useful for emulating functions such as <a href="/windows/desktop/api/winbase/nf-winbase-lstrcpya">lstrcpy</a>.

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
As in the case of STRSAFE_NULL_ON_FAILURE, if the function fails, <i>pszDest</i> is set to an empty string (TEXT("")). In the case of a <b>STRSAFE_E_INSUFFICIENT_BUFFER</b> failure, any truncated string is overwritten.

</td>
</tr>
</table>

## -returns

Type: <b>HRESULT</b>

This function can return one of the following values. It is strongly recommended that you use the <a href="/windows/desktop/api/winerror/nf-winerror-succeeded">SUCCEEDED</a> and <a href="/windows/desktop/api/winerror/nf-winerror-failed">FAILED</a> macros to test the return value of this function.

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
Characters were read from stdin, were copied to the buffer at <i>pszDest</i>, and the buffer was null-terminated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_END_OF_FILE</b></dt>
</dl>
</td>
<td width="60%">
Indicates an error or end-of-file condition. Use <a href="/previous-versions/visualstudio/visual-studio-2010/xssktc6e(v=vs.100)">feof</a> or <a href="/previous-versions/visualstudio/visual-studio-2010/y2wc3w90(v=vs.100)">ferror</a> to determine which one has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>cchDest</i> is larger than the maximum allowed value or an invalid flag was passed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>cchDest</i> is 1 or less.

</td>
</tr>
</table>
 

Note that this function returns an <b>HRESULT</b> value, unlike the functions that it replaces.

## -remarks

<b>StringCchGetsEx</b> provides additional processing for proper buffer handling in your code. Poor buffer handling is implicated in many security issues that involve buffer overruns. <b>StringCchGetsEx</b> always null-terminates a nonzero-length destination buffer.

The value of <i>pszDest</i> should not be <b>NULL</b> unless the <b>STRSAFE_IGNORE_NULLS</b> flag is specified. However, an error due to insufficient space may still be returned even though <b>NULL</b> values are ignored.

<b>StringCchGetsEx</b> can be used in its generic form, or in its more specific forms. The data type of the string determines the form of this function that you should use, as shown in the following table.

<table class="clsStd">
<tr>
<th>String Data Type</th>
<th>String Literal</th>
<th>Function</th>
</tr>
<tr>
<td><b>char</b></td>
<td>"string"</td>
<td><b>StringCchGetsExA</b></td>
</tr>
<tr>
<td><b>TCHAR</b></td>
<td>TEXT("string")</td>
<td><b>StringCchGetsEx</b></td>
</tr>
<tr>
<td><b>WCHAR</b></td>
<td>L"string"</td>
<td><b>StringCchGetsExW</b></td>
</tr>
</table>
 





> [!NOTE]
> The strsafe.h header defines StringCchGetsEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbgetsexa">StringCbGetsEx</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchgetsa">StringCchGets</a>
