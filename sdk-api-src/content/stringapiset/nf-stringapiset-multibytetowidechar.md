---
UID: NF:stringapiset.MultiByteToWideChar
title: MultiByteToWideChar function (stringapiset.h)
description: Maps a character string to a UTF-16 (wide character) string.
helpviewer_keywords: ["CP_ACP","CP_MACCP","CP_OEMCP","CP_SYMBOL","CP_THREAD_ACP","CP_UTF7","CP_UTF8","MB_COMPOSITE","MB_ERR_INVALID_CHARS","MB_PRECOMPOSED","MB_USEGLYPHCHARS","MultiByteToWideChar","MultiByteToWideChar function [Internationalization for Windows Applications]","_win32_MultiByteToWideChar","intl.multibytetowidechar","stringapiset/MultiByteToWideChar"]
old-location: intl\multibytetowidechar.htm
tech.root: Intl
ms.assetid: a117fdfe-b52b-466f-9300-6455e91ea2a8
ms.date: 12/05/2018
ms.keywords: CP_ACP, CP_MACCP, CP_OEMCP, CP_SYMBOL, CP_THREAD_ACP, CP_UTF7, CP_UTF8, MB_COMPOSITE, MB_ERR_INVALID_CHARS, MB_PRECOMPOSED, MB_USEGLYPHCHARS, MultiByteToWideChar, MultiByteToWideChar function [Internationalization for Windows Applications], _win32_MultiByteToWideChar, intl.multibytetowidechar, stringapiset/MultiByteToWideChar
f1_keywords:
- stringapiset/MultiByteToWideChar
dev_langs:
- c++
req.header: stringapiset.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- kernel32.dll
- API-MS-Win-Core-String-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
api_name:
- MultiByteToWideChar
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MultiByteToWideChar function


## -description


Maps a character string to a UTF-16 (wide character) string. The character string is not necessarily from a multibyte character set.<div class="alert"><b>Caution</b>  Using the <b>MultiByteToWideChar</b> function incorrectly can compromise the security of your application. Calling this function can easily cause a buffer overrun because the size of the input buffer indicated by <i>lpMultiByteStr</i> equals the number of bytes in the string, while the size of the output buffer indicated by <i>lpWideCharStr</i> equals the number of characters. To avoid a buffer overrun, your application must specify a buffer size appropriate for the data type the buffer receives. For more information, see <a href="https://docs.microsoft.com/windows/desktop/Intl/security-considerations--international-features">Security Considerations: International Features</a>.</div>
<div> </div>
<div class="alert"><b>Note</b>  The ANSI code pages can be different on different computers, or can be changed for a single computer, leading to data corruption. For the most consistent results, applications should use Unicode, such as UTF-8 or UTF-16, instead of a specific code page, unless legacy standards or data formats prevent the use of Unicode. If using Unicode is not possible, applications should tag the data stream with the appropriate encoding name when protocols allow it. HTML and XML files allow tagging, but text files do not.</div>
<div> </div>



## -parameters




### -param CodePage [in]

Code page to use in performing the conversion. This parameter can be set to the value of any code page that is installed or available in the operating system. For a list of code pages, see <a href="https://docs.microsoft.com/windows/desktop/Intl/code-page-identifiers">Code Page Identifiers</a>. Your application can also specify one of the values shown in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CP_ACP"></a><a id="cp_acp"></a><dl>
<dt><b>CP_ACP</b></dt>
</dl>
</td>
<td width="60%">
The system default Windows ANSI code page. 

<div class="alert"><b>Note</b>  This value can be different on different computers, even on the same network. It can be changed on the same computer, leading to stored data becoming irrecoverably corrupted. This value is only intended for temporary use and permanent storage should use UTF-16 or UTF-8 if possible.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="CP_MACCP"></a><a id="cp_maccp"></a><dl>
<dt><b>CP_MACCP</b></dt>
</dl>
</td>
<td width="60%">
The current system Macintosh code page. 

<div class="alert"><b>Note</b>  This value can be different on different computers, even on the same network. It can be changed on the same computer, leading to stored data becoming irrecoverably corrupted. This value is only intended for temporary use and permanent storage should use UTF-16 or UTF-8 if possible.</div>
<div> </div>
<div class="alert"><b>Note</b>   This value is used primarily in legacy code and should not generally be needed since modern Macintosh computers use Unicode for encoding.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="CP_OEMCP"></a><a id="cp_oemcp"></a><dl>
<dt><b>CP_OEMCP</b></dt>
</dl>
</td>
<td width="60%">
The current system OEM code page. 

<div class="alert"><b>Note</b>  This value can be different on different computers, even on the same network. It can be changed on the same computer, leading to stored data becoming irrecoverably corrupted. This value is only intended for temporary use and permanent storage should use UTF-16 or UTF-8 if possible.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="CP_SYMBOL"></a><a id="cp_symbol"></a><dl>
<dt><b>CP_SYMBOL</b></dt>
</dl>
</td>
<td width="60%">
Symbol code page (42).

</td>
</tr>
<tr>
<td width="40%"><a id="CP_THREAD_ACP"></a><a id="cp_thread_acp"></a><dl>
<dt><b>CP_THREAD_ACP</b></dt>
</dl>
</td>
<td width="60%">
The Windows ANSI code page for the current thread. 

<div class="alert"><b>Note</b>  This value can be different on different computers, even on the same network. It can be changed on the same computer, leading to stored data becoming irrecoverably corrupted. This value is only intended for temporary use and permanent storage should use UTF-16 or UTF-8 if possible.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="CP_UTF7"></a><a id="cp_utf7"></a><dl>
<dt><b>CP_UTF7</b></dt>
</dl>
</td>
<td width="60%">
UTF-7. Use this value only when forced by a 7-bit transport mechanism. Use of UTF-8 is preferred.

</td>
</tr>
<tr>
<td width="40%"><a id="CP_UTF8"></a><a id="cp_utf8"></a><dl>
<dt><b>CP_UTF8</b></dt>
</dl>
</td>
<td width="60%">
UTF-8.

</td>
</tr>
</table>
 


### -param dwFlags [in]

Flags indicating the conversion type. The application can specify a combination of the following values, with MB_PRECOMPOSED being the default. MB_PRECOMPOSED and MB_COMPOSITE are mutually exclusive. MB_USEGLYPHCHARS and MB_ERR_INVALID_CHARS can be set regardless of the state of the other flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MB_COMPOSITE"></a><a id="mb_composite"></a><dl>
<dt><b>MB_COMPOSITE</b></dt>
</dl>
</td>
<td width="60%">
Always use decomposed characters, that is, characters in which a base character and one or more nonspacing characters each have distinct code point values. For example, Ä is represented by A + ¨: LATIN CAPITAL LETTER A (U+0041) + COMBINING DIAERESIS (U+0308). Note that this flag cannot be used with MB_PRECOMPOSED.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_ERR_INVALID_CHARS"></a><a id="mb_err_invalid_chars"></a><dl>
<dt><b>MB_ERR_INVALID_CHARS</b></dt>
</dl>
</td>
<td width="60%">
Fail if an invalid input character is encountered.
                  

Starting with Windows Vista, the function does not drop illegal code points if the application does not set this flag, but instead replaces illegal sequences with U+FFFD (encoded as appropriate for the specified codepage).

<b>Windows 2000 with SP4 and later, Windows XP:  </b> If this flag is not set, the function silently drops illegal code points. A call to <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_NO_UNICODE_TRANSLATION.

</td>
</tr>
<tr>
<td width="40%"><a id="MB_PRECOMPOSED"></a><a id="mb_precomposed"></a><dl>
<dt><b>MB_PRECOMPOSED</b></dt>
</dl>
</td>
<td width="60%">
Default; do not use with MB_COMPOSITE. Always use precomposed characters, that is, characters having a single character value for a base or nonspacing character combination. For example, in the character è, the e is the base character and the accent grave mark is the nonspacing character. If a single Unicode code point is defined for a character, the application should use it instead of a separate base character and a nonspacing character. For example, Ä is represented by the single Unicode code point LATIN CAPITAL LETTER A WITH DIAERESIS (U+00C4).

</td>
</tr>
<tr>
<td width="40%"><a id="MB_USEGLYPHCHARS"></a><a id="mb_useglyphchars"></a><dl>
<dt><b>MB_USEGLYPHCHARS</b></dt>
</dl>
</td>
<td width="60%">
Use glyph characters instead of control characters.

</td>
</tr>
</table>
 

For the code pages listed below, <i>dwFlags</i> must be set to 0. Otherwise, the function fails with ERROR_INVALID_FLAGS.

<ul>
<li>50220 </li>
<li>50221
</li>
<li>50222
</li>
<li>50225</li>
<li>50227 </li>
<li>50229
</li>
<li>57002 through 57011</li>
<li>65000 (UTF-7)</li>
<li>42 (Symbol)</li>
</ul>
<div class="alert"><b>Note</b>  For UTF-8 or code page 54936 (GB18030, starting with Windows Vista), <i>dwFlags</i> must be set to either 0 or MB_ERR_INVALID_CHARS. Otherwise, the function fails with ERROR_INVALID_FLAGS.</div>
<div> </div>

### -param lpMultiByteStr [in]

Pointer to the character string to convert.


### -param cbMultiByte [in]

Size, in bytes, of the string indicated by the <i>lpMultiByteStr</i> parameter. Alternatively, this parameter can be set to -1 if the string is null-terminated. Note that, if <i>cbMultiByte</i> is 0, the function fails.

If this parameter is -1, the function processes the entire input string, including the terminating null character. Therefore, the resulting Unicode string has a terminating null character, and the length returned by the function includes this character.

If this parameter is set to a positive integer, the function processes exactly the specified number of bytes. If the provided size does not include a terminating null character, the resulting Unicode string is not null-terminated, and the returned length does not include this character.


### -param lpWideCharStr [out, optional]

Pointer to a buffer that receives the converted string.


### -param cchWideChar [in]

Size, in characters, of the buffer indicated by <i>lpWideCharStr</i>. If this value is 0, the function returns the required buffer size, in characters, including any terminating null character, and makes no use of the <i>lpWideCharStr</i> buffer.


## -returns



Returns the number of characters written to the buffer indicated by <i>lpWideCharStr</i> if successful. If the function succeeds and <i>cchWideChar</i> is 0, the return value is the required size, in characters, for the buffer indicated by <i>lpWideCharStr</i>. Also see <i>dwFlags</i> for info about how the MB_ERR_INVALID_CHARS flag affects the return value when invalid sequences are input.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid. </li>
<li>ERROR_NO_UNICODE_TRANSLATION. Invalid Unicode was found in a string.</li>
</ul>



## -remarks



The default behavior of this function is to translate to a precomposed form of the input character string. If a precomposed form does not exist, the function attempts to translate to a composite form.

The use of the MB_PRECOMPOSED flag has very little effect on most code pages because most input data is composed already. Consider calling <a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-normalizestring">NormalizeString</a> after converting with <b>MultiByteToWideChar</b>. <b>NormalizeString</b> provides more accurate, standard, and consistent data, and can also be faster. Note that for the <a href="https://docs.microsoft.com/windows/desktop/api/winnls/ne-winnls-norm_form">NORM_FORM</a> enumeration being passed to <b>NormalizeString</b>, NormalizationC corresponds to MB_PRECOMPOSED and NormalizationD corresponds to MB_COMPOSITE.

As mentioned in the caution above, the output buffer can easily be overrun if this function is not first called with <i>cchWideChar</i> set to 0 in order to obtain the required size. If the MB_COMPOSITE flag is used, the output can be three or more characters long for each input character.

The <i>lpMultiByteStr</i> and <i>lpWideCharStr</i> pointers must not be the same. If they are the same, the function fails, and <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns the value ERROR_INVALID_PARAMETER.

<b>MultiByteToWideChar</b> does not null-terminate an output string if the input string length is explicitly specified without a terminating null character. To null-terminate an output string for this function, the application should pass in -1 or explicitly count the terminating null character for the input string.

The function fails if MB_ERR_INVALID_CHARS is set and an invalid character is encountered in the source string. An invalid character is one of the following:

<ul>
<li>A character that is not the default character in the source string, but translates to the default character when MB_ERR_INVALID_CHARS is not set</li>
<li>For DBCS strings, a character that has a lead byte but no valid trail byte</li>
</ul>
Starting with Windows Vista, this function fully conforms with the Unicode 4.1 specification for UTF-8 and UTF-16. The function used on earlier operating systems encodes or decodes lone <a href="https://docs.microsoft.com/windows/desktop/Intl/surrogates-and-supplementary-characters">surrogate</a> halves or mismatched surrogate pairs. Code written in earlier versions of Windows that rely on this behavior to encode random non-text binary data might run into problems. However, code that uses this function on valid UTF-8 strings will behave the same way as on earlier Windows operating systems.

<b>Windows XP:</b> To prevent the security problem of the non-shortest-form versions of UTF-8 characters, <b>MultiByteToWideChar</b> deletes these characters.

<b>Starting with Windows 8: </b><b>MultiByteToWideChar</b>  is declared in Stringapiset.h. Before Windows 8, it was declared in Winnls.h.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Intl/unicode-and-character-set-functions">Unicode and Character Set Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/unicode-and-character-sets">Unicode and Character Sets</a>



<a href="https://docs.microsoft.com/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte">WideCharToMultiByte</a>
 

 

