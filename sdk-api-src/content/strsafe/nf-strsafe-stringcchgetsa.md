---
UID: NF:strsafe.StringCchGetsA
title: StringCchGetsA function (strsafe.h)
description: Gets one line of text from stdin, up to and including the newline character ('\n'). (StringCchGetsA)
helpviewer_keywords: ["StringCchGetsA", "strsafe/StringCchGetsA"]
old-location: menurc\stringcchgets.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\stringcchgets.htm
ms.date: 12/05/2018
ms.keywords: StringCchGets, StringCchGets function [Menus and Other Resources], StringCchGetsA, StringCchGetsW, _shell_StringCchGets, _shell_stringcchgets_cpp, menurc.stringcchgets, strsafe/StringCchGets, strsafe/StringCchGetsA, strsafe/StringCchGetsW, winui._shell_stringcchgets
req.header: strsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StringCchGetsW (Unicode) and StringCchGetsA (ANSI)
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
 - StringCchGetsA
 - strsafe/StringCchGetsA
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
 - StringCchGets
 - StringCchGetsA
 - StringCchGetsW
---

# StringCchGetsA function


## -description

Gets one line of text from stdin, up to and including the newline character ('\n'). The line of text is copied to the destination buffer, and the newline character is replaced with a null character. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer.
<div class="alert"><b>Note</b>  This function can only be used inline.</div><div> </div><b>StringCchGets</b> is a replacement for the following functions:
<ul>
<li><a href="/cpp/c-runtime-library/gets-getws">gets, _getws, _getts</a></li>
</ul><b>StringCchGets</b> is not a replacement for <b>fgets</b>, which does not replace newline characters with a terminating null character.

## -parameters

### -param pszDest [out]

Type: <b>LPTSTR</b>

The destination buffer, which receives the copied characters.

### -param cchDest [in]

Type: <b>size_t</b>

The size of the destination buffer, in characters. This value must be at least 2 for the function to succeed. The maximum number of characters allowed, including the terminating null character, is <b>STRSAFE_MAX_CCH</b>. If <i>cchDest</i> is too small to hold the full line of text, the data is truncated.

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
The value in <i>cchDest</i> is larger than the maximum allowed value.

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

<b>StringCchGets</b> provides additional processing for proper buffer handling in your code. Poor buffer handling is implicated in many security issues that involve buffer overruns. <b>StringCchGets</b> always null-terminates a nonzero-length destination buffer.

The value of <i>pszDest</i> should not be <b>NULL</b>. See <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchgetsexa">StringCchGetsEx</a> if you require the handling of null string pointer values.

<b>StringCchGets</b> can be used in its generic form, or in its more specific forms. The data type of the string determines the form of this function that you should use, as shown in the following table.

<table class="clsStd">
<tr>
<th>String Data Type</th>
<th>String Literal</th>
<th>Function</th>
</tr>
<tr>
<td><b>char</b></td>
<td>"string"</td>
<td><b>StringCchGetsA</b></td>
</tr>
<tr>
<td><b>TCHAR</b></td>
<td>TEXT("string")</td>
<td><b>StringCchGets</b></td>
</tr>
<tr>
<td><b>WCHAR</b></td>
<td>L"string"</td>
<td><b>StringCchGetsW</b></td>
</tr>
</table>
 





> [!NOTE]
> The strsafe.h header defines StringCchGets as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbgetsa">StringCbGets</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchgetsexa">StringCchGetsEx</a>
