---
UID: NF:strsafe.StringCbCatA
title: StringCbCatA function (strsafe.h)
description: Concatenates one string to another string. (StringCbCatA)
helpviewer_keywords: ["StringCbCatA", "strsafe/StringCbCatA"]
old-location: menurc\stringcbcat.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\stringcbcat.htm
ms.date: 12/05/2018
ms.keywords: StringCbCat, StringCbCat function [Menus and Other Resources], StringCbCatA, StringCbCatW, _shell_StringCbCat, _shell_stringcbcat_cpp, menurc.stringcbcat, strsafe/StringCbCat, strsafe/StringCbCatA, strsafe/StringCbCatW, winui._shell_stringcbcat
req.header: strsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StringCbCatW (Unicode) and StringCbCatA (ANSI)
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
 - StringCbCatA
 - strsafe/StringCbCatA
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
 - StringCbCat
 - StringCbCatA
 - StringCbCatW
---

# StringCbCatA function


## -description

Concatenates one  string to another string. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer.

<b>StringCbCat</b> is a replacement for the following functions:
<ul>
<li><a href="/cpp/c-runtime-library/reference/strcat-wcscat-mbscat">strcat, wcscat, _tcsat</a></li>
<li>
<a href="/windows/desktop/api/winbase/nf-winbase-lstrcata">lstrcat</a>
</li>
<li>
<a href="/windows/desktop/api/shlwapi/nf-shlwapi-strcatw">StrCat</a>
</li>
<li>
<a href="/windows/desktop/api/shlwapi/nf-shlwapi-strcatbuffa">StrCatBuff</a>
</li>
</ul>

## -parameters

### -param pszDest [in, out]

Type: <b>LPTSTR</b>

The string to which <i>pszSrc</i> is to be concatenated, and that will receive the entire resultant string. The string at <i>pszSrc</i> is added to the end of the string at <i>pszDest</i>.

### -param cbDest [in]

Type: <b>size_t</b>

The size of the destination buffer, in bytes. This value must consider the length of <i>pszSrc</i> plus the length of <i>pszDest</i> plus the terminating null character. The maximum number of bytes allowed is <code>STRSAFE_MAX_CCH * sizeof(TCHAR)</code>.

### -param pszSrc [in]

Type: <b>LPCTSTR</b>

The source string that is to be concatenated to the end of <i>pszDest</i>. This string must be null-terminated.

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
Source data was present, the strings were fully concatenated without truncation, and the resultant destination buffer is null-terminated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>cbDest</i> is either less than <code>sizeof(TCHAR)</code> or larger than the maximum allowed value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The concatenation operation failed due to insufficient buffer space. The destination buffer contains a truncated, null-terminated version of the intended result. In situations where truncation is acceptable, this may not necessarily be seen as a failure condition.

</td>
</tr>
</table>
 

Note that this function returns an <b>HRESULT</b> value, unlike the functions that it replaces.

## -remarks

<b>StringCbCat</b> provides additional processing for proper buffer handling in your code. Poor buffer handling is implicated in many security issues that involve buffer overruns. It always null-terminates and never overflows a valid destination buffer, even if the contents of the source string change during the operation.

<b>StringCbCat</b> can be used in its generic form, or in its more specific forms. The data type of the string determines the form of this function that you should use, as shown in the following table.

<table class="clsStd">
<tr>
<th>String Data Type</th>
<th>String Literal</th>
<th>Function</th>
</tr>
<tr>
<td><b>char</b></td>
<td>"string"</td>
<td><b>StringCbCatA</b></td>
</tr>
<tr>
<td><b>TCHAR</b></td>
<td>TEXT("string")</td>
<td><b>StringCbCat</b></td>
</tr>
<tr>
<td><b>WCHAR</b></td>
<td>L"string"</td>
<td><b>StringCbCatW</b></td>
</tr>
</table>
 

Behavior is undefined if the strings pointed to by <i>pszSrc</i> and <i>pszDest</i> overlap.

Neither <i>pszSrc</i> nor <i>pszDest</i> should be <b>NULL</b>. See <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcatexa">StringCbCatEx</a> if you require the handling of null string pointer values.





> [!NOTE]
> The strsafe.h header defines StringCbCat as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcatexa">StringCbCatEx</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcatna">StringCbCatN</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcata">StringCchCat</a>
