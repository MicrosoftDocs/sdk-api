---
UID: NF:strsafe.StringCbCatNExA
title: StringCbCatNExA function (strsafe.h)
description: Concatenates the specified number of bytes from one string to another string. (StringCbCatNExA)
helpviewer_keywords: ["STRSAFE_FILL_BEHIND_NULL","STRSAFE_FILL_ON_FAILURE","STRSAFE_IGNORE_NULLS","STRSAFE_NO_TRUNCATION","STRSAFE_NULL_ON_FAILURE","StringCbCatNEx","StringCbCatNEx function [Menus and Other Resources]","StringCbCatNExA","StringCbCatNExW","_shell_StringCbCatNEx","_shell_stringcbcatnex_cpp","menurc.stringcbcatnex","strsafe/StringCbCatNEx","strsafe/StringCbCatNExA","strsafe/StringCbCatNExW","winui._shell_stringcbcatnex"]
old-location: menurc\stringcbcatnex.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\stringcbcatnex.htm
ms.date: 12/05/2018
ms.keywords: STRSAFE_FILL_BEHIND_NULL, STRSAFE_FILL_ON_FAILURE, STRSAFE_IGNORE_NULLS, STRSAFE_NO_TRUNCATION, STRSAFE_NULL_ON_FAILURE, StringCbCatNEx, StringCbCatNEx function [Menus and Other Resources], StringCbCatNExA, StringCbCatNExW, _shell_StringCbCatNEx, _shell_stringcbcatnex_cpp, menurc.stringcbcatnex, strsafe/StringCbCatNEx, strsafe/StringCbCatNExA, strsafe/StringCbCatNExW, winui._shell_stringcbcatnex
req.header: strsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StringCbCatNExW (Unicode) and StringCbCatNExA (ANSI)
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
 - StringCbCatNExA
 - strsafe/StringCbCatNExA
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
 - StringCbCatNEx
 - StringCbCatNExA
 - StringCbCatNExW
---

# StringCbCatNExA function


## -description

Concatenates the specified number of bytes from one  string to another string. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer.

<b>StringCbCatNEx</b> is a replacement for the following functions:
<ul>
<li><a href="/cpp/c-runtime-library/reference/strncat-strncat-l-wcsncat-wcsncat-l-mbsncat-mbsncat-l">strncat</a></li>
<li>
<a href="/windows/desktop/api/shlwapi/nf-shlwapi-strncata">StrNCat</a>
</li>
</ul><b>StringCbCatNEx</b> adds to the functionality of <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcatna">StringCbCatN</a> by returning a pointer to the end of the destination string as well as the number of bytes left unused in that string. Flags may also be passed to the function for additional control.

## -parameters

### -param pszDest [in, out]

Type: <b>LPTSTR</b>

The destination buffer, which contains the string that is to be concatenated with <i>pszSrc</i>, and will receive the entire resultant string. The string at <i>pszSrc</i> is added to the end of the string at <i>pszDest</i>.

### -param cbDest [in]

Type: <b>size_t</b>

The size of the destination buffer, in bytes. This value must consider the length of <i>pszSrc</i> plus the length of <i>pszDest</i> plus the bytes used for the terminating null character. The maximum number of bytes allowed is <code>STRSAFE_MAX_CCH * sizeof(TCHAR)</code>.

### -param pszSrc [in]

Type: <b>LPCTSTR</b>

The source string that is to be concatenated to the end of <i>pszDest</i>. This string must be null-terminated.

### -param cbToAppend [in]

Type: <b>size_t</b>

The maximum number of bytes to append to <i>pszDest</i>.

### -param ppszDestEnd [out, optional]

Type: <b>LPTSTR*</b>

The address of a pointer to the end of <i>pszDest</i>. If <i>ppszDestEnd</i> is non-<b>NULL</b> and any data is appended to the destination buffer, this points to the terminating null character at the end of the string.

### -param pcbRemaining [out, optional]

Type: <b>size_t*</b>

The number of unused bytes in <i>pszDest</i>, including those used for the terminating null character. If <i>pcbRemaining</i> is <b>NULL</b>, the count is not kept or returned.

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
If the function fails, the low byte of <i>dwFlags</i> (0) is used to fill the entire <i>pszDest</i> buffer, and the buffer is null-terminated. In the case of a <b>STRSAFE_E_INSUFFICIENT_BUFFER</b> failure, any pre-existing or truncated string in the destination buffer is overwritten.

</td>
</tr>
<tr>
<td width="40%"><a id="STRSAFE_NULL_ON_FAILURE"></a><a id="strsafe_null_on_failure"></a><dl>
<dt><b>STRSAFE_NULL_ON_FAILURE</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
If the function fails, <i>pszDest</i> is set to an empty string (TEXT("")). In the case of a <b>STRSAFE_E_INSUFFICIENT_BUFFER</b> failure, any pre-existing or truncated string in the destination buffer is overwritten.

</td>
</tr>
<tr>
<td width="40%"><a id="STRSAFE_NO_TRUNCATION"></a><a id="strsafe_no_truncation"></a><dl>
<dt><b>STRSAFE_NO_TRUNCATION</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
If the function fails, <i>pszDest</i> is untouched. Nothing is added to the original contents.

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
Source data was present, the strings were concatenated without truncation, and the resultant destination buffer is null-terminated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>cbDest</i> is larger than <code>STRSAFE_MAX_CCH * sizeof(TCHAR)</code>, an invalid flag was passed, or there are discrepancies between the size of the <i>pszDest</i>, <i>cbDest</i>, and the amount of material to append in <i>pszSrc</i>.

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

Compared to  the functions it replaces, <b>StringCbCatNEx</b> provides additional processing for proper buffer handling in your code. Poor buffer handling is implicated in many security issues that involve buffer overruns. <b>StringCbCatNEx</b> always null-terminates and never overflows a valid destination buffer, even if the contents of the source string change during the operation.

Behavior is undefined if the strings pointed to by <i>pszSrc</i> and <i>pszDest</i> overlap.

Neither <i>pszSrc</i> nor <i>pszDest</i> should be <b>NULL</b> unless the <b>STRSAFE_IGNORE_NULLS</b> flag is specified, in which case both may be <b>NULL</b>. However, an error due to insufficient space may still be returned even though <b>NULL</b> values are ignored.

<b>StringCbCatNEx</b> can be used in its generic form, or in its more specific forms. The data type of the string determines the form of this function that you should use.

<table class="clsStd">
<tr>
<th>String Data Type</th>
<th>String Literal</th>
<th>Function</th>
</tr>
<tr>
<td><b>char</b></td>
<td>"string"</td>
<td><b>StringCbCatNExA</b></td>
</tr>
<tr>
<td><b>TCHAR</b></td>
<td>TEXT("string")</td>
<td><b>StringCbCatNEx</b></td>
</tr>
<tr>
<td><b>WCHAR</b></td>
<td>L"string"</td>
<td><b>StringCbCatNExW</b></td>
</tr>
</table>
 





> [!NOTE]
> The strsafe.h header defines StringCbCatNEx as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcatexa">StringCbCatEx</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcatna">StringCbCatN</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcatnexa">StringCchCatNEx</a>
