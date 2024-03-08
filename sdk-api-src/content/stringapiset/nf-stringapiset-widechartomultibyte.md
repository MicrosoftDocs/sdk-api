---
UID: NF:stringapiset.WideCharToMultiByte
title: WideCharToMultiByte function (stringapiset.h)
description: Maps a UTF-16 (wide character) string to a new character string.
helpviewer_keywords: ["CP_ACP","CP_MACCP","CP_OEMCP","CP_SYMBOL","CP_THREAD_ACP","CP_UTF7","CP_UTF8","WC_COMPOSITECHECK","WC_ERR_INVALID_CHARS","WC_NO_BEST_FIT_CHARS","WideCharToMultiByte","WideCharToMultiByte function [Internationalization for Windows Applications]","_win32_WideCharToMultiByte","intl.widechartomultibyte","stringapiset/WideCharToMultiByte"]
old-location: intl\widechartomultibyte.htm
tech.root: Intl
ms.assetid: b8c13444-86ab-479c-ac04-9b184d9eebf6
ms.date: 02/05/2024
ms.keywords: CP_ACP, CP_MACCP, CP_OEMCP, CP_SYMBOL, CP_THREAD_ACP, CP_UTF7, CP_UTF8, WC_COMPOSITECHECK, WC_ERR_INVALID_CHARS, WC_NO_BEST_FIT_CHARS, WideCharToMultiByte, WideCharToMultiByte function [Internationalization for Windows Applications], _win32_WideCharToMultiByte, intl.widechartomultibyte, stringapiset/WideCharToMultiByte
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: snippet-project
f1_keywords:
 - WideCharToMultiByte
 - stringapiset/WideCharToMultiByte
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-String-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - vertdll.dll
api_name:
 - WideCharToMultiByte
---

# WideCharToMultiByte function

## -description

Maps a UTF-16 (wide character) string to a new character string. The new character string is not necessarily from a multibyte character set.

<div class="alert"><b>Caution</b>  Using the <b>WideCharToMultiByte</b> function incorrectly can compromise the security of your application. Calling this function can easily cause a buffer overrun because the size of the input buffer indicated by <i>lpWideCharStr</i> equals the number of characters in the Unicode string, while the size of the output buffer indicated by <i>lpMultiByteStr</i> equals the number of bytes. To avoid a buffer overrun, your application must specify a buffer size appropriate for the data type the buffer receives.

<p class="note">Data converted from UTF-16 to non-Unicode encodings is subject to data loss, because a code page might not be able to represent every character used in the specific Unicode data. For more information, see <a href="/windows/desktop/Intl/security-considerations--international-features">Security Considerations: International Features</a>.

</div>
<div> </div>

<div class="alert"><b>Note</b>  The ANSI code pages can be different on different computers, or can be changed for a single computer, leading to data corruption. For the most consistent results, applications should use Unicode, such as UTF-8 or UTF-16, instead of a specific code page, unless legacy standards or data formats prevent the use of Unicode. If using Unicode is not possible, applications should tag the data stream with the appropriate encoding name when protocols allow it. HTML and XML files allow tagging, but text files do not.</div>
<div> </div>

## -parameters

### -param CodePage [in]

Code page to use in performing the conversion. This parameter can be set to the value of any code page that is installed or available in the operating system. For a list of code pages, see <a href="/windows/desktop/Intl/code-page-identifiers">Code Page Identifiers</a>. Your application can also specify one of the values shown in the following table.

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
<b>Windows 2000:</b> Symbol code page (42).

</td>
</tr>
<tr>
<td width="40%"><a id="CP_THREAD_ACP"></a><a id="cp_thread_acp"></a><dl>
<dt><b>CP_THREAD_ACP</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows 2000:</b> The Windows ANSI code page for the current thread. 

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
UTF-7. Use this value only when forced by a 7-bit transport mechanism. Use of UTF-8 is preferred. With this value set, <i>lpDefaultChar</i> and <i>lpUsedDefaultChar</i> must be set to <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CP_UTF8"></a><a id="cp_utf8"></a><dl>
<dt><b>CP_UTF8</b></dt>
</dl>
</td>
<td width="60%">
UTF-8. With this value set, <i>lpDefaultChar</i> and <i>lpUsedDefaultChar</i> must be set to <b>NULL</b>.

</td>
</tr>
</table>

### -param dwFlags [in]

Flags indicating the conversion type. The application can specify a combination of the following values. The function performs more quickly when none of these flags is set. The application should specify WC_NO_BEST_FIT_CHARS and WC_COMPOSITECHECK with the specific value WC_DEFAULTCHAR to retrieve all possible conversion results. If all three values are not provided, some results will be missing.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WC_COMPOSITECHECK"></a><a id="wc_compositecheck"></a><dl>
<dt><b>WC_COMPOSITECHECK</b></dt>
</dl>
</td>
<td width="60%">
Convert composite characters, consisting of a base character and a nonspacing character, each with different character values. Translate these characters to precomposed characters, which have a single character value for a base-nonspacing character combination. For example, in the character è, the e is the base character and the accent grave mark is the nonspacing character.<div class="alert"><b>Note</b>  Windows normally represents Unicode strings with precomposed data, making the use of the WC_COMPOSITECHECK flag unnecessary.</div>
<div> </div>

Your application can combine WC_COMPOSITECHECK with any one of the following flags, with the default being WC_SEPCHARS. These flags determine the behavior of the function when no precomposed mapping for a base-nonspacing character combination in a Unicode string is available. If none of these flags is supplied, the function behaves as if the WC_SEPCHARS flag is set. For more information, see WC_COMPOSITECHECK and related flags in the [Remarks](#remarks) section.

<table>
<tr>
<td>WC_DEFAULTCHAR</td>
<td>Replace exceptions with the default character during conversion.</td>
</tr>
<tr>
<td>WC_DISCARDNS</td>
<td>Discard nonspacing characters during conversion.</td>
</tr>
<tr>
<td>WC_SEPCHARS</td>
<td>Default. Generate separate characters during conversion.</td>
</tr>
</table>
 

</td>
</tr>
<tr>
<td width="40%"><a id="WC_ERR_INVALID_CHARS"></a><a id="wc_err_invalid_chars"></a><dl>
<dt><b>WC_ERR_INVALID_CHARS</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista and later:</b> Fail (by returning 0 and setting the last-error code to  ERROR_NO_UNICODE_TRANSLATION) if an invalid input character is encountered. You can retrieve the last-error code with a call to <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. If this flag is not set, the function replaces illegal sequences with U+FFFD (encoded as appropriate for the specified codepage) and succeeds by returning the length of the converted string. Note that this flag only applies when <i>CodePage</i> is specified as CP_UTF8 or 54936. It cannot be used with other code page values.

</td>
</tr>
<tr>
<td width="40%"><a id="WC_NO_BEST_FIT_CHARS"></a><a id="wc_no_best_fit_chars"></a><dl>
<dt><b>WC_NO_BEST_FIT_CHARS</b></dt>
</dl>
</td>
<td width="60%">
Translate any Unicode characters that do not translate directly to multibyte equivalents to the default character specified by <i>lpDefaultChar</i>. In other words, if translating from Unicode to multibyte and back to Unicode again does not yield the same Unicode character, the function uses the default character. This flag can be used by itself or in combination with the other defined flags.

For strings that require validation, such as file, resource, and user names, the application should always use the WC_NO_BEST_FIT_CHARS flag. This flag prevents the function from mapping characters to characters that appear similar but have very different semantics. In some cases, the semantic change can be extreme. For example, the symbol for "∞" (infinity) maps to 8 (eight) in some code pages.

</td>
</tr>
</table>
 

For the code pages listed below, <i>dwFlags</i> must be 0. Otherwise, the function fails with ERROR_INVALID_FLAGS.

<ul>
<li>50220</li>
<li>50221</li>
<li>50222</li>
<li>50225</li>
<li>50227</li>
<li>50229</li>
<li>57002 through 57011</li>
<li>65000 (UTF-7)</li>
<li>42 (Symbol)</li>
</ul>
<div class="alert"><b>Note</b>  For the code page 65001 (UTF-8) or the code page 54936 (GB18030, Windows Vista and later), <i>dwFlags</i> must be set to either 0 or WC_ERR_INVALID_CHARS. Otherwise, the function fails with ERROR_INVALID_FLAGS.</div>
<div> </div>

### -param lpWideCharStr [in]

Pointer to the Unicode string to convert.

### -param cchWideChar [in]

Size, in characters, of the string indicated by <i>lpWideCharStr</i>. Alternatively, this parameter can be set to -1 if the string is null-terminated. If <i>cchWideChar</i> is set to 0, the function fails.

If this parameter is -1, the function processes the entire input string, including the terminating null character. Therefore, the resulting character string has a terminating null character, and the length returned by the function includes this character.

If this parameter is set to a positive integer, the function processes exactly the specified number of characters. If the provided size does not include a terminating null character, the resulting character string is not null-terminated, and the returned length does not include this character.

### -param lpMultiByteStr [out, optional]

Pointer to a buffer that receives the converted string.

### -param cbMultiByte [in]

Size, in bytes, of the buffer indicated by <i>lpMultiByteStr</i>. If this value is 0, the function returns the required buffer size, in bytes, including any terminating null character, and makes no use of the <i>lpMultiByteStr</i> buffer.

### -param lpDefaultChar [in, optional]

Pointer to the character to use if a character cannot be represented in the specified code page. The application sets this parameter to <b>NULL</b> if the function is to use a system default value. To obtain the system default character, the application can call the <a href="/windows/desktop/api/winnls/nf-winnls-getcpinfo">GetCPInfo</a> or <a href="/windows/desktop/api/winnls/nf-winnls-getcpinfoexa">GetCPInfoEx</a> function.

For the CP_UTF7 and CP_UTF8 settings for <i>CodePage</i>, this parameter must be set to <b>NULL</b>. Otherwise, the function fails with ERROR_INVALID_PARAMETER.

### -param lpUsedDefaultChar [out, optional]

Pointer to a flag that indicates if the function has used a default character in the conversion. The flag is set to <b>TRUE</b> if one or more characters in the source string cannot be represented in the specified code page. Otherwise, the flag is set to <b>FALSE</b>. This parameter can be set to <b>NULL</b>.

For the CP_UTF7 and CP_UTF8 settings for <i>CodePage</i>, this parameter must be set to <b>NULL</b>. Otherwise, the function fails with ERROR_INVALID_PARAMETER.

## -returns

If successful, returns the number of bytes written to the buffer pointed to by <i>lpMultiByteStr</i>. If the function succeeds and <i>cbMultiByte</i> is 0, the return value is the required size, in bytes, for the buffer indicated by <i>lpMultiByteStr</i>. Also see <i>dwFlags</i> for info about how the WC_ERR_INVALID_CHARS flag affects the return value when invalid sequences are input.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid. </li>
<li>ERROR_NO_UNICODE_TRANSLATION. Invalid Unicode was found in a string.</li>
</ul>

## -remarks

The <i>lpMultiByteStr</i> and <i>lpWideCharStr</i> pointers must not be the same. If they are the same, the function fails, and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INVALID_PARAMETER.

<b>WideCharToMultiByte</b> does not null-terminate an output string if the input string length is explicitly specified without a terminating null character. To null-terminate an output string for this function, the application should pass in -1 or explicitly count the terminating null character for the input string.

If <i>cbMultiByte</i> is less than <i>cchWideChar</i>, this function writes the number of characters specified by <i>cbMultiByte</i> to the buffer indicated by <i>lpMultiByteStr</i>. However, if <i>CodePage</i> is set to CP_SYMBOL and <i>cbMultiByte</i> is less than <i>cchWideChar,</i> the function writes no characters to <i>lpMultiByteStr</i>.

The <b>WideCharToMultiByte</b> function operates most efficiently when both <i>lpDefaultChar</i> and <i>lpUsedDefaultChar</i> are set to <b>NULL</b>. The following table shows the behavior of the function for the four possible combinations of these parameters.

<table>
<tr>
<th><i>lpDefaultChar</i></th>
<th><i>lpUsedDefaultChar</i></th>
<th>Result</th>
</tr>
<tr>
<td><b>NULL</b></td>
<td><b>NULL</b></td>
<td>No default checking. These parameter settings are the most efficient ones for use with this function.</td>
</tr>
<tr>
<td>Non-null character</td>
<td><b>NULL</b></td>
<td>Uses the specified default character, but does not set <i>lpUsedDefaultChar</i>.</td>
</tr>
<tr>
<td><b>NULL</b></td>
<td>Non-null character</td>
<td>Uses the system default character and sets <i>lpUsedDefaultChar</i> if necessary.</td>
</tr>
<tr>
<td>Non-null character</td>
<td>Non-null character</td>
<td>Uses the specified default character and sets <i>lpUsedDefaultChar</i> if necessary.</td>
</tr>
</table>

Starting with Windows Vista, this function fully conforms with the Unicode 4.1 specification for UTF-8 and UTF-16. The function used on earlier operating systems encodes or decodes lone <a href="/windows/desktop/Intl/surrogates-and-supplementary-characters">surrogate</a> halves or mismatched surrogate pairs. Code written in earlier versions of Windows that rely on this behavior to encode random non-text binary data might run into problems. However, code that uses this function to produce valid UTF-8 strings will behave the same way as on earlier Windows operating systems.

<b>Starting with Windows 8: </b><b>WideCharToMultiByte</b>  is declared in Stringapiset.h. Before Windows 8, it was declared in Winnls.h.

<h3><a id="wc_compositecheck_and_related_flags"></a><a id="WC_COMPOSITECHECK_AND_RELATED_FLAGS"></a>WC_COMPOSITECHECK and related flags</h3>
As discussed in <a href="/windows/desktop/Intl/using-unicode-normalization-to-represent-strings">Using Unicode Normalization to Represent Strings</a>, Unicode allows multiple representations of the same string (interpreted linguistically). For example, Capital A with dieresis (umlaut) can be represented either precomposed as a single Unicode code point "Ä" (U+00C4) or decomposed as the combination of Capital A and the combining dieresis character ("A" + "¨", that is U+0041 U+0308). However, most code pages provide only composed characters.

The WC_COMPOSITECHECK flag causes the <b>WideCharToMultiByte</b> function to test for decomposed Unicode characters and attempts to compose them before converting them to the requested code page. This flag is only available for conversion to <a href="/windows/desktop/Intl/single-byte-character-sets">single byte (SBCS)</a> or <a href="/windows/desktop/Intl/double-byte-character-sets">double byte (DBCS)</a> code pages (code pages &lt; 50000, excluding code page 42). If your application needs to convert decomposed Unicode data to single byte or double byte code pages, this flag might be useful. However, not all characters can be converted this way and it is more reliable to save and store such data as Unicode.

When an application is using WC_COMPOSITECHECK, some character combinations might remain incomplete or might have additional nonspacing characters left over. For example, A + ¨ + ¨ combines to Ä + ¨. Using the WC_DISCARDNS flag causes the function to discard additional nonspacing characters. Using the WC_DEFAULTCHAR flag causes the function to use the default replacement character (typically "?") instead. Using the WC_SEPCHARS flag causes the function to attempt to convert each additional nonspacing character to the target code page. Usually this flag also causes the use of the replacement character ("?"). However, for code page 1258 (Vietnamese) and 20269, nonspacing characters exist and can be used. The conversions for these code pages are not perfect. Some combinations do not convert correctly to code page 1258, and WC_COMPOSITECHECK corrupts data in code page 20269. As mentioned earlier, it is more reliable to design your application to save and store such data as Unicode.

## Examples

```cpp
ISDSC_STATUS DiscpUnicodeToAnsiSize(
    IN __in PWCHAR UnicodeString,
    OUT ULONG *AnsiSizeInBytes
    )
/*++
Routine Description:
    This routine will return the length needed to represent the unicode
    string as ANSI
Arguments:
    UnicodeString is the unicode string whose ansi length is returned
    *AnsiSizeInBytes is number of bytes needed to represent unicode
        string as ANSI
Return Value:
    ERROR_SUCCESS or error code
--*/
{
    _try
    {
        *AnsiSizeInBytes = WideCharToMultiByte(CP_ACP,
                                               0,
                                               UnicodeString,
                                               -1,
                                               NULL,
                                               0, NULL, NULL);
    } _except(EXCEPTION_EXECUTE_HANDLER) {
        return(ERROR_NOACCESS);
    }
    return((*AnsiSizeInBytes == 0) ? GetLastError() : ERROR_SUCCESS);
}
```

## -see-also

[MultiByteToWideChar](nf-stringapiset-multibytetowidechar.md)

[Unicode and Character Set Functions](/windows/win32/Intl/unicode-and-character-set-functions)

[Unicode and Character Sets](/windows/win32/Intl/unicode-and-character-sets)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
