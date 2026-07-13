---
UID: NF:winnls.ConvertDefaultLocale
title: ConvertDefaultLocale function (winnls.h)
description: Converts a default locale value to an actual locale identifier.
helpviewer_keywords: ["ConvertDefaultLocale","ConvertDefaultLocale function [Internationalization for Windows Applications]","_win32_ConvertDefaultLocale","intl.convertdefaultlocale","winnls/ConvertDefaultLocale"]
old-location: intl\convertdefaultlocale.htm
tech.root: Intl
ms.assetid: e227bb9f-f072-4e44-bd55-24c98b990a36
ms.date: 12/05/2018
ms.keywords: ConvertDefaultLocale, ConvertDefaultLocale function [Internationalization for Windows Applications], _win32_ConvertDefaultLocale, intl.convertdefaultlocale, winnls/ConvertDefaultLocale
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ConvertDefaultLocale
 - winnls/ConvertDefaultLocale
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
 - kernel32.dll
 - API-MS-Win-Core-Localization-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - ConvertDefaultLocale
---

# ConvertDefaultLocale function


## -description

Converts a default locale value to an actual <a href="/windows/desktop/Intl/locale-identifiers">locale identifier</a>.
<div class="alert"><b>Note</b>  This function is only provided for converting partial locale identifiers. Your applications should use locale names instead of identifiers. The <a href="/windows/desktop/api/winnls/nf-winnls-lcidtolocalename">LCIDToLocaleName</a> function can be used to convert a locale identifier to a valid locale name. Your application can also use <a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultlocalename">GetUserDefaultLocaleName</a> to retrieve the current user locale name; <a href="/windows/desktop/api/winnls/nf-winnls-getsystemdefaultlocalename">GetSystemDefaultLocaleName</a> to retrieve the current system locale name; and <a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoex">GetLocaleInfoEx</a> with <a href="/windows/desktop/Intl/locale-sname">LOCALE_SNAME</a> to retrieve the locale name for any input locale, including the default constants.</div><div> </div>

## -parameters

### -param Locale [in]

Default locale identifier value to convert. You can use the <a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

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

## -returns

Returns the appropriate locale identifier if successful.

This function returns the value of the <i>Locale</i> parameter if it does not succeed. The function fails when the <i>Locale</i> value is not one of the default values listed above.

## -remarks

A call to <b>ConvertDefaultLocale</b> specifying LOCALE_SYSTEM_DEFAULT is equivalent to a call to <a href="/windows/desktop/api/winnls/nf-winnls-getsystemdefaultlcid">GetSystemDefaultLCID</a>. A call to <b>ConvertDefaultLocale</b> specifying LOCALE_USER_DEFAULT is equivalent to a call to <a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultlcid">GetUserDefaultLCID</a>.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoex">GetLocaleInfoEx</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getsystemdefaultlcid">GetSystemDefaultLCID</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getsystemdefaultlocalename">GetSystemDefaultLocaleName</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultlcid">GetUserDefaultLCID</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultlocalename">GetUserDefaultLocaleName</a>



<a href="/windows/desktop/api/winnls/nf-winnls-lcidtolocalename">LCIDToLocaleName</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>