---
UID: NF:winnls.FindNLSStringEx
title: FindNLSStringEx function (winnls.h)
description: Locates a Unicode string (wide characters) or its equivalent in another Unicode string for a locale specified by name.Caution  Because strings with very different binary representations can compare as identical, this function can raise certain security concerns. For more information, see the discussion of comparison functions in Security Considerations:\_International Features.
helpviewer_keywords: ["FIND_ENDSWITH","FIND_FROMEND","FIND_FROMSTART","FIND_STARTSWITH","FindNLSStringEx","FindNLSStringEx function [Internationalization for Windows Applications]","LINGUISTIC_IGNORECASE","LINGUISTIC_IGNOREDIACRITIC","NORM_IGNORECASE","NORM_IGNOREKANATYPE","NORM_IGNORENONSPACE","NORM_IGNORESYMBOLS","NORM_IGNOREWIDTH","NORM_LINGUISTIC_CASING","_win32_FindNLSStringEx","intl.findnlsstringex","winnls/FindNLSStringEx"]
old-location: intl\findnlsstringex.htm
tech.root: Intl
ms.assetid: 38339881-30d2-4f55-9fee-81916ab15135
ms.date: 12/05/2018
ms.keywords: FIND_ENDSWITH, FIND_FROMEND, FIND_FROMSTART, FIND_STARTSWITH, FindNLSStringEx, FindNLSStringEx function [Internationalization for Windows Applications], LINGUISTIC_IGNORECASE, LINGUISTIC_IGNOREDIACRITIC, NORM_IGNORECASE, NORM_IGNOREKANATYPE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREWIDTH, NORM_LINGUISTIC_CASING, _win32_FindNLSStringEx, intl.findnlsstringex, winnls/FindNLSStringEx
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
 - FindNLSStringEx
 - winnls/FindNLSStringEx
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
 - FindNLSStringEx
---

# FindNLSStringEx function


## -description

Locates a Unicode string (wide characters) or its equivalent in another Unicode string for a locale specified by name.
<div class="alert"><b>Caution</b>  Because strings with very different binary representations can compare as identical, this function can raise certain security concerns. For more information, see the discussion of comparison functions in <a href="/windows/desktop/Intl/security-considerations--international-features">Security Considerations: International Features</a>.</div><div> </div>

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

### -param dwFindNLSStringFlags [in]

Flags specifying details of the find operation. These flags are mutually exclusive, with FIND_FROMSTART being the default. The application can specify just one of the find flags with any of the filtering flags defined in the next table. If the application does not specify a flag, the function uses the default comparison for the specified locale. As discussed in <a href="/windows/desktop/Intl/handling-sorting-in-your-applications">Handling Sorting in Your Applications</a>, there is no binary comparison mode.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FIND_FROMSTART"></a><a id="find_fromstart"></a><dl>
<dt><b>FIND_FROMSTART</b></dt>
</dl>
</td>
<td width="60%">
Search the string, starting with the first character of the string.

</td>
</tr>
<tr>
<td width="40%"><a id="FIND_FROMEND"></a><a id="find_fromend"></a><dl>
<dt><b>FIND_FROMEND</b></dt>
</dl>
</td>
<td width="60%">
Search the string in the reverse direction, starting with the last character of the string.

</td>
</tr>
<tr>
<td width="40%"><a id="FIND_STARTSWITH"></a><a id="find_startswith"></a><dl>
<dt><b>FIND_STARTSWITH</b></dt>
</dl>
</td>
<td width="60%">
Test to find out if the value specified by <i>lpStringValue</i> is the first value in the source string indicated by <i>lpStringSource</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="FIND_ENDSWITH"></a><a id="find_endswith"></a><dl>
<dt><b>FIND_ENDSWITH</b></dt>
</dl>
</td>
<td width="60%">
Test to find out if the value specified by <i>lpStringValue</i> is the last value in the source string indicated by <i>lpStringSource</i>.

</td>
</tr>
</table>
 

The application can use the filtering flags defined below in combination with a find flag.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LINGUISTIC_IGNORECASE"></a><a id="linguistic_ignorecase"></a><dl>
<dt><b>LINGUISTIC_IGNORECASE</b></dt>
</dl>
</td>
<td width="60%">
Ignore case in the search, as linguistically appropriate. For more information, see the Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="LINGUISTIC_IGNOREDIACRITIC"></a><a id="linguistic_ignorediacritic"></a><dl>
<dt><b>LINGUISTIC_IGNOREDIACRITIC</b></dt>
</dl>
</td>
<td width="60%">
Ignore diacritics, as linguistically appropriate. For more information, see the Remarks section.

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
Ignore case in the search. For more information, see the Remarks section.

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
<td width="40%"><a id="NORM_IGNORENONSPACE"></a><a id="norm_ignorenonspace"></a><dl>
<dt><b>NORM_IGNORENONSPACE</b></dt>
</dl>
</td>
<td width="60%">
Ignore nonspacing characters. For more information, see the Remarks section.

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
Use linguistic rules for casing, instead of file system rules (default). For more information, see the Remarks section.

</td>
</tr>
</table>

### -param lpStringSource [in]

Pointer to the source string, in which the function searches for the string specified by <i>lpStringValue</i>.

### -param cchSource [in]

Size, in characters excluding the terminating null character, of the string indicated by <i>lpStringSource</i>. The application cannot specify 0 or any negative number other than -1 for this parameter. The application specifies -1 if the source string is null-terminated and the function should calculate the size automatically.

### -param lpStringValue [in]

Pointer to the search string, for which the function searches in the source string.

### -param cchValue [in]

Size, in characters excluding the terminating null character, of the string indicated by <i>lpStringValue</i>. The application cannot specify 0 or any negative number other than -1 for this parameter. The application specifies -1 if the search string is null-terminated and the function should calculate the size automatically.

### -param pcchFound [out, optional]

Pointer to a buffer containing the length of the string that the function finds. The string can be either longer or shorter than the search string. If the function fails to find the search string, this parameter is not modified.

The function can retrieve <b>NULL</b> in this parameter. In this case, the function makes no indication if the length of the found string differs from the length of the source string. 

Note that the value of <i>pcchFound</i> is often identical to the value provided in <i>cchValue</i>, but can differ in the following cases:

<ul>
<li>The value provided in <i>cchValue</i> is negative.</li>
<li>The strings are equivalent, but have different lengths. For example, "A" plus "Combining Ring" (U+0041 U+030A) is equivalent to the "A Ring" (U+00c5).</li>
</ul>

### -param lpVersionInformation [in, optional]

Reserved; must be <b>NULL</b>.

### -param lpReserved [in, optional]

Reserved; must be <b>NULL</b>.

### -param sortHandle [in, optional]

Reserved; must be 0.

## -returns

Returns a 0-based index into the source string indicated by <i>lpStringSource</i> if successful. In combination with the value in <i>pcchFound</i>, this index provides the exact location of the entire found string in the source string. A return value of 0 is an error-free index into the source string, and the matching string is in the source string at offset 0.

The function returns -1 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
<li>ERROR_SUCCESS. The action completed successfully but yielded no results.</li>
</ul>

## -remarks

This function provides a variety of search options, including search direction, character equivalence filtering, and locale-specific filtering. Note that equivalence depends on the locale and flags specified in the call to the function. The filtering flags can alter the results of the search. For example, the potential matches increase when the function ignores case or diacritic marks when performing the search.

By default, this function maps the lowercase "i" to the uppercase "I", even when the <i>Locale</i> parameter specifies Turkish (Turkey) or Azerbaijani (Azerbaijan). To override this behavior for Turkish or Azerbaijani, the application should specify NORM_LINGUISTIC_CASING. If this flag is specified for the correct locale, "ı" (lowercase dotless I) is the lowercase form of "I" (uppercase dotless I) and "i" (lowercase dotted I) is the lowercase form of "ı" (uppercase dotted I).


For many scripts (notably Latin scripts), NORM_IGNORENONSPACE coincides with LINGUISTIC_IGNOREDIACRITIC and NORM_IGNORECASE coincides with LINGUISTIC_IGNORECASE, with the following exceptions:

<ul>
<li>NORM_IGNORENONSPACE ignores any secondary distinction, whether or not it is a diacritic. Scripts for Korean, Japanese, Chinese, Indic languages, and others use this distinction for purposes other than diacritics. LINGUISTIC_IGNOREDIACRITIC ignores only actual diacritics, instead of simply ignoring the second sorting weight.</li>
<li>NORM_IGNORECASE ignores any tertiary distinction, whether or not it is actually linguistic case. For example, in Arabic and Indic scripts, this flag distinguishes alternate forms of a character. However, the differences do not correspond to linguistic case. LINGUISTIC_IGNORECASE ignores only actual linguistic casing, instead of ignoring the third sorting weight.</li>
</ul>
In contrast to other NLS API functions, which return 0 for failure, this function returns -1 if it fails. On success, it returns a 0-based index. Use of this index helps the function avoid off-by-one errors and one-character buffer overruns.

This function is one of the few NLS functions that calls <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> even when it succeeds. It makes this call to clear the last error in a thread when it fails to match the search string. This clears the value returned by <b>GetLastError</b>.

<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="/uwp/api/Windows.Globalization">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="/windows/desktop/api/winnls/nf-winnls-resolvelocalename">ResolveLocaleName</a>.

## -see-also

<a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex">CompareStringEx</a>



<a href="/windows/desktop/api/winnls/nf-winnls-findnlsstring">FindNLSString</a>



<a href="/windows/desktop/Intl/handling-sorting-in-your-applications">Handling Sorting in Your Applications</a>



<a href="/windows/desktop/api/winnls/nf-winnls-lcmapstringex">LCMapStringEx</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>



<a href="/windows/desktop/Intl/security-considerations--international-features">Security Considerations: International Features</a>