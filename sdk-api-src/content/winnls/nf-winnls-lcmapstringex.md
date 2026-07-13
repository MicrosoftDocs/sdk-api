---
UID: NF:winnls.LCMapStringEx
title: LCMapStringEx function (winnls.h)
description: For a locale specified by name, maps an input character string to another using a specified transformation, or generates a sort key for the input string.Note  The application should call this function in preference to LCMapString if designed to run only on Windows Vista and later.
helpviewer_keywords: ["LCMAP_BYTEREV","LCMAP_FULLWIDTH","LCMAP_HALFWIDTH","LCMAP_HIRAGANA","LCMAP_KATAKANA","LCMAP_LINGUISTIC_CASING","LCMAP_LOWERCASE","LCMAP_SIMPLIFIED_CHINESE","LCMAP_SORTKEY","LCMAP_TITLECASE","LCMAP_TRADITIONAL_CHINESE","LCMAP_UPPERCASE","LCMapStringEx","LCMapStringEx function [Internationalization for Windows Applications]","LINGUISTIC_IGNORECASE","LINGUISTIC_IGNOREDIACRITIC","NORM_IGNORECASE","NORM_IGNOREKANATYPE","NORM_IGNORENONSPACE","NORM_IGNORESYMBOLS","NORM_IGNOREWIDTH","NORM_LINGUISTIC_CASING","SORT_DIGITSASNUMBERS","SORT_STRINGSORT","_win32_LCMapStringEx","intl.lcmapstringex","winnls/LCMapStringEx"]
old-location: intl\lcmapstringex.htm
tech.root: Intl
ms.assetid: 725e4e75-c328-40bc-a594-20a295a487c6
ms.date: 07/22/2019
ms.keywords: LCMAP_BYTEREV, LCMAP_FULLWIDTH, LCMAP_HALFWIDTH, LCMAP_HIRAGANA, LCMAP_KATAKANA, LCMAP_LINGUISTIC_CASING, LCMAP_LOWERCASE, LCMAP_SIMPLIFIED_CHINESE, LCMAP_SORTKEY, LCMAP_TITLECASE, LCMAP_TRADITIONAL_CHINESE, LCMAP_UPPERCASE, LCMapStringEx, LCMapStringEx function [Internationalization for Windows Applications], LINGUISTIC_IGNORECASE, LINGUISTIC_IGNOREDIACRITIC, NORM_IGNORECASE, NORM_IGNOREKANATYPE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREWIDTH, NORM_LINGUISTIC_CASING, SORT_DIGITSASNUMBERS, SORT_STRINGSORT, _win32_LCMapStringEx, intl.lcmapstringex, winnls/LCMapStringEx
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
ms.custom: 19H1
f1_keywords:
 - LCMapStringEx
 - winnls/LCMapStringEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-localization-l1-2-4.dll
 - api-ms-win-core-localization-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-Localization-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - LCMapStringEx
---

# LCMapStringEx function


## -description

For a locale specified by name, maps an input character string to another using a specified transformation, or generates a sort key for the input string.<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="/windows/desktop/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> if designed to run only on Windows Vista and later.</div>
<div> </div>

## -parameters

### -param lpLocaleName [in, optional]

Pointer to a <a href="/windows/desktop/Intl/locale-names">locale name</a>, or one of the following predefined values. 

<ul>
<li>
<a href="/windows/desktop/Intl/locale-name-constants">LOCALE_NAME_INVARIANT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-name-constants">LOCALE_NAME_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-name-constants">LOCALE_NAME_USER_DEFAULT</a>
</li>
</ul>

### -param dwMapFlags [in]

Flag specifying the type of transformation to use during string mapping or the type of sort key to generate. This parameter can have the following values.

| Flag | Meaning |
| --- | --- |
| **LCMAP_BYTEREV**| Use byte reversal. For example, if the application passes in 0x3450 0x4822, the result is 0x5034 0x2248. |
| **LCMAP_FULLWIDTH** | Use Unicode (wide) characters where applicable. This flag and LCMAP_HALFWIDTH are mutually exclusive. With this flag, the mapping may use Normalization Form C even if an input character is already full-width. For example, the string "は゛" (which is already full-width) is normalized to "ば". See [Unicode normalization forms](http://www.unicode.org/reports/tr15/). |
|**LCMAP_HALFWIDTH** | Use narrow characters where applicable. This flag and LCMAP_FULLWIDTH are mutually exclusive. |
| **LCMAP_HIRAGANA** | Map all katakana characters to hiragana. This flag and LCMAP_KATAKANA are mutually exclusive. |
| **LCMAP_KATAKANA** | Map all hiragana characters to katakana. This flag and LCMAP_HIRAGANA are mutually exclusive. |
| **LCMAP_LINGUISTIC_CASING** | Use linguistic rules for casing, instead of file system rules (default). This flag is valid with LCMAP_LOWERCASE or LCMAP_UPPERCASE only. |
| **LCMAP_LOWERCASE** | For locales and scripts capable of handling uppercase and lowercase, map all characters to lowercase.
| **LCMAP_HASH** | Return a hash of the raw sort weights of a string.<br> <br>Strings that appear equivalent typically return the same hash (for example, "hello" and "HELLO" with LCMAP_IGNORECASE). However, some complex cases, such as East Asian languages, can have similar strings with identical weights that compare as equal but do not return the same hash.<br> <br>LCMAP_HASH requires that the output buffer be of size sizeof(int) |
| **LCMAP_SIMPLIFIED_CHINESE** | Map traditional Chinese characters to simplified Chinese characters. This flag and LCMAP_TRADITIONAL_CHINESE are mutually exclusive. |
| **LCMAP_SORTHANDLE** <br> **The use of a sort handle results in minimal performance improvements and is discouraged.** | Return a token representing the resolved sort parameters for the locale (like locale name), so future calls can pass <code>NULL</code> for the sort name and pass the previously queried sort handle as the last parameter (sortHandle) in subsequent calls to [CompareStringEx](../stringapiset/nf-stringapiset-comparestringex.md) or [LCMapStringEx](nf-winnls-lcmapstringex.md).<br> <br>LCMAP_SORTHANDLE requires that the output buffer be of size sizeof(lparam) |
| **LCMAP_SORTKEY** | Produce a normalized sort key. If the LCMAP_SORTKEY flag is not specified, the function performs string mapping. For details of sort key generation and string mapping, see the Remarks section. |
| **LCMAP_TITLECASE** | Windows 7:</b> Map all characters to title case, in which the first letter of each major word is capitalized. |
| **LCMAP_TRADITIONAL_CHINESE** | Map simplified Chinese characters to traditional Chinese characters. This flag and LCMAP_SIMPLIFIED_CHINESE are mutually exclusive. |
| **LCMAP_UPPERCASE** | For locales and scripts capable of handling uppercase and lowercase, map all characters to uppercase. |

The following flags can be used alone, with one another, or with the LCMAP_SORTKEY and/or LCMAP_BYTEREV flags. However, they cannot be combined with the other flags listed above.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NORM_IGNORENONSPACE"></a><a id="norm_ignorenonspace"></a><dl>
<dt><b>NORM_IGNORENONSPACE</b></dt>
</dl>
</td>
<td width="60%">
Ignore nonspacing characters. For many scripts (notably Latin scripts), NORM_IGNORENONSPACE coincides with LINGUISTIC_IGNOREDIACRITIC.

<div class="alert"><b>Note</b>  NORM_IGNORENONSPACE ignores any secondary distinction, whether it is a diacritic or not. Scripts for Korean, Japanese, Chinese, and Indic languages, among others, use this distinction for purposes other than diacritics. LINGUISTIC_IGNOREDIACRITIC causes the function to ignore only actual diacritics, instead of ignoring the second sorting weight.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="NORM_IGNORESYMBOLS"></a><a id="norm_ignoresymbols"></a><dl>
<dt><b>NORM_IGNORESYMBOLS</b></dt>
</dl>
</td>
<td width="60%">
Ignore symbols and punctuation.

</td>
</tr>
</table>
 

The flags listed below are used only with the LCMAP_SORTKEY flag.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LINGUISTIC_IGNORECASE"></a><a id="linguistic_ignorecase"></a><dl>
<dt><b>LINGUISTIC_IGNORECASE</b></dt>
</dl>
</td>
<td width="60%">
Ignore case, as linguistically appropriate.

</td>
</tr>
<tr>
<td width="40%"><a id="LINGUISTIC_IGNOREDIACRITIC"></a><a id="linguistic_ignorediacritic"></a><dl>
<dt><b>LINGUISTIC_IGNOREDIACRITIC</b></dt>
</dl>
</td>
<td width="60%">
Ignore nonspacing characters, as linguistically appropriate.

<div class="alert"><b>Note</b>  This flag does not always produce predictable results when used with decomposed characters, that is, characters in which a base character and one or more nonspacing characters each have distinct code point values.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="NORM_IGNORECASE"></a><a id="norm_ignorecase"></a><dl>
<dt><b>NORM_IGNORECASE</b></dt>
</dl>
</td>
<td width="60%">
Ignore case. For many scripts (notably Latin scripts), NORM_IGNORECASE coincides with LINGUISTIC_IGNORECASE.

<div class="alert"><b>Note</b>  NORM_IGNORECASE ignores any tertiary distinction, whether it is actually linguistic case or not. For example, in Arabic and Indic scripts, this flag distinguishes alternate forms of a character, but the differences do not correspond to linguistic case. LINGUISTIC_IGNORECASE causes the function to ignore only actual linguistic casing, instead of ignoring the third sorting weight.</div>
<div> </div>
<div class="alert"><b>Note</b>  For double-byte character set (DBCS) locales, NORM_IGNORECASE has an effect on all Unicode characters as well as narrow (one-byte) characters, including Greek and Cyrillic characters.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="NORM_IGNOREKANATYPE"></a><a id="norm_ignorekanatype"></a><dl>
<dt><b>NORM_IGNOREKANATYPE</b></dt>
</dl>
</td>
<td width="60%">
Do not differentiate between hiragana and katakana characters. Corresponding hiragana and katakana characters compare as equal.

</td>
</tr>
<tr>
<td width="40%"><a id="NORM_IGNOREWIDTH"></a><a id="norm_ignorewidth"></a><dl>
<dt><b>NORM_IGNOREWIDTH</b></dt>
</dl>
</td>
<td width="60%">
Ignore the difference between half-width and full-width characters, for example, C a t == cat. The full-width form is a formatting distinction used in Chinese and Japanese scripts.

</td>
</tr>
<tr>
<td width="40%"><a id="NORM_LINGUISTIC_CASING"></a><a id="norm_linguistic_casing"></a><dl>
<dt><b>NORM_LINGUISTIC_CASING</b></dt>
</dl>
</td>
<td width="60%">
Use linguistic rules for casing, instead of file system rules (default).

</td>
</tr>
<tr>
<td width="40%"><a id="SORT_DIGITSASNUMBERS"></a><a id="sort_digitsasnumbers"></a><dl>
<dt><b>SORT_DIGITSASNUMBERS</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows 7:</b> Treat digits as numbers during sorting, for example, sort "2" before "10".

</td>
</tr>
<tr>
<td width="40%"><a id="SORT_STRINGSORT"></a><a id="sort_stringsort"></a><dl>
<dt><b>SORT_STRINGSORT</b></dt>
</dl>
</td>
<td width="60%">
Treat punctuation the same as symbols.

</td>
</tr>
</table>

### -param lpSrcStr [in]

Pointer to a source string that the function maps or uses for sort key generation. This string cannot have a size of 0.

### -param cchSrc [in]

Size, in characters, of the source string indicated by <i>lpSrcStr</i>. The size of the source string can include the terminating null character, but does not have to. If the terminating null character is included, the mapping behavior of the function is not greatly affected because the terminating null character is considered to be unsortable and always maps to itself.

The application can set this parameter to any negative value to specify that the source string is null-terminated. In this case, if <b>LCMapStringEx</b> is being used in its string-mapping mode, the function calculates the string length itself, and null-terminates the mapped string indicated by <i>lpDestStr</i>.

The application cannot set this parameter to 0.

### -param lpDestStr [out, optional]

Pointer to a buffer in which this function retrieves the mapped string or a sort key.

If the application is using the function to generate a sort key (LCMAP_SORTKEY):

- The sort key is stored in the buffer and treated as an opaque array of bytes. The stored values can include embedded 0 bytes at any position.
- The destination string can contain an odd number of bytes. The LCMAP_BYTEREV flag only reverses an even number of bytes. The last byte (odd-positioned) in the sort key is not reversed.

If the caller explicitly requests a subset of the string, the destination string does not include a terminating null character unless the caller specified it in *cchDest*.

If this function fails, the destination buffer might contain either partial results or no results at all. In this case, all results should be considered invalid.

> [!NOTE]
> When setting LCMAP_UPPERCASE or LCMAP_LOWERCASE, the destination string can use the same buffer as the source string. However, this is strongly discouraged, as some conditions may cause the returned cased string to be a different length.

### -param cchDest [in]

Size, in characters, of the destination string indicated by <i>lpDestStr</i>. If the application is using the function for string mapping, it supplies a character count for this parameter. If space for a terminating null character is included in <i>cchSrc</i>, <i>cchDest</i> must also include space for a terminating null character.

If the application is using the function to generate a sort key, it supplies a byte count for the size. This byte count must include space for the sort key 0x00 terminator.

The application can set <i>cchDest</i> to 0. In this case, the function does not use the <i>lpDestStr</i> parameter and returns the required buffer size for the mapped string or sort key.

### -param lpVersionInformation [in, optional]

Pointer to an <a href="/windows/desktop/api/winnls/ns-winnls-nlsversioninfoex">NLSVERSIONINFOEX</a> structure that contains the version information about the relevant NLS capability; usually retrieved from <a href="/windows/desktop/api/winnls/nf-winnls-getnlsversionex">GetNLSVersionEx</a>.

**Windows Vista, Windows 7:** Reserved; must set to NULL.

### -param lpReserved [in, optional]

Reserved; must be NULL.

### -param sortHandle [in, optional]

Reserved; must be 0.

> [!NOTE]
> [CompareStringEx](../stringapiset/nf-stringapiset-comparestringex.md) and [LCMapStringEx](nf-winnls-lcmapstringex.md) can specify a sort handle (if the locale name is null).  This use is discouraged for most apps.

## -returns

If the function succeeds when used for string mapping, it returns the number of characters in the translated string (see *cchSrc* and *cchDest* for more details).

If the function succeeds when used for generating a sort key, it returns the number of bytes in the sort key.

This function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

The application can use <a href="/windows/desktop/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> or <b>LCMapStringEx</b> to generate a sort key. To do this, the application specifies  LCMAP_SORTKEY for the <i>dwMapFlags</i> parameter. For more information, see <a href="/windows/desktop/Intl/handling-sorting-in-your-applications">Handling Sorting in Your Applications</a>.

> [!NOTE]
> Sort keys are opaque byte streams. Callers should treat them as a byte array of the length returned by the API and not rely on any internal structure that may appear to be present. Zero, one or more of the bytes in the returned sort key could be 0. Absence or presence of a zero byte should not be expected.

Another way for your application to use <a href="/windows/desktop/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> or <b>LCMapStringEx</b> is in mapping strings. In this case, the application does not specify LCMAP_SORTKEY for the <i>dwMapFlags</i> parameter, but supplies some other combination of flags. For more information, see <a href="/windows/desktop/Intl/handling-sorting-in-your-applications">Handling Sorting in Your Applications</a>.

<b>Beginning in Windows Vista:</b> This function can handle data from <a href="/windows/desktop/Intl/custom-locales">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.

<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="/uwp/api/Windows.Globalization">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="/windows/desktop/api/winnls/nf-winnls-resolvelocalename">ResolveLocaleName</a>.

## -see-also

<a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw">CompareString</a>

<a href="/windows/desktop/api/winnls/nf-winnls-findnlsstringex">FindNLSStringEx</a>

<a href="/windows/desktop/api/winnls/nf-winnls-getnlsversionex">GetNLSVersionEx</a>

<a href="/windows/desktop/Intl/handling-sorting-in-your-applications">Handling Sorting in Your Applications</a>

<a href="/windows/desktop/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>

<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>

<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
