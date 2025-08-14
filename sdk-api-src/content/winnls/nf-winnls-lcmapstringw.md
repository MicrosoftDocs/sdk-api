---
UID: NF:winnls.LCMapStringW
title: LCMapStringW function (winnls.h)
description: For a locale specified by identifier, maps one input character string to another using a specified transformation, or generates a sort key for the input string. (Unicode)
helpviewer_keywords: ["LCMapString", "LCMapString function [Internationalization for Windows Applications]", "LCMapStringW", "_win32_LCMapString", "intl.lcmapstring", "winnls/LCMapString", "winnls/LCMapStringW"]
old-location: intl\lcmapstring.htm
tech.root: Intl
ms.assetid: 84dda2cd-cbf9-45e9-b18c-7dea0b5bc991
ms.date: 08/08/2025
ms.keywords: LCMapString, LCMapString function [Internationalization for Windows Applications], LCMapStringA, LCMapStringW, _win32_LCMapString, intl.lcmapstring, winnls/LCMapString, winnls/LCMapStringA, winnls/LCMapStringW
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LCMapStringW (Unicode) and LCMapStringA (ANSI)
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
 - LCMapStringW
 - winnls/LCMapStringW
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
 - API-MS-Win-Core-misc-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - LCMapString
 - LCMapStringA
 - LCMapStringW
---

# LCMapStringW function

## -description

For a locale specified by identifier, maps one input character string to another using a specified transformation, or generates a sort key for the input string. <div class="alert"><b>Note</b>  For interoperability reasons, the application should prefer the <a href="/windows/desktop/api/winnls/nf-winnls-lcmapstringex">LCMapStringEx</a> function to <b>LCMapString</b> because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. This recommendation applies especially to custom locales, including those created by Microsoft. Any application that will be run only on Windows Vista and later should use <a href="/windows/desktop/api/winnls/nf-winnls-lcmapstringex">LCMapStringEx</a>. </div>
<div> </div>

## -parameters

### -param Locale [in]

<a href="/windows/desktop/Intl/locale-identifiers">Locale identifier</a> that specifies the locale. You can use the <a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values.

<ul>
<li>
<a href="/windows/desktop/Intl/locale-invariant">LOCALE_INVARIANT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-system-default">LOCALE_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-user-default">LOCALE_USER_DEFAULT</a>
</li>
</ul>
The following custom locale identifiers are also supported.

<ul>
<li>
<a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UI_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UNSPECIFIED</a>
</li>
</ul>

### -param dwMapFlags [in]

Flags specifying the type of transformation to use during string mapping or the type of sort key to generate. For detailed definitions, see the <i>dwMapFlags</i> parameter of <a href="/windows/desktop/api/winnls/nf-winnls-lcmapstringex">LCMapStringEx</a>.

### -param lpSrcStr [in]

Pointer to a source string that the function maps or uses for sort key generation. This string cannot have a size of 0.

### -param cchSrc [in]

Size, in characters, of the source string indicated by <i>lpSrcStr</i>. The size of the source string can include the terminating null character, but does not have to. If the terminating null character is included, the mapping behavior of the function is not greatly affected because the terminating null character is considered to be unsortable and always maps to itself.

The application can set the parameter to any negative value to specify that the source string is null-terminated. In this case, if <b>LCMapString</b> is being used in its string-mapping mode, the function calculates the string length itself, and null-terminates the mapped string indicated by <i>lpDestStr</i>.

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

## -returns

If the function succeeds when used for string mapping, it returns the number of characters in the translated string (see *cchSrc* and *cchDest* for more details).

If the function succeeds when used to generate sort keys, it returns the number of bytes in the sort key.

This function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

This function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

See Remarks for <a href="/windows/desktop/api/winnls/nf-winnls-lcmapstringex">LCMapStringEx</a>.

The ANSI version of <b>LCMapString</b> maps strings to and from Unicode based on the default Windows (ANSI) code page associated with the specified locale. When the ANSI version of this function is used with a Unicode-only locale, the function can succeed because the operating system uses the CP_ACP value, representing the system default Windows ANSI code page. However, characters that are undefined in the system code page appear in the string as a question mark (?).





> [!NOTE]
> The winnls.h header defines LCMapString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw">CompareString</a>



<a href="/windows/desktop/api/winnls/nf-winnls-findnlsstring">FindNLSString</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getnlsversion">GetNLSVersion</a>



<a href="/windows/desktop/Intl/handling-sorting-in-your-applications">Handling Sorting in Your Applications</a>



<a href="/windows/desktop/api/winnls/nf-winnls-lcmapstringex">LCMapStringEx</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
