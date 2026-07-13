---
UID: NF:strsafe.StringCchCopyNW
title: StringCchCopyNW function (strsafe.h)
description: Copies the specified number of characters from one string to another. (StringCchCopyNW)
helpviewer_keywords: ["StringCchCopyN", "StringCchCopyN function [Menus and Other Resources]", "StringCchCopyNW", "_shell_StringCchCopyN", "_shell_stringcchcopyn_cpp", "menurc.stringcchcopyn", "strsafe/StringCchCopyN", "strsafe/StringCchCopyNW", "winui._shell_stringcchcopyn"]
old-location: menurc\stringcchcopyn.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\stringcchcopyn.htm
ms.date: 12/05/2018
ms.keywords: StringCchCopyN, StringCchCopyN function [Menus and Other Resources], StringCchCopyNA, StringCchCopyNW, _shell_StringCchCopyN, _shell_stringcchcopyn_cpp, menurc.stringcchcopyn, strsafe/StringCchCopyN, strsafe/StringCchCopyNA, strsafe/StringCchCopyNW, winui._shell_stringcchcopyn
req.header: strsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StringCchCopyNW (Unicode) and StringCchCopyNA (ANSI)
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
 - StringCchCopyNW
 - strsafe/StringCchCopyNW
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
 - StringCchCopyN
 - StringCchCopyNA
 - StringCchCopyNW
---

# StringCchCopyNW function


## -description

Copies the specified number of characters from one string to another. The size of the destination buffer is provided to the function to ensure that <b>StringCchCopyN</b> does not write past the end of this buffer.

<b>StringCchCopyN</b> is a replacement for the following functions:
<ul>
<li><a href="/cpp/c-runtime-library/reference/strncpy-strncpy-l-wcsncpy-wcsncpy-l-mbsncpy-mbsncpy-l">strncpy, wcsncpy, _tcsncpy</a></li>
</ul>

## -parameters

### -param pszDest [out]

Type: <b>LPTSTR</b>

The destination buffer, which receives the copied characters.

### -param cchDest [in]

Type: <b>size_t</b>

The size of <i>pszDest</i>, in characters. This value must be large enough to hold the copied characters (the length of <i>pszSrc</i> or the value of <i>cchSrc</i>, whichever is smaller) plus 1 to account for the terminating null character. The maximum number of characters allowed is <b>STRSAFE_MAX_CCH</b>.

### -param pszSrc [in]

Type: <b>LPCTSTR</b>

The source string. This string must be readable up to <i>cchSrc</i> characters or a null terminator, whichever comes first.

### -param cchToCopy [in]

Type: <b>size_t</b>

The maximum number of characters to be copied from <i>pszSrc</i> to <i>pszDest</i>.

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
Source data was present, the characters were copied from <i>pszSrc</i> without truncation, and the resultant destination buffer is null-terminated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>cchDest</i> is either larger than <b>STRSAFE_MAX_CCH</b>, or the destination buffer is already full.

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

<b>StringCchCopyN</b> provides additional processing for proper buffer handling in your code. Poor buffer handling is implicated in many security issues that involve buffer overruns. <b>StringCchCopyN</b> always null-terminates and never overflows a valid destination buffer, even if the contents of the source string change during the operation.

While this routine is meant as a replacement for <a href="/previous-versions/visualstudio/visual-studio-2010/xdsywd25(v=vs.100)">strncpy</a>, there are differences in behavior. If <i>cchSrc</i> is larger than the number of characters in <i>pszSrc</i>, <b>StringCchCopyN</b>—unlike <b>strncpy</b>—does not continue to pad <i>pszDest</i> with null characters until <i>cchSrc</i> characters have been copied.

Behavior is undefined if the strings pointed to by <i>pszSrc</i> and <i>pszDest</i> overlap.

Neither <i>pszSrc</i> nor <i>pszDest</i> should be <b>NULL</b>. See <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopynexa">StringCchCopyNEx</a> if you require the handling of null string pointer values.

<b>StringCchCopyN</b> can be used in its generic form, or in its more specific forms. The data type of the string determines the form of this function that you should use, as shown in the following table.

<table class="clsStd">
<tr>
<th>String Data Type</th>
<th>String Literal</th>
<th>Function</th>
</tr>
<tr>
<td><b>char</b></td>
<td>"string"</td>
<td><b>StringCchCopyNA</b></td>
</tr>
<tr>
<td><b>TCHAR</b></td>
<td>TEXT("string")</td>
<td><b>StringCchCopyN</b></td>
</tr>
<tr>
<td><b>WCHAR</b></td>
<td>L"string"</td>
<td><b>StringCchCopyNW</b></td>
</tr>
</table>
 





> [!NOTE]
> The strsafe.h header defines StringCchCopyN as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcopyna">StringCbCopyN</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopya">StringCchCopy</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopynexa">StringCchCopyNEx</a>
