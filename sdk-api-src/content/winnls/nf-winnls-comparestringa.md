---
UID: NF:winnls.CompareStringA
title: CompareStringA function (winnls.h)
description: Compares two character strings, for a locale specified by identifier.Caution  Using CompareString incorrectly can compromise the security of your application. (CompareStringA)
helpviewer_keywords: ["CompareString","CompareString function [Internationalization for Windows Applications]","CompareStringA","CompareStringW","_win32_CompareString","_win32_CompareString_cpp","intl.comparestring","stringapiset/CompareString","stringapiset/CompareStringA","stringapiset/CompareStringW","winnls/CompareString","winnls/CompareStringA","winnls/CompareStringW","winui._win32_CompareString"]
old-location: intl\comparestring.htm
tech.root: Intl
ms.assetid: 4db84fa7-f3c2-48fb-ad7d-8673397c4b0e
ms.date: 12/05/2018
ms.keywords: CompareString, CompareString function [Internationalization for Windows Applications], CompareStringA, CompareStringW, _win32_CompareString, _win32_CompareString_cpp, intl.comparestring, stringapiset/CompareString, stringapiset/CompareStringA, stringapiset/CompareStringW, winnls/CompareString, winnls/CompareStringA, winnls/CompareStringW, winui._win32_CompareString
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CompareStringW (Unicode) and CompareStringA (ANSI)
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
 - CompareStringA
 - winnls/CompareStringA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Localization-Obsolete-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-Obsolete-l1-2-0.dll
 - API-MS-Win-Core-String-l1-1-0.dll
 - API-MS-Win-deprecated-apis-Obsolete-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-Obsolete-L1-3-0.dll
api_name:
 - CompareString
 - CompareStringA
 - CompareStringW
---

# CompareStringA function


## -description

Compares two character strings, for a <a href="/windows/desktop/Intl/locales-and-languages">locale</a> specified by identifier.
<div class="alert"><b>Caution</b>  Using <b>CompareString</b> incorrectly can compromise the security of your application. Strings that are not compared correctly can produce invalid input. For example, the function can raise security issues when used for a non-linguistic comparison, because two strings that are distinct in their binary representation can be linguistically equivalent. The application should test strings for validity before using them, and should provide error handlers. For more information, see <a href="/windows/desktop/Intl/security-considerations--international-features">Security Considerations: International Features</a>.</div><div> </div><div class="alert"><b>Note</b>  For compatibility with Unicode, your applications should prefer <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex">CompareStringEx</a> or the Unicode version of <b>CompareString</b>. Another reason for preferring <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex">CompareStringEx</a> is that Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales, for interoperability reasons. Any application that will be run only on Windows Vista and later should use <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex">CompareStringEx</a>.</div><div> </div>

## -parameters

### -param Locale [in]

<a href="/windows/desktop/Intl/locale-identifiers">Locale identifier</a> of the locale used for the comparison. You can use the <a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values.

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

### -param dwCmpFlags [in]

Flags that indicate how the function compares the two strings. For detailed definitions, see the <i>dwCmpFlags</i> parameter of <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex">CompareStringEx</a>.

### -param lpString1 [in]

Pointer to the first string to compare.

### -param cchCount1 [in]

Length of the string indicated by <i>lpString1</i>, excluding the terminating null character. This value represents bytes for the ANSI version of the function and wide characters for the Unicode version. The application can supply a negative value if the string is null-terminated. In this case, the function determines the length automatically.

### -param lpString2 [in]

Pointer to the second string to compare.

### -param cchCount2 [in]

Length of the string indicated by <i>lpString2</i>, excluding the terminating null character. This value represents bytes for the ANSI version of the function and wide characters for the Unicode version. The application can supply a negative value if the string is null-terminated. In this case, the function determines the length automatically.

## -returns

Returns the values described for <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex">CompareStringEx</a>.

## -remarks

See Remarks for <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex">CompareStringEx</a>.

If your application is calling the ANSI version of <b>CompareString</b>, the function converts parameters via the default code page of the supplied locale. Thus, an application can never use <b>CompareString</b> to handle UTF-8 text.

Normally, for case-insensitive comparisons, <b>CompareString</b> maps the lowercase "i" to the uppercase "I", even when the locale is Turkish or Azerbaijani. The  NORM_LINGUISTIC_CASING flag overrides this behavior for Turkish or Azerbaijani. If this flag is specified in conjunction with Turkish or Azerbaijani, LATIN SMALL LETTER DOTLESS I (U+0131) is the lowercase form of LATIN CAPITAL LETTER I (U+0049) and LATIN SMALL LETTER I (U+0069) is the lowercase form of LATIN CAPITAL LETTER I WITH DOT ABOVE (U+0130).

<b>Starting with Windows 8: </b>The ANSI version of the function is declared in Winnls.h, and the Unicode version is declared in Stringapiset.h. Before Windows 8, both versions were declared in Winnls.h.





> [!NOTE]
> The winnls.h header defines CompareString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex">CompareStringEx</a>



<a href="/windows/desktop/Intl/handling-sorting-in-your-applications">Handling Sorting in Your Applications</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>



<a href="/windows/desktop/Intl/security-considerations--international-features">Security Considerations: International Features</a>



<a href="/windows/desktop/Intl/using-unicode-normalization-to-represent-strings">Using Unicode Normalization to Represent Strings</a>
