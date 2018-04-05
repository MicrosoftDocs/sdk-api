---
UID: NF:strsafe.StringCbGetsExA
title: StringCbGetsExA function
author: windows-driver-content
description: Gets one line of text from stdin, up to and including the newline character ('\n').
old-location: menurc\stringcbgetsex.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\stringcbgetsex.htm
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: STRSAFE_FILL_BEHIND_NULL, STRSAFE_FILL_ON_FAILURE, STRSAFE_IGNORE_NULLS, STRSAFE_NO_TRUNCATION, STRSAFE_NULL_ON_FAILURE, StringCbGetsEx, StringCbGetsEx function [Menus and Other Resources], StringCbGetsExA, StringCbGetsExW, _shell_StringCbGetsEx, _shell_stringcbgetsex_cpp, menurc.stringcbgetsex, strsafe/StringCbGetsEx, strsafe/StringCbGetsExA, strsafe/StringCbGetsExW, winui._shell_stringcbgetsex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: strsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StringCbGetsExW (Unicode) and StringCbGetsExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AM_DVD_RENDERSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Strsafe.h
api_name:
-	StringCbGetsEx
-	StringCbGetsExA
-	StringCbGetsExW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# StringCbGetsExA function


## -description


Gets one line of text from stdin, up to and including the newline character ('\n'). The line of text is copied to the destination buffer, and the newline character is replaced with a null character. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer.
<div class="alert"><b>Note</b>  This function can only be used inline.</div><div> </div><b>StringCbGetsEx</b> adds to the functionality of <a href="https://msdn.microsoft.com/6dea3433-9d63-40b0-907a-c79dd11ecd6f">StringCbGets</a> by returning a pointer to the end of the destination string as well as the number of bytes left unused in that string. Flags may also be passed to the function for additional control.

<b>StringCbGetsEx</b> is a replacement for the following functions:
<ul>
<li><a href="http://go.microsoft.com/fwlink/p/?linkid=192504">gets, _getws, _getts</a></li>
</ul><b>StringCbGetsEx</b> is not a replacement for <b>fgets</b>, which does not replace newline characters with a terminating null character.


## -parameters




### -param pszDest [out]

Type: <b>LPTSTR</b>

The destination buffer, which is to receive the input.


### -param cbDest [in]

Type: <b>size_t</b>

The size of the destination buffer, in bytes. This value must be greater than <code>sizeof(TCHAR)</code> for the function to succeed. The maximum number of bytes allowed is <code>STRSAFE_MAX_CCH * sizeof(TCHAR)</code>. If <i>cbDest</i> is too small to hold the full line of text, the data is truncated.


### -param ppszDestEnd [out, optional]

Type: <b>LPTSTR*</b>

The address of a pointer to the end of <i>pszDest</i>. If <i>ppszDestEnd</i> is non-<b>NULL</b> and any data is copied into the destination buffer, this points to the terminating null character at the end of the string.


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
Treat <b>NULL</b> string pointers like empty strings (TEXT("")). This flag is useful for emulating functions such as <a href="https://msdn.microsoft.com/3960fe0e-954d-4463-bc81-e1682e468278">lstrcpy</a>.

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
 


## -returns



Type: <b>HRESULT</b>

This function can return one of the following values. It is strongly recommended that you use the <a href="https://msdn.microsoft.com/7a258b0b-d214-46c5-be0a-6493cd14a0e5">SUCCEEDED</a> and <a href="https://msdn.microsoft.com/d9c4ff73-c255-4a82-b901-23bd5b41ee6c">FAILED</a> macros to test the return value of this function.

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
Data was read from stdin, was copied to the buffer at <i>pszDest</i>, and the buffer was null-terminated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_END_OF_FILE</b></dt>
</dl>
</td>
<td width="60%">
Indicates an error or end-of-file condition. Use <a href="09081eee-7c4b-4189-861f-2fad95d3ec6d">feof</a> or <a href="528a34bc-f2aa-4c3f-b89a-5b148e6864f7">ferror</a> to determine which one has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>cbDest</i> is larger than the maximum allowed value or an invalid flag was passed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>cbDest</i> is 1 or less.

</td>
</tr>
</table>
 

Note that this function returns an <b>HRESULT</b> value, unlike the functions that it replaces.




## -remarks



<b>StringCbGetsEx</b> provides additional processing for proper buffer handling in your code. Poor buffer handling is implicated in many security issues that involve buffer overruns. <b>StringCbGetsEx</b>
				always null-terminates a nonzero-length destination buffer.

The value of <i>pszDest</i> should not be <b>NULL</b> unless the <b>STRSAFE_IGNORE_NULLS</b> flag is specified. However, an error due to insufficient space may still be returned even though <b>NULL</b> values are ignored.

<b>StringCbGetsEx</b> can be used in its generic form, or in its more specific forms. The data type of the string determines the form of this function that you should use, as shown in the following table.

<table class="clsStd">
<tr>
<th>String Data Type</th>
<th>String Literal</th>
<th>Function</th>
</tr>
<tr>
<td><b>char</b></td>
<td>"string"</td>
<td><b>StringCbGetsExA</b></td>
</tr>
<tr>
<td><b>TCHAR</b></td>
<td>TEXT("string")</td>
<td><b>StringCbGetsEx</b></td>
</tr>
<tr>
<td><b>WCHAR</b></td>
<td>L"string"</td>
<td><b>StringCbGetsExW</b></td>
</tr>
</table>
 




## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/6dea3433-9d63-40b0-907a-c79dd11ecd6f">StringCbGets</a>



<a href="https://msdn.microsoft.com/12937a53-377d-46a7-88fb-124ade72f866">StringCchGetsEx</a>
 

 

