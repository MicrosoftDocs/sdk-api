---
UID: NF:strsafe.StringCchVPrintf_lExA
title: StringCchVPrintf_lExA function (strsafe.h)
description: Writes formatted data to the specified string using a pointer to a list of arguments. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer.helpviewer_keywords: ["STRSAFE_FILL_BEHIND_NULL","STRSAFE_FILL_ON_FAILURE","STRSAFE_IGNORE_NULLS","STRSAFE_NO_TRUNCATION","STRSAFE_NULL_ON_FAILURE","StringCchVPrintf_lEx","StringCchVPrintf_lEx function [Menus and Other Resources]","StringCchVPrintf_lExA","StringCchVPrintf_lExW","menurc.stringcchvprintf_lex","strsafe/StringCchVPrintf_lEx","strsafe/StringCchVPrintf_lExA","strsafe/StringCchVPrintf_lExW"]
old-location: menurc\stringcchvprintf_lex.htm
tech.root: menurc
ms.assetid: 9ba9b785-806d-4a94-9ff4-81307dc6d8b9
ms.date: 12/05/2018
ms.keywords: STRSAFE_FILL_BEHIND_NULL, STRSAFE_FILL_ON_FAILURE, STRSAFE_IGNORE_NULLS, STRSAFE_NO_TRUNCATION, STRSAFE_NULL_ON_FAILURE, StringCchVPrintf_lEx, StringCchVPrintf_lEx function [Menus and Other Resources], StringCchVPrintf_lExA, StringCchVPrintf_lExW, menurc.stringcchvprintf_lex, strsafe/StringCchVPrintf_lEx, strsafe/StringCchVPrintf_lExA, strsafe/StringCchVPrintf_lExW
f1_keywords:
- strsafe/StringCchVPrintf_lEx
dev_langs:
- c++
req.header: strsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StringCchVPrintf_lExW (Unicode) and StringCchVPrintf_lExA (ANSI)
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
- StrSafe.h
api_name:
- StringCchVPrintf_lEx
- StringCchVPrintf_lExA
- StringCchVPrintf_lExW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# StringCchVPrintf_lExA function


## -description


Writes formatted data to the specified string using a pointer to a list of arguments. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer.

<b>StringCchVPrintf_lEx</b> is similar to <a href="https://docs.microsoft.com/windows/desktop/api/strsafe/nf-strsafe-stringcchvprintfexa">StringCchVPrintfEx</a> but includes a parameter for locale information.


## -parameters




### -param pszDest [out]

The destination buffer, which receives the formatted, null-terminated string created from <i>pszFormat</i> and <i>argList</i>.


### -param cchDest [in]

The size of the destination buffer, in characters. This value must be sufficiently large to accommodate the final formatted string plus 1 to account for the terminating null character. The maximum number of characters allowed is <b>STRSAFE_MAX_CCH</b>.


### -param ppszDestEnd [out]

The address of a pointer to the end of <i>pszDest</i>. If <i>ppszDestEnd</i> is non-<b>NULL</b> and any data is copied into the destination buffer, this points to the terminating null character at the end of the string.


### -param pcchRemaining [out, optional]

The number of unused characters in <i>pszDest</i>, including the terminating null character. If <i>pcchRemaining</i> is <b>NULL</b>, the count is not kept or returned.


### -param dwFlags [in]

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

The format string. This string must be null-terminated. For more information, see <a href="https://docs.microsoft.com/cpp/c-runtime-library/format-specification-syntax-printf-and-wprintf-functions">Format Specification Syntax</a>.


### -param locale [in]

The locale object. For more information, see <b>_create_locale</b>.


### -param argList [in]

The arguments to be inserted into the <i>pszFormat</i> string.


## -returns



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
 




## -remarks



For more information on va_lists, see the conventions defined in Stdarg.h.

Behavior is undefined if the strings pointed to by <i>pszDest</i>, <i>pszFormat</i>, or any argument strings overlap.

Neither <i>pszFormat</i> nor <i>pszDest</i> should be <b>NULL</b> unless the <b>STRSAFE_IGNORE_NULLS</b> flag is specified, in which case both may be <b>NULL</b>. However, an error due to insufficient space may still be returned even though <b>NULL</b> values are ignored.

In order to use this function, you must define the following macro in your header file, before including StrSafe.h.

<code>#define STRSAFE_LOCALE_FUNCTIONS</code>



