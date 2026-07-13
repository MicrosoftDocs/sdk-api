---
UID: NF:strsafe.StringCbLengthA
title: StringCbLengthA function (strsafe.h)
description: Determines whether a string exceeds the specified length, in bytes. (ANSI)
helpviewer_keywords: ["StringCbLengthA", "strsafe/StringCbLengthA"]
old-location: menurc\stringcblength.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\stringcblength.htm
ms.date: 12/05/2018
ms.keywords: StringCbLength, StringCbLength function [Menus and Other Resources], StringCbLengthA, StringCbLengthW, UnalignedStringCbLength, _shell_StringCbLength, _shell_stringcblength_cpp, menurc.stringcblength, strsafe/StringCbLength, strsafe/StringCbLengthA, strsafe/StringCbLengthW, winui._shell_stringcblength
req.header: strsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StringCbLengthW (Unicode) and StringCbLengthA (ANSI)
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
 - StringCbLengthA
 - strsafe/StringCbLengthA
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
 - StringCbLength
 - StringCbLengthA
 - StringCbLengthW
---

# StringCbLengthA function


## -description

Determines whether a  string exceeds the specified length, in bytes.

<b>StringCbLength</b> is a replacement for the following functions:
<ul>
<li><a href="/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l">strlen, wcslen, _tcslen</a></li>
</ul>

## -parameters

### -param psz [in]

Type: <b>LPCTSTR</b>

The string whose length is to be checked.

### -param cbMax [in]

Type: <b>size_t</b>

The maximum number of bytes allowed in <i>psz</i>, including those used for the terminating null character. This value cannot exceed <code>STRSAFE_MAX_CCH * sizeof(TCHAR)</code>.

### -param pcbLength [out]

Type: <b>size_t*</b>

The number of bytes in <i>psz</i>, excluding those used for the terminating null character. This value is valid only if <i>pcb</i> is not <b>NULL</b> and the function succeeds.

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
The string at <i>psz</i> was not <b>NULL</b>, and the length of the string (including the terminating null character) is less than or equal to <i>cbMax</i> characters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>psz</i> is <b>NULL</b>, <i>cbMax</i> is larger than <code>STRSAFE_MAX_CCH * sizeof(TCHAR)</code>, or <i>psz</i> is longer than <i>cbMax</i>.

</td>
</tr>
</table>
 

Note that this function returns an <b>HRESULT</b> value, unlike the functions that it replaces.

## -remarks

Compared to  the functions it replaces, <b>StringCbLength</b> is an additional tool for proper buffer handling in your code. Poor buffer handling is implicated in many security issues that involve buffer overruns.

<b>StringCbLength</b> can be used in its generic form, or in its more specific forms. The data type of the string determines the form of this function that you should use.

<table class="clsStd">
<tr>
<th>String Data Type</th>
<th>String Literal</th>
<th>Function</th>
</tr>
<tr>
<td><b>char</b></td>
<td>"string"</td>
<td><b>StringCbLengthA</b></td>
</tr>
<tr>
<td><b>TCHAR</b></td>
<td>TEXT("string")</td>
<td><b>StringCbLength</b></td>
</tr>
<tr>
<td><b>WCHAR</b></td>
<td>L"string"</td>
<td><b>StringCbLengthW</b></td>
</tr>
</table>
 


<a href="/previous-versions/windows/desktop/legacy/hh305643(v=vs.85)">UnalignedStringCbLength</a> is an alias for this function.





> [!NOTE]
> The strsafe.h header defines StringCbLength as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchlengtha">StringCchLength</a>
