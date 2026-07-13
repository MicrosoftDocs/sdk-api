---
UID: NF:winnls.FoldStringA
title: FoldStringA function (winnls.h)
description: Maps one Unicode string to another, performing the specified transformation. (FoldStringA)
helpviewer_keywords: ["FoldString","FoldString function [Internationalization for Windows Applications]","FoldStringA","FoldStringW","MAP_COMPOSITE","MAP_EXPAND_LIGATURES","MAP_FOLDCZONE","MAP_FOLDDIGITS","MAP_PRECOMPOSED","_win32_FoldString","_win32_FoldString_cpp","intl.foldstring","stringapiset/FoldString","stringapiset/FoldStringA","stringapiset/FoldStringW","winnls/FoldString","winnls/FoldStringA","winnls/FoldStringW","winui._win32_FoldString"]
old-location: intl\foldstring.htm
tech.root: Intl
ms.assetid: 986b9a72-04c0-49e2-8424-8948dc64de0c
ms.date: 12/05/2018
ms.keywords: FoldString, FoldString function [Internationalization for Windows Applications], FoldStringA, FoldStringW, MAP_COMPOSITE, MAP_EXPAND_LIGATURES, MAP_FOLDCZONE, MAP_FOLDDIGITS, MAP_PRECOMPOSED, _win32_FoldString, _win32_FoldString_cpp, intl.foldstring, stringapiset/FoldString, stringapiset/FoldStringA, stringapiset/FoldStringW, winnls/FoldString, winnls/FoldStringA, winnls/FoldStringW, winui._win32_FoldString
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FoldStringW (Unicode) and FoldStringA (ANSI)
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
 - FoldStringA
 - winnls/FoldStringA
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
 - API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - FoldString
 - FoldStringA
 - FoldStringW
---

# FoldStringA function


## -description

Maps one Unicode string to another, performing the specified transformation. For an overview of the use of the string functions, see <a href="/windows/desktop/menurc/strings">Strings</a>.
<div class="alert"><b>Caution</b>  Using <b>FoldString</b> incorrectly can compromise the security of your application. Strings that are not mapped correctly can produce invalid input. Test strings to make sure they are valid before using them and provide error handlers. For more information, see <a href="/windows/desktop/Intl/security-considerations--international-features">Security Considerations: International Features</a>.</div><div> </div>

## -parameters

### -param dwMapFlags [in]

Flags specifying the type of transformation to use during string mapping. This parameter can be a combination of the following values.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MAP_COMPOSITE"></a><a id="map_composite"></a><dl>
<dt><b>MAP_COMPOSITE</b></dt>
</dl>
</td>
<td width="60%">
Map accented characters to decomposed characters, that is, characters in which a base character and one or more nonspacing characters each have distinct code point values. For example, Ä is represented by A + ¨: LATIN CAPITAL LETTER A (U+0041) + COMBINING DIAERESIS (U+0308). This flag is equivalent to normalization form D in Windows Vista. Note that this flag cannot be used with MB_PRECOMPOSED.

</td>
</tr>
<tr>
<td width="40%"><a id="MAP_EXPAND_LIGATURES"></a><a id="map_expand_ligatures"></a><dl>
<dt><b>MAP_EXPAND_LIGATURES</b></dt>
</dl>
</td>
<td width="60%">
Expand all ligature characters so that they are represented by their two-character equivalent. For example, the ligature "æ" (U+00e6) expands to the two characters "a" (U+0061) + "e" (U+0065). This value cannot be combined with MAP_PRECOMPOSED or MAP_COMPOSITE.

</td>
</tr>
<tr>
<td width="40%"><a id="MAP_FOLDCZONE"></a><a id="map_foldczone"></a><dl>
<dt><b>MAP_FOLDCZONE</b></dt>
</dl>
</td>
<td width="60%">
Fold compatibility zone characters into standard Unicode equivalents. This flag is equivalent to normalization form KD in Windows Vista, if the MAP_COMPOSITE flag is also set. If the composite flag is not set (default), this flag is equivalent to normalization form KC in Windows Vista.

</td>
</tr>
<tr>
<td width="40%"><a id="MAP_FOLDDIGITS"></a><a id="map_folddigits"></a><dl>
<dt><b>MAP_FOLDDIGITS</b></dt>
</dl>
</td>
<td width="60%">
Map all digits to Unicode characters 0 through 9. 

</td>
</tr>
<tr>
<td width="40%"><a id="MAP_PRECOMPOSED"></a><a id="map_precomposed"></a><dl>
<dt><b>MAP_PRECOMPOSED</b></dt>
</dl>
</td>
<td width="60%">
Map accented characters to precomposed characters, in which the accent and base character are combined into a single character value. This flag is equivalent to normalization form C in Windows Vista. This value cannot be combined with MAP_COMPOSITE.

</td>
</tr>
</table>

### -param lpSrcStr [in]

Pointer to a source string that the function maps.

### -param cchSrc [in]

Size, in characters, of the source string indicated by <i>lpSrcStr</i>, excluding the terminating null character. The application can set the parameter to any negative value to specify that the source string is null-terminated. In this case, the function calculates the string length automatically, and null-terminates the mapped string indicated by <i>lpDestStr</i>.

### -param lpDestStr [out, optional]

Pointer to a buffer in which this function retrieves the mapped string.

### -param cchDest [in]

Size, in characters, of the destination string indicated by <i>lpDestStr</i>. If space for a terminating null character is included in <i>cchSrc</i>, <i>cchDest</i> must also include space for a terminating null character.

The application can set <i>cchDest</i> to 0. In this case, the function does not use the <i>lpDestStr</i> parameter and returns the required buffer size for the mapped string. If the MAP_FOLDDIGITS flag is specified, the return value is the maximum size required, even if the actual number of characters needed is smaller than the maximum size. If the maximum size is not passed, the function fails with ERROR_INSUFFICIENT_BUFFER.

## -returns

Returns the number of characters in the translated string, including a terminating null character, if successful. If the function succeeds and the value of <i>cchDest</i> is 0, the return value is the size of the buffer required to hold the translated string, including a terminating null character.

This function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_DATA. The data was invalid.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
<li>ERROR_MOD_NOT_FOUND. The module was not found. </li>
<li>ERROR_OUTOFMEMORY. Not enough storage was available to complete this operation. </li>
<li>ERROR_PROC_NOT_FOUND. The required procedure was not found.</li>
</ul>

## -remarks

The values of the <i>lpSrcStr</i> and <i>lpDestStr</i> parameters must not be the same. If they are the same, the function fails with ERROR_INVALID_PARAMETER.

The compatibility zone in Unicode consists of characters in the range 0xF900 through 0xFFEF that are assigned to characters from other encoding standards for characters but are actually variants of characters already in Unicode. The compatibility zone is used to support round-trip mapping to these standards. Applications can use the MAP_FOLDCZONE flag to avoid supporting the duplication of characters in the compatibility zone.

<b>Starting with Windows Vista:</b> This function supports Unicode normalization. All Unicode compatibility characters are mapped.

<b>Starting with Windows Vista:</b> The transformations indicated by the MAP_FOLDCZONE, MAP_PRECOMPOSED, and MAP_COMPOSITE flags use Unicode normalization forms KC, C, and D (through the <a href="/windows/desktop/api/winnls/nf-winnls-normalizestring">NormalizeString</a> function) to do the mappings.

<b>Starting with Windows 8: </b>The ANSI version of the function is declared in Winnls.h and the Unicode version is declared in Stringapiset.h. Before Windows 8, both versions were declared in Winnls.h.

## -see-also

<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>



<a href="/windows/desktop/api/winnls/nf-winnls-normalizestring">NormalizeString</a>



<a href="/windows/desktop/Intl/security-considerations--international-features">Security Considerations: International Features</a>



<a href="/windows/desktop/Intl/sorting">Sorting</a>



<a href="/windows/desktop/Intl/using-unicode-normalization-to-represent-strings">Using Unicode Normalization to Represent Strings</a>
