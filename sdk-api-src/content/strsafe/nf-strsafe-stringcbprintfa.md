---
UID: NF:strsafe.StringCbPrintfA
title: StringCbPrintfA function (strsafe.h)
description: Writes formatted data to the specified string. (StringCbPrintfA)
helpviewer_keywords: ["StringCbPrintfA", "strsafe/StringCbPrintfA"]
old-location: menurc\stringcbprintf.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\stringcbprintf.htm
ms.date: 12/05/2018
ms.keywords: StringCbPrintf, StringCbPrintf function [Menus and Other Resources], StringCbPrintfA, StringCbPrintfW, _shell_StringCbPrintf, _shell_stringcbprintf_cpp, menurc.stringcbprintf, strsafe/StringCbPrintf, strsafe/StringCbPrintfA, strsafe/StringCbPrintfW, winui._shell_stringcbprintf
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StringCbPrintfA
 - strsafe/StringCbPrintfA
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
 - StringCbPrintf
 - StringCbPrintfA
 - StringCbPrintfW
---

# StringCbPrintfA function


## -description

Writes formatted data to the specified string. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer.

<b>StringCbPrintf</b> is a replacement for the following functions:
				
<ul>
<li><a href="/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l">sprintf, swprintf, _stprintf</a></li>
<li>
<a href="/windows/desktop/api/winuser/nf-winuser-wsprintfa">wsprintf</a>
</li>
<li>
<a href="/windows/desktop/api/shlwapi/nf-shlwapi-wnsprintfa">wnsprintf</a>
</li>
<li><a href="/cpp/c-runtime-library/reference/snprintf-snprintf-snprintf-l-snwprintf-snwprintf-l">_snprintf, _snwprintf, _sntprintf</a></li>
</ul>

## -parameters

### -param pszDest [out]

Type: <b>LPSTR</b>

The destination buffer, which receives the formatted, null-terminated string created from <i>pszFormat</i> and its arguments.

### -param cbDest [in]

Type: <b>size_t</b>

The size of the destination buffer, in bytes. This value must be sufficiently large to accommodate the final formatted string plus the terminating null character. The maximum number of bytes allowed is <code>STRSAFE_MAX_CCH * sizeof(TCHAR)</code>.

### -param pszFormat [in]

Type: <b>LPCSTR</b>

The format string. This string must be null-terminated. For more information, see <a href="/cpp/c-runtime-library/format-specification-syntax-printf-and-wprintf-functions">Format Specification Syntax</a>.

### -param ...

The arguments to be inserted into the <i>pszFormat</i> string.

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

Compared to  the functions it replaces, <b>StringCbPrintf</b> provides additional processing for proper buffer handling in your code. Poor buffer handling is implicated in many security issues that involve buffer overruns. <b>StringCbPrintf</b> always null-terminates a nonzero-length destination buffer.

Behavior is undefined if the strings pointed to by <i>pszDest</i>, <i>pszFormat</i>, or any argument strings overlap.

Neither <i>pszFormat</i> nor <i>pszDest</i> should be <b>NULL</b>. See <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbprintfexa">StringCbPrintfEx</a> if you require the handling of null string pointer values.

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


```cpp
int const arraysize = 30;
TCHAR pszDest[arraysize]; 
size_t cbDest = arraysize * sizeof(TCHAR);

LPCTSTR pszFormat = TEXT("%s %d + %d = %d.");
TCHAR* pszTxt = TEXT("The answer is");

HRESULT hr = StringCbPrintf(pszDest, cbDest, pszFormat, pszTxt, 1, 2, 3);

// The resultant string at pszDest is "The answer is 1 + 2 = 3."
```






> [!NOTE]
> The strsafe.h header defines StringCbPrintf as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbprintfexa">StringCbPrintfEx</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbvprintfa">StringCbVPrintf</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa">StringCchPrintf</a>

