---
UID: NF:stringapiset.GetStringTypeW
title: GetStringTypeW function (stringapiset.h)
description: Retrieves character type information for the characters in the specified Unicode source string.
helpviewer_keywords: ["CT_CTYPE1","CT_CTYPE2","CT_CTYPE3","GetStringTypeW","GetStringTypeW function [Internationalization for Windows Applications]","_win32_GetStringTypeW","_win32_GetStringTypeW_cpp","intl.getstringtypew","stringapiset/GetStringTypeW","winui._win32_GetStringTypeW"]
old-location: intl\getstringtypew.htm
tech.root: Intl
ms.assetid: 092541ea-e568-4aa3-b99e-ce0bac9c120b
ms.date: 10/23/2024
ms.keywords: CT_CTYPE1, CT_CTYPE2, CT_CTYPE3, GetStringTypeW, GetStringTypeW function [Internationalization for Windows Applications], _win32_GetStringTypeW, _win32_GetStringTypeW_cpp, intl.getstringtypew, stringapiset/GetStringTypeW, winui._win32_GetStringTypeW
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
ms.custom: 19H1
f1_keywords:
 - GetStringTypeW
 - stringapiset/GetStringTypeW
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
 - GetStringTypeW
---

# GetStringTypeW function


## -description

> [!NOTE]
> This API may have incomplete/outdated information for certain Unicode characters, particularly those in the supplementary range. For more accurate and comprehensive Unicode character type information, consider using equivalent ICU APIs such as [u_charType](https://unicode-org.github.io/icu-docs/apidoc/dev/icu4c/uchar_8h.html#a53f7567680cb6d92489d6e7750c90284), [u_islower](https://unicode-org.github.io/icu-docs/apidoc/dev/icu4c/uchar_8h.html#a65980f5668ed1df7f183a090f62b0e61), [u_isspace](https://unicode-org.github.io/icu-docs/apidoc/dev/icu4c/uchar_8h.html#a48dd198b451e691cf81eb41831474ddc), and [u_ispunct](https://unicode-org.github.io/icu-docs/apidoc/dev/icu4c/uchar_8h.html#add0409f1e6cbbc84dda50c45cc3e7302). For guidance on using ICU APIs on Windows, see [Getting Started with ICU on Windows](/windows/win32/intl/international-components-for-unicode--icu-#getting-started).

Retrieves character type information for the characters in the specified Unicode source string. For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array. Each bit identifies a given character type, for example, letter, digit, or neither.      <div class="alert"><b>Caution</b>  Using the <b>GetStringTypeW</b> function incorrectly can compromise the security of your application. To avoid a buffer overflow, the application must set the output buffer size correctly. For more security information, see <a href="/windows/desktop/AppUIStart/sec-ui">Security Considerations: Windows User Interface</a>.</div>
<div> </div>

## -parameters

### -param dwInfoType [in]

Flags specifying the character type information to retrieve. This parameter can have the following values. The character types are divided into different levels as described in the Remarks section.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CT_CTYPE1"></a><a id="ct_ctype1"></a><dl>
<dt><b>CT_CTYPE1</b></dt>
</dl>
</td>
<td width="60%">
Retrieve character type information.

</td>
</tr>
<tr>
<td width="40%"><a id="CT_CTYPE2"></a><a id="ct_ctype2"></a><dl>
<dt><b>CT_CTYPE2</b></dt>
</dl>
</td>
<td width="60%">
Retrieve bidirectional layout information.

</td>
</tr>
<tr>
<td width="40%"><a id="CT_CTYPE3"></a><a id="ct_ctype3"></a><dl>
<dt><b>CT_CTYPE3</b></dt>
</dl>
</td>
<td width="60%">
Retrieve text processing information.

</td>
</tr>
</table>

### -param lpSrcStr [in]

Pointer to the Unicode string for which to retrieve the character types. The string is assumed to be null-terminated if <i>cchSrc</i> is set to any negative value.

### -param cchSrc [in]

Size, in characters, of the string indicated by <i>lpSrcStr</i>. If the size includes a terminating null character, the function retrieves character type information for that character. If the application sets the size to any negative integer, the source string is assumed to be null-terminated and the function calculates the size automatically with an additional character for the null termination.

### -param lpCharType [out]

Pointer to an array of 16-bit values. The length of this array must be large enough to receive one 16-bit value for each character in the source string. If <i>cchSrc</i> is not a negative number, <i>lpCharType</i> should be an array of words with <i>cchSrc</i> elements. If <i>cchSrc</i> is set to a negative number, <i>lpCharType</i> is an array of words with <i>lpSrcStr</i> + 1 elements. When the function returns, this array contains one word corresponding to each character in the source string.

## -returns

Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

For an overview of the use of the string functions, see <a href="/windows/desktop/menurc/strings">Strings</a>.

The values of the <i>lpSrcStr</i> and <i>lpCharType</i> parameters must not be the same. If they are the same, the function fails with ERROR_INVALID_PARAMETER.

The <i>Locale</i> parameter used by the corresponding <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea">GetStringTypeA</a> function is not used by this function. Because of the parameter difference, an application cannot automatically invoke the proper ANSI or Unicode version of a <b>GetStringType*</b> function through the use of the #define UNICODE switch. An application can circumvent this limitation by using <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw">GetStringTypeEx</a>, which is the recommended function.

<b>Supported Character Types</b>

The character type bits are divided into several levels. The information for one level can be retrieved by a single call to this function. Each level is limited to 16 bits of information so that the other mapping functions, which are limited to 16 bits of representation per character, can also return character type information.

<u>Ctype 1</u>

These types support ANSI C and POSIX (LC_CTYPE) character typing functions. A bitwise-OR of these values is retrieved in the array in the output buffer when <i>dwInfoType</i> is set to CT_CTYPE1. For DBCS locales, the type attributes apply to both narrow characters and wide characters. The Japanese hiragana and katakana characters, and the kanji ideograph characters all have the C1_ALPHA attribute.


<table class="clsStd">
<tr>
<th>Name</th>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>C1_UPPER </td>
<td>0x0001</td>
<td>Uppercase </td>
</tr>
<tr>
<td>C1_LOWER</td>
<td>0x0002</td>
<td>Lowercase </td>
</tr>
<tr>
<td>C1_DIGIT</td>
<td>0x0004</td>
<td>Decimal digits </td>
</tr>
<tr>
<td>C1_SPACE</td>
<td>0x0008</td>
<td>Space characters </td>
</tr>
<tr>
<td>C1_PUNCT</td>
<td>0x0010</td>
<td>Punctuation </td>
</tr>
<tr>
<td>C1_CNTRL</td>
<td>0x0020</td>
<td>Control characters </td>
</tr>
<tr>
<td>C1_BLANK</td>
<td>0x0040</td>
<td>Blank characters </td>
</tr>
<tr>
<td>C1_XDIGIT</td>
<td>0x0080</td>
<td>Hexadecimal digits </td>
</tr>
<tr>
<td>C1_ALPHA</td>
<td>0x0100</td>
<td>Any linguistic character: alphabetical, syllabary, or ideographic</td>
</tr>
<tr>
<td>C1_DEFINED</td>
<td>0x0200</td>
<td>A defined character, but not one of the other C1_* types</td>
</tr>
</table>
 



The following character types are either constant or computable from basic types and do not need to be supported by this function.


<table class="clsStd">
<tr>
<th>Type</th>
<th>Description</th>
</tr>
<tr>
<td>Alphanumeric</td>
<td>Alphabetical characters and digits (C1_ALPHA and C1_DIGIT)</td>
</tr>
<tr>
<td>Printable</td>
<td>Graphic characters and blanks (all C1_* types except C1_CNTRL)</td>
</tr>
</table>
 



<u>Ctype 2</u>

These types support proper layout of Unicode text. For DBCS locales, the character type applies to both narrow and wide characters. The direction attributes are assigned so that the bidirectional layout algorithm standardized by Unicode produces accurate results. These types are mutually exclusive. For more information about the use of these attributes, see <a href="https://www.unicode.org/standard/standard.html">The Unicode Standard</a>.


<table class="clsStd">
<tr>
<th>Name</th>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>Strong</td>
<td></td>
<td></td>
</tr>
<tr>
<td>C2_LEFTTORIGHT</td>
<td>0x0001</td>
<td>Left to right </td>
</tr>
<tr>
<td>C2_RIGHTTOLEFT</td>
<td>0x0002</td>
<td>Right to left </td>
</tr>
<tr>
<td>Weak</td>
<td></td>
<td></td>
</tr>
<tr>
<td>C2_EUROPENUMBER</td>
<td>0x0003</td>
<td>European number, European digit</td>
</tr>
<tr>
<td>C2_EUROPESEPARATOR</td>
<td>0x0004</td>
<td>European numeric separator </td>
</tr>
<tr>
<td>C2_EUROPETERMINATOR</td>
<td>0x0005</td>
<td>European numeric terminator</td>
</tr>
<tr>
<td>C2_ARABICNUMBER</td>
<td>0x0006</td>
<td>Arabic number </td>
</tr>
<tr>
<td>C2_COMMONSEPARATOR</td>
<td>0x0007</td>
<td>Common numeric separator </td>
</tr>
<tr>
<td>Neutral</td>
<td></td>
<td></td>
</tr>
<tr>
<td>C2_BLOCKSEPARATOR</td>
<td>0x0008</td>
<td>Block separator </td>
</tr>
<tr>
<td>C2_SEGMENTSEPARATOR</td>
<td>0x0009</td>
<td>Segment separator </td>
</tr>
<tr>
<td>C2_WHITESPACE</td>
<td>0x000A</td>
<td>White space </td>
</tr>
<tr>
<td>C2_OTHERNEUTRAL</td>
<td>0x000B</td>
<td>Other neutrals </td>
</tr>
<tr>
<td>Not applicable</td>
<td></td>
<td></td>
</tr>
<tr>
<td>C2_NOTAPPLICABLE</td>
<td>0x0000</td>
<td>No implicit directionality (for example, control codes)</td>
</tr>
</table>
 



<u>Ctype 3</u>

These types are intended to be placeholders for extensions to the POSIX types required for general text processing or for the standard C library functions. A bitwise-OR of these values is retrieved when <i>dwInfoType</i> is set to CT_CTYPE3. For DBCS locales, the Ctype 3 attributes apply to both narrow characters and wide characters. The Japanese hiragana and katakana characters, and the kanji ideograph characters all have the C3_ALPHA attribute.



<table class="clsStd">
<tr>
<th>Name</th>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>C3_NONSPACING</td>
<td>0x0001</td>
<td>Nonspacing mark </td>
</tr>
<tr>
<td>C3_DIACRITIC</td>
<td>0x0002</td>
<td>Diacritic nonspacing mark </td>
</tr>
<tr>
<td>C3_VOWELMARK</td>
<td>0x0004</td>
<td>Vowel nonspacing mark </td>
</tr>
<tr>
<td>C3_SYMBOL</td>
<td>0x0008</td>
<td>Symbol </td>
</tr>
<tr>
<td>C3_KATAKANA</td>
<td>0x0010</td>
<td>Katakana character</td>
</tr>
<tr>
<td>C3_HIRAGANA</td>
<td>0x0020</td>
<td>Hiragana character </td>
</tr>
<tr>
<td>C3_HALFWIDTH</td>
<td>0x0040</td>
<td>Half-width (narrow) character </td>
</tr>
<tr>
<td>C3_FULLWIDTH</td>
<td>0x0080</td>
<td>Full-width (wide) character </td>
</tr>
<tr>
<td>C3_IDEOGRAPH</td>
<td>0x0100</td>
<td>Ideographic character </td>
</tr>
<tr>
<td>C3_KASHIDA</td>
<td>0x0200</td>
<td>Arabic kashida character </td>
</tr>
<tr>
<td>C3_LEXICAL</td>
<td>0x0400</td>
<td>Punctuation which is counted as part of the word (kashida, hyphen, feminine/masculine ordinal indicators, equal sign, and so forth) </td>
</tr>
<tr>
<td>C3_ALPHA</td>
<td>0x8000</td>
<td>All linguistic characters (alphabetical, syllabary, and ideographic)</td>
</tr>
<tr>
<td>C3_HIGHSURROGATE</td>
<td>0x0800</td>
<td><b>Windows Vista:</b> High surrogate code unit</td>
</tr>
<tr>
<td>C3_LOWSURROGATE</td>
<td>0x1000</td>
<td><b>Windows Vista:</b> Low surrogate code unit</td>
</tr>
<tr>
<td>Not applicable</td>
<td></td>
<td></td>
</tr>
<tr>
<td>C3_NOTAPPLICABLE</td>
<td>0x0000</td>
<td>Not applicable</td>
</tr>
</table>
 



C3_HIGHSURROGATE and C3_LOWSURROGATE are listed only for completeness, and should never be provided to this function. They are relevant only for Unicode.

<b>Starting with Windows 8: </b><b>GetStringTypeW</b>  is declared in Stringapiset.h. Before Windows 8, it was declared in Winnls.h.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea">GetStringTypeA</a>



<a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw">GetStringTypeEx</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
