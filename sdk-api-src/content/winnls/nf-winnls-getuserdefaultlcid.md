---
UID: NF:winnls.GetUserDefaultLCID
title: GetUserDefaultLCID function (winnls.h)
description: Returns the locale identifier for the user default locale.Caution  If the user default locale is a custom locale, an application cannot accurately tag data with the value or exchange it.
helpviewer_keywords: ["GetUserDefaultLCID","GetUserDefaultLCID function [Internationalization for Windows Applications]","_win32_GetUserDefaultLCID","intl.getuserdefaultlcid","winnls/GetUserDefaultLCID"]
old-location: intl\getuserdefaultlcid.htm
tech.root: Intl
ms.assetid: bbf8399e-9034-4480-8d6e-030714f94e48
ms.date: 12/05/2018
ms.keywords: GetUserDefaultLCID, GetUserDefaultLCID function [Internationalization for Windows Applications], _win32_GetUserDefaultLCID, intl.getuserdefaultlcid, winnls/GetUserDefaultLCID
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
 - GetUserDefaultLCID
 - winnls/GetUserDefaultLCID
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
 - GetUserDefaultLCID
---

# GetUserDefaultLCID function


## -description

Returns the <a href="/windows/desktop/Intl/locale-identifiers">locale identifier</a> for the user default locale.
<div class="alert"><b>Caution</b>  If the user default locale is a custom locale, an application cannot accurately tag data with the value or exchange it. In this case, the application should use  <a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultlocalename">GetUserDefaultLocaleName</a> in preference to <b>GetUserDefaultLCID</b>.</div><div> </div><div class="alert"><b>Note</b>  Applications that are intended to run only on Windows Vista and later should use <a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultlocalename">GetUserDefaultLocaleName</a>.</div><div> </div>



## -returns

Returns the locale identifier for the user default locale, represented as <a href="/windows/desktop/Intl/locale-user-default">LOCALE_USER_DEFAULT</a>. If the user default locale is a custom locale, this function always returns <a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_DEFAULT</a>, regardless of the custom locale that is selected. For example, whether the user locale is Hawaiian (US), haw-US, or Fijiian (Fiji), fj-FJ, the function returns the same value.

## -remarks

This function can retrieve data from <a href="/windows/desktop/Intl/custom-locales">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-convertdefaultlocale">ConvertDefaultLocale</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoa">GetLocaleInfo</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getsystemdefaultlcid">GetSystemDefaultLCID</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultlocalename">GetUserDefaultLocaleName</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
