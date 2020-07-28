---
UID: NF:strsafe.StringCbCopyA
title: StringCbCopyA function (strsafe.h)
description: Copies one string to another.
helpviewer_keywords: ["StringCbCopy","StringCbCopy function [Menus and Other Resources]","StringCbCopyA","StringCbCopyW","_shell_StringCbCopy","_shell_stringcbcopy_cpp","menurc.stringcbcopy","strsafe/StringCbCopy","strsafe/StringCbCopyA","strsafe/StringCbCopyW","winui._shell_stringcbcopy"]
old-location: menurc\stringcbcopy.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\stringcbcopy.htm
ms.date: 12/05/2018
ms.keywords: StringCbCopy, StringCbCopy function [Menus and Other Resources], StringCbCopyA, StringCbCopyW, _shell_StringCbCopy, _shell_stringcbcopy_cpp, menurc.stringcbcopy, strsafe/StringCbCopy, strsafe/StringCbCopyA, strsafe/StringCbCopyW, winui._shell_stringcbcopy
f1_keywords:
- strsafe/StringCbCopy
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
req.unicode-ansi: StringCbCopyW (Unicode) and StringCbCopyA (ANSI)
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
- StringCbCopy
- StringCbCopyA
- StringCbCopyW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# StringCbCopyA function


## -description


Copies one string to another. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer.

<b>StringCbCopy</b> is a replacement for the following functions:
<ul>
<li><a href="https://msdn.microsoft.com/library/kk6xf663.aspx">strcpy, wcscpy, _tcscpy</a></li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-lstrcpya">lstrcpy</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-strcpyw">StrCpy</a>
</li>
</ul>

## -parameters




### -param pszDest [out]

Type: <b>LPTSTR</b>

The destination buffer, which receives the copied string.


### -param cbDest [in]

Type: <b>size_t</b>

The size of the destination buffer, in bytes. This value must consider the length of <i>pszSrc</i> plus the terminating null character. The maximum number of bytes allowed is <code>STRSAFE_MAX_CCH * sizeof(TCHAR)</code>.


### -param pszSrc [in]

Type: <b>LPCTSTR</b>

A pointer to a buffer containing the source string. This source string must be null-terminated.


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
Source data was present, fully copied without truncation, and the resultant destination buffer is null-terminated.

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
The copy operation failed due to insufficient buffer space. The destination buffer contains a truncated, null-terminated version of the intended result. In situations where truncation is acceptable, this may not necessarily be seen as a failure condition.

</td>
</tr>
</table>
 

Note that this function returns an <b>HRESULT</b> value, unlike the functions that it replaces.




## -remarks



Compared to  the functions it replaces, <b>StringCbCopy</b> provides additional processing for proper buffer handling in your code. Poor buffer handling is implicated in many security issues that involve buffer overruns. <b>StringCbCopy</b>always null-terminates and never overflows a valid destination buffer, even if the contents of the source string change during the operation.

Behavior is undefined if the strings pointed to by <i>pszSrc</i> and <i>pszDest</i> overlap.

Neither <i>pszSrc</i> nor <i>pszDest</i> should be <b>NULL</b>. See <a href="https://docs.microsoft.com/windows/desktop/api/strsafe/nf-strsafe-stringcbcopyexa">StringCbCopyEx</a> if you require the handling of null string pointer values.

<b>StringCbCopy</b> can be used in its generic form, or in its more specific forms. The data type of the string determines the form of this function that you should use.

<table class="clsStd">
<tr>
<th>String Data Type</th>
<th>String Literal</th>
<th>Function</th>
</tr>
<tr>
<td><b>char</b></td>
<td>"string"</td>
<td><b>StringCbCopyA</b></td>
</tr>
<tr>
<td><b>TCHAR</b></td>
<td>TEXT("string")</td>
<td><b>StringCbCopy</b></td>
</tr>
<tr>
<td><b>WCHAR</b></td>
<td>L"string"</td>
<td><b>StringCbCopyW</b></td>
</tr>
</table>
 





> [!NOTE]
> The strsafe.h header defines StringCbCopy as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also




<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/strsafe/nf-strsafe-stringcbcopyexa">StringCbCopyEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strsafe/nf-strsafe-stringcchcopya">StringCchCopy</a>
 

 

