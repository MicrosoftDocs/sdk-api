---
UID: NF:winnls.FindNLSString
title: FindNLSString function (winnls.h)
description: Locates a Unicode string (wide characters) or its equivalent in another Unicode string for a locale specified by identifier.Caution  Because strings with very different binary representations can compare as identical, this function can raise certain security concerns. For more information, see the discussion of comparison functions in Security Considerations:\_International Features. Note  For interoperability reasons, the application should prefer the FindNLSStringEx function because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. Although FindNLSString supports custom locales, most applications should use FindNLSStringEx for this type of support.
helpviewer_keywords: ["FindNLSString","FindNLSString function [Internationalization for Windows Applications]","_win32_FindNLSString","intl.findnlsstring","winnls/FindNLSString"]
old-location: intl\findnlsstring.htm
tech.root: Intl
ms.assetid: d65a67d1-a7e1-4d2a-ae8b-6b4ac7f2a987
ms.date: 12/05/2018
ms.keywords: FindNLSString, FindNLSString function [Internationalization for Windows Applications], _win32_FindNLSString, intl.findnlsstring, winnls/FindNLSString
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - FindNLSString
 - winnls/FindNLSString
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
 - FindNLSString
---

# FindNLSString function


## -description

Locates a Unicode string (wide characters) or its equivalent in another Unicode string for a locale specified by identifier.
<div class="alert"><b>Caution</b>  Because strings with very different binary representations can compare as identical, this function can raise certain security concerns. For more information, see the discussion of comparison functions in <a href="/windows/desktop/Intl/security-considerations--international-features">Security Considerations: International Features</a>.</div><div> </div><div class="alert"><b>Note</b>  For interoperability reasons, the application should prefer the <a href="/windows/desktop/api/winnls/nf-winnls-findnlsstringex">FindNLSStringEx</a> function because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. Although <b>FindNLSString</b> supports custom locales, most applications should use <a href="/windows/desktop/api/winnls/nf-winnls-findnlsstringex">FindNLSStringEx</a> for this type of support.</div><div> </div>

## -parameters

### -param Locale [in]

<a href="/windows/desktop/Intl/locale-identifiers">Locale identifier</a> that specifies the locale. You can use the <a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro to create an identifier or use one of the following predefined values. 

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
<b>Windows Vista and later:</b> The following custom locale identifiers are also supported.

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

### -param dwFindNLSStringFlags [in]

Flags specifying details of the find operation. For detailed definitions, see the <i>dwFindNLSStringFlags</i> parameter of <a href="/windows/desktop/api/winnls/nf-winnls-findnlsstringex">FindNLSStringEx</a>.

### -param lpStringSource [in]

Pointer to the source string, in which the function searches for the string specified by <i>lpStringValue</i>.

### -param cchSource [in]

Size, in characters excluding the terminating null character, of the string indicated by <i>lpStringSource</i>. The application cannot specify 0 or any negative number other than -1 for this parameter. The application specifies -1 if the source string is null-terminated and the function should calculate the size automatically.

### -param lpStringValue [in]

Pointer to the search string, for which the function searches in the source string.

### -param cchValue [in]

Size, in characters excluding the terminating null character, of the string indicated by <i>lpStringValue</i>. The application cannot specify 0 or any negative number other than -1 for this parameter. The application specifies -1 if the search string is null-terminated and the function should calculate the size automatically.

### -param pcchFound [out, optional]

Pointer to a buffer containing the length of the string that the function finds. For details, see the <i>pcchFound</i> parameter of <a href="/windows/desktop/api/winnls/nf-winnls-findnlsstringex">FindNLSStringEx</a>.

## -returns

Returns a 0-based index into the source string indicated by <i>lpStringSource</i> if successful. In combination with the value in <i>pcchFound</i>, this index provides the exact location of the entire found string in the source string. A return value of 0 is an error-free index into the source string, and the matching string is in the source string at offset 0.

The function returns -1 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
<li>ERROR_SUCCESS. The action completed successfully but yielded no results.</li>
</ul>

## -remarks

See Remarks for <a href="/windows/desktop/api/winnls/nf-winnls-findnlsstringex">FindNLSStringEx</a>.

## -see-also

<a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw">CompareString</a>



<a href="/windows/desktop/api/winnls/nf-winnls-findnlsstringex">FindNLSStringEx</a>



<a href="/windows/desktop/Intl/handling-sorting-in-your-applications">Handling Sorting in Your Applications</a>



<a href="/windows/desktop/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>



<a href="/windows/desktop/Intl/security-considerations--international-features">Security Considerations: International Features</a>