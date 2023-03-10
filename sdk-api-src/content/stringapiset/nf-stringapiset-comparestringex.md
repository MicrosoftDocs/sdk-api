---
UID: NF:stringapiset.CompareStringEx
title: CompareStringEx function (stringapiset.h)
description: Compares two Unicode (wide character) strings, for a locale specified by name.Caution  Using CompareStringEx incorrectly can compromise the security of your application.
helpviewer_keywords: ["CompareStringEx","CompareStringEx function [Internationalization for Windows Applications]","LINGUISTIC_IGNORECASE","LINGUISTIC_IGNOREDIACRITIC","NORM_IGNORECASE","NORM_IGNOREKANATYPE","NORM_IGNORENONSPACE","NORM_IGNORESYMBOLS","NORM_IGNOREWIDTH","NORM_LINGUISTIC_CASING","SORT_DIGITSASNUMBERS","SORT_STRINGSORT","_win32_CompareStringEx","_win32_CompareStringEx_cpp","intl.comparestringex","stringapiset/CompareStringEx","winui._win32_CompareStringEx"]
old-location: intl\comparestringex.htm
tech.root: Intl
ms.assetid: 264c67b6-848d-48ef-9bfa-4990bfa2fbf5
ms.date: 12/05/2018
ms.keywords: CompareStringEx, CompareStringEx function [Internationalization for Windows Applications], LINGUISTIC_IGNORECASE, LINGUISTIC_IGNOREDIACRITIC, NORM_IGNORECASE, NORM_IGNOREKANATYPE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREWIDTH, NORM_LINGUISTIC_CASING, SORT_DIGITSASNUMBERS, SORT_STRINGSORT, _win32_CompareStringEx, _win32_CompareStringEx_cpp, intl.comparestringex, stringapiset/CompareStringEx, winui._win32_CompareStringEx
req.header: stringapiset.h
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
 - CompareStringEx
 - stringapiset/CompareStringEx
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
api_name:
 - CompareStringEx
---

# CompareStringEx function


## -description

Compares two Unicode (wide character) strings, for a <a href="/windows/desktop/Intl/locales-and-languages">locale</a> specified by name.
<div class="alert"><b>Caution</b>  Using <b>CompareStringEx</b> incorrectly can compromise the security of your application. Strings that are not compared correctly can produce invalid input. Test strings to make sure they are valid before using them, and provide error handlers. For more information, see <a href="/windows/desktop/Intl/security-considerations--international-features">Security Considerations: International Features</a>.</div><div> </div><div class="alert"><b>Note</b>  The application should call this function in preference to <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw">CompareString</a> if designed to run only on Windows Vista and later.</div><div> </div>

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

### -param dwCmpFlags [in]

Flags that indicate how the function compares the two strings. By default, these flags are not set. This parameter can specify a combination of any of the following values, or it can be set to 0 to obtain the default behavior.

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

<div class="alert"><b>Note</b>  NORM_IGNORECASE ignores any tertiary distinction, whether it is actually linguistic case or not. For example, in Arabic and Indic scripts, this distinguishes alternate forms of a character, but the differences do not correspond to linguistic case. LINGUISTIC_IGNORECASE causes the function to ignore only actual linguistic casing, instead of ignoring the third sorting weight.</div>
<div> </div>
<div class="alert"><b>Note</b>  With this flag set, the function ignores the distinction between the wide and narrow forms of the CJK compatibility characters.</div>
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
<td width="40%"><a id="NORM_IGNORENONSPACE"></a><a id="norm_ignorenonspace"></a><dl>
<dt><b>NORM_IGNORENONSPACE</b></dt>
</dl>
</td>
<td width="60%">
Ignore nonspacing characters. For many scripts (notably Latin scripts), NORM_IGNORENONSPACE coincides with LINGUISTIC_IGNOREDIACRITIC.

<div class="alert"><b>Note</b>  NORM_IGNORENONSPACE ignores any secondary distinction, whether it is a diacritic or not. Scripts for Korean, Japanese, Chinese, and Indic languages, among others, use this distinction for purposes other than diacritics. LINGUISTIC_IGNOREDIACRITIC causes the function to ignore only actual diacritics, instead of ignoring the second sorting weight.</div>
<div> </div>
<div class="alert"><b>Note</b>  NORM_IGNORENONSPACE only has an effect for locales in which accented characters are sorted in a second pass from main characters. Normally all characters in the string are first compared without regard to accents and, if the strings are equal, a second pass over the strings is performed to compare accents. This flag causes the second pass to not be performed. For locales that sort accented characters in the first pass, this flag has no effect.</div>
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
Use the default linguistic rules for casing, instead of file system rules. Note that most scenarios for <b>CompareStringEx</b> use this flag. This flag does not have to be used when your application calls <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringordinal">CompareStringOrdinal</a>.

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

### -param lpString1 [in]

Pointer to the first string to compare.

### -param cchCount1 [in]

Length of the string indicated by <i>lpString1</i>, excluding the terminating null character. The application can supply a negative value if the string is null-terminated. In this case, the function determines the length automatically.

### -param lpString2 [in]

Pointer to the second string to compare.

### -param cchCount2 [in]

Length of the string indicated by <i>lpString2</i>, excluding the terminating null character. The application can supply a negative value if the string is null-terminated. In this case, the function determines the length automatically.

### -param lpVersionInformation [in, optional]

Pointer to an <a href="/windows/desktop/api/winnls/ns-winnls-nlsversioninfoex">NLSVERSIONINFOEX</a> structure that contains the version information about the relevant NLS capability; usually retrieved from <a href="/windows/desktop/api/winnls/nf-winnls-getnlsversionex">GetNLSVersionEx</a>.

<b>Windows Vista, Windows 7:</b> Reserved; must set to <b>NULL</b>.

### -param lpReserved [in, optional]

Reserved; must set to <b>NULL</b>.

### -param lParam [in, optional]

Reserved; must be set to 0.

## -returns

Returns one of the following values if successful. To maintain the C runtime convention of comparing strings, the value 2 can be subtracted from a nonzero return value. Then, the meaning of &lt;0, ==0, and &gt;0 is consistent with the C runtime.

<ul>
<li>CSTR_LESS_THAN. The string indicated by <i>lpString1</i> is less in lexical value than the string indicated by <i>lpString2</i>.</li>
<li>CSTR_EQUAL. The string indicated by <i>lpString1</i> is equivalent in lexical value to the string indicated by <i>lpString2</i>. The two strings are equivalent for sorting purposes, although not necessarily identical.</li>
<li>CSTR_GREATER_THAN. The string indicated by <i>lpString1</i> is greater in lexical value than the string indicated by <i>lpString2</i>.</li>
</ul>
The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were invalid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid. </li>
</ul>

## -remarks

Both <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw">CompareString</a> and <b>CompareStringEx</b> are optimized to run at the highest speed when <i>dwCmpFlags</i> is set to 0 or NORM_IGNORECASE, <i>cchCount1</i> and <i>cchCount2</i> are set to -1, and the locale does not support any linguistic compressions, as when traditional Spanish sorting treats "ch" as a single character.

Both <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw">CompareString</a> and <b>CompareStringEx</b> ignore Arabic kashidas during the comparison. Thus, if two strings are identical except for the presence of kashidas, the function returns CSTR_EQUAL.
      

When the application uses the NORM_IGNORENONSPACE and NORM_IGNORECASE flags with the sorting function, the flags can sometimes interfere with string comparisons. This situation might result for a locale that does not support non-spacing characters or case, but uses equivalent weight levels to handle other important operations. In such cases, your application should use the LINGUISTIC_IGNOREDIACRITIC and LINGUISTIC_IGNORECASE flags. These flags provide linguistically appropriate results for sorting code points that use case and diacritic marks, and have no impact on other code points.

<b>Beginning in Windows Vista: </b> Both <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw">CompareString</a> and <b>CompareStringEx</b> can retrieve data from <a href="/windows/desktop/Intl/custom-locales">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.
      

<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="/uwp/api/Windows.Globalization">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="/windows/desktop/api/winnls/nf-winnls-resolvelocalename">ResolveLocaleName</a>.

<b>Beginning in Windows 8: </b><b>CompareStringEx</b>  is declared in Stringapiset.h. Before Windows 8, it was declared in Winnls.h.

<div class="alert"><b>Note</b>  The behavior of sorting can change between Windows releases. For example, there may be new Unicode code points created. Use <a href="/windows/desktop/api/winnls/nf-winnls-getnlsversionex">GetNlsVersionEx</a> to discover if the sort version has changed.</div>
<div> </div>

#### Examples

An example showing the use of this function can be found in <a href="/windows/desktop/Intl/nls--name-based-apis-sample">NLS: Name-based APIs Sample</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw">CompareString</a>



<a href="/windows/desktop/Intl/custom-locales">Custom Locales</a>



<a href="/windows/desktop/Intl/handling-sorting-in-your-applications">Handling Sorting in Your Applications</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>



<a href="/windows/desktop/Intl/security-considerations--international-features">Security Considerations: International Features</a>



<a href="/windows/desktop/Intl/using-unicode-normalization-to-represent-strings">Using Unicode Normalization to Represent Strings</a>