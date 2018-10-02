---
UID: NF:winnls.LCMapStringEx
title: LCMapStringEx function
author: windows-sdk-content
description: For a locale specified by name, maps an input character string to another using a specified transformation, or generates a sort key for the input string.Note  The application should call this function in preference to LCMapString if designed to run only on Windows Vista and later.
old-location: intl\lcmapstringex.htm
tech.root: Intl
ms.assetid: 725e4e75-c328-40bc-a594-20a295a487c6
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: LCMAP_BYTEREV, LCMAP_FULLWIDTH, LCMAP_HALFWIDTH, LCMAP_HIRAGANA, LCMAP_KATAKANA, LCMAP_LINGUISTIC_CASING, LCMAP_LOWERCASE, LCMAP_SIMPLIFIED_CHINESE, LCMAP_SORTKEY, LCMAP_TITLECASE, LCMAP_TRADITIONAL_CHINESE, LCMAP_UPPERCASE, LCMapStringEx, LCMapStringEx function [Internationalization for Windows Applications], LINGUISTIC_IGNORECASE, LINGUISTIC_IGNOREDIACRITIC, NORM_IGNORECASE, NORM_IGNOREKANATYPE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREWIDTH, NORM_LINGUISTIC_CASING, SORT_DIGITSASNUMBERS, SORT_STRINGSORT, _win32_LCMapStringEx, intl.lcmapstringex, winnls/LCMapStringEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LCMapStringEx function


## -description


For a locale specified by name, maps an input character string to another using a specified transformation, or generates a sort key for the input string.<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="https://msdn.microsoft.com/84dda2cd-cbf9-45e9-b18c-7dea0b5bc991">LCMapString</a> if designed to run only on Windows Vista and later.</div>
<div> </div>



## -parameters




### -param lpLocaleName [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/221aae7b-3a7c-4995-ae78-50d97de436d8">locale name</a>, or one of the following predefined values. 

<ul>
<li>
<a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_INVARIANT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_USER_DEFAULT</a>
</li>
</ul>

### -param dwMapFlags [in]

Flag specifying the type of transformation to use during string mapping or the type of sort key to generate. This parameter can have the following values.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LCMAP_BYTEREV"></a><a id="lcmap_byterev"></a><dl>
<dt><b>LCMAP_BYTEREV</b></dt>
</dl>
</td>
<td width="60%">
Use byte reversal. For example, if the application passes in 0x3450 0x4822, the result is 0x5034 0x2248.

</td>
</tr>
<tr>
<td width="40%"><a id="LCMAP_FULLWIDTH"></a><a id="lcmap_fullwidth"></a><dl>
<dt><b>LCMAP_FULLWIDTH</b></dt>
</dl>
</td>
<td width="60%">
Use Unicode (wide) characters where applicable. This flag and LCMAP_HALFWIDTH are mutually exclusive. With this flag, the mapping may use Normalization Form C even if an input character is already full-width. For example, the string "は゛" (which is already full-width) is normalized to "ば". See <a href="http://unicode.org/reports/tr15">Unicode normalization forms</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="LCMAP_HALFWIDTH"></a><a id="lcmap_halfwidth"></a><dl>
<dt><b>LCMAP_HALFWIDTH</b></dt>
</dl>
</td>
<td width="60%">
Use narrow characters where applicable. This flag and LCMAP_FULLWIDTH are mutually exclusive.

</td>
</tr>
<tr>
<td width="40%"><a id="LCMAP_HIRAGANA"></a><a id="lcmap_hiragana"></a><dl>
<dt><b>LCMAP_HIRAGANA</b></dt>
</dl>
</td>
<td width="60%">
Map all katakana characters to hiragana. This flag and LCMAP_KATAKANA are mutually exclusive.

</td>
</tr>
<tr>
<td width="40%"><a id="LCMAP_KATAKANA"></a><a id="lcmap_katakana"></a><dl>
<dt><b>LCMAP_KATAKANA</b></dt>
</dl>
</td>
<td width="60%">
Map all hiragana characters to katakana. This flag and LCMAP_HIRAGANA are mutually exclusive.

</td>
</tr>
<tr>
<td width="40%"><a id="LCMAP_LINGUISTIC_CASING"></a><a id="lcmap_linguistic_casing"></a><dl>
<dt><b>LCMAP_LINGUISTIC_CASING</b></dt>
</dl>
</td>
<td width="60%">
Use linguistic rules for casing, instead of file system rules (default). This flag is valid with LCMAP_LOWERCASE or LCMAP_UPPERCASE only.

</td>
</tr>
<tr>
<td width="40%"><a id="LCMAP_LOWERCASE"></a><a id="lcmap_lowercase"></a><dl>
<dt><b>LCMAP_LOWERCASE</b></dt>
</dl>
</td>
<td width="60%">
For locales and scripts capable of handling uppercase and lowercase, map all characters to lowercase.

</td>
</tr>
<tr>
<td width="40%"><a id="LCMAP_SIMPLIFIED_CHINESE"></a><a id="lcmap_simplified_chinese"></a><dl>
<dt><b>LCMAP_SIMPLIFIED_CHINESE</b></dt>
</dl>
</td>
<td width="60%">
Map traditional Chinese characters to simplified Chinese characters. This flag and LCMAP_TRADITIONAL_CHINESE are mutually exclusive.

</td>
</tr>
<tr>
<td width="40%"><a id="LCMAP_SORTKEY"></a><a id="lcmap_sortkey"></a><dl>
<dt><b>LCMAP_SORTKEY</b></dt>
</dl>
</td>
<td width="60%">
Produce a normalized sort key. If the LCMAP_SORTKEY flag is not specified, the function performs string mapping. For details of sort key generation and string mapping, see the Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="LCMAP_TITLECASE"></a><a id="lcmap_titlecase"></a><dl>
<dt><b>LCMAP_TITLECASE</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows 7:</b> Map all characters to title case, in which the first letter of each major word is capitalized.

</td>
</tr>
<tr>
<td width="40%"><a id="LCMAP_TRADITIONAL_CHINESE"></a><a id="lcmap_traditional_chinese"></a><dl>
<dt><b>LCMAP_TRADITIONAL_CHINESE</b></dt>
</dl>
</td>
<td width="60%">
Map simplified Chinese characters to traditional Chinese characters. This flag and LCMAP_SIMPLIFIED_CHINESE are mutually exclusive.

</td>
</tr>
<tr>
<td width="40%"><a id="LCMAP_UPPERCASE"></a><a id="lcmap_uppercase"></a><dl>
<dt><b>LCMAP_UPPERCASE</b></dt>
</dl>
</td>
<td width="60%">
For locales and scripts capable of handling uppercase and lowercase, map all characters to uppercase.

</td>
</tr>
</table>
 

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

Pointer to a buffer in which this function retrieves the mapped string or sort key. If the application specifies LCMAP_SORTKEY, the function stores a sort key in the buffer as an opaque array of byte values that can include embedded 0 bytes.

<div class="alert"><b>Note</b>  If the function fails, the destination buffer might contain either partial results or no results at all. In this case, it is recommended for your application to consider any results invalid.</div>
<div> </div>

### -param cchDest [in]

Size, in characters, of the buffer indicated by <i>lpDestStr</i>. If the application is using the function for string mapping, it supplies a character count for this parameter. If space for a terminating null character is included in <i>cchSrc</i>, <i>cchDest</i> must also include space for a terminating null character.

If the application is using the function to generate a sort key, it supplies a byte count for the size. This byte count must include space for the sort key 0x00 terminator.

The application can set <i>cchDest</i> to 0. In this case, the function does not use the <i>lpDestStr</i> parameter and returns the required buffer size for the mapped string or sort key.


### -param lpVersionInformation [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/97f637df-3e0e-4349-a617-96b7c640b19d">NLSVERSIONINFOEX</a> structure that contains the version information about the relevant NLS capability; usually retrieved from <a href="https://msdn.microsoft.com/255e6774-eb70-41db-a372-8796166ee8d6">GetNLSVersionEx</a>.

<b>Windows Vista, Windows 7:</b> Reserved; must set to <b>NULL</b>.


### -param lpReserved [in, optional]

Reserved; must be <b>NULL</b>.


### -param sortHandle [in, optional]

Reserved; must be 0.


## -returns



Returns the number of characters or bytes in the translated string or sort key, including a terminating null character, if successful. If the function succeeds and the value of <i>cchDest</i> is 0, the return value is the size of the buffer required to hold the translated string or sort key, including a terminating null character if the input was null terminated.

This function returns 0 if it does not succeed. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



The application can use <a href="https://msdn.microsoft.com/84dda2cd-cbf9-45e9-b18c-7dea0b5bc991">LCMapString</a> or <b>LCMapStringEx</b> to generate a sort key. To do this, the application specifies  LCMAP_SORTKEY for the <i>dwMapFlags</i> parameter. For more information, see <a href="https://msdn.microsoft.com/c8fc32bd-02bd-4a40-a836-d9ad9f69c209">Handling Sorting in Your Applications</a>.

Another way for your application to use <a href="https://msdn.microsoft.com/84dda2cd-cbf9-45e9-b18c-7dea0b5bc991">LCMapString</a> or <b>LCMapStringEx</b> is in mapping strings. In this case, the application does not specify LCMAP_SORTKEY for the <i>dwMapFlags</i> parameter, but supplies some other combination of flags. For more information, see <a href="https://msdn.microsoft.com/c8fc32bd-02bd-4a40-a836-d9ad9f69c209">Handling Sorting in Your Applications</a>.

<b>Beginning in Windows Vista:</b> This function can handle data from <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="https://msdn.microsoft.com/f62402d6-31de-4ff7-9538-7925a007a089">Using Persistent Locale Data</a>.

<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="https://msdn.microsoft.com/e9e566c3-e84a-44d3-980f-fe8bbd5e052a">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="https://msdn.microsoft.com/99264b22-3fb5-47e2-b0b9-42a6768e67c1">ResolveLocaleName</a>.




## -see-also




<a href="https://msdn.microsoft.com/4db84fa7-f3c2-48fb-ad7d-8673397c4b0e">CompareString</a>



<a href="https://msdn.microsoft.com/38339881-30d2-4f55-9fee-81916ab15135">FindNLSStringEx</a>



<a href="https://msdn.microsoft.com/255e6774-eb70-41db-a372-8796166ee8d6">GetNLSVersionEx</a>



<a href="https://msdn.microsoft.com/c8fc32bd-02bd-4a40-a836-d9ad9f69c209">Handling Sorting in Your Applications</a>



<a href="https://msdn.microsoft.com/84dda2cd-cbf9-45e9-b18c-7dea0b5bc991">LCMapString</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

