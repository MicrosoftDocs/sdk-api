---
UID: NF:winnls.GetThreadLocale
title: GetThreadLocale function (winnls.h)
description: Returns the locale identifier of the current locale for the calling thread.Note  This function can retrieve data that changes between releases, for example, due to a custom locale.
helpviewer_keywords: ["GetThreadLocale","GetThreadLocale function [Internationalization for Windows Applications]","_win32_GetThreadLocale","intl.getthreadlocale","winnls/GetThreadLocale"]
old-location: intl\getthreadlocale.htm
tech.root: Intl
ms.assetid: 4d77f78b-f059-40f3-b4ed-c3ffd09d9e9f
ms.date: 12/05/2018
ms.keywords: GetThreadLocale, GetThreadLocale function [Internationalization for Windows Applications], _win32_GetThreadLocale, intl.getthreadlocale, winnls/GetThreadLocale
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
 - GetThreadLocale
 - winnls/GetThreadLocale
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
 - GetThreadLocale
---

# GetThreadLocale function


## -description

Returns the <a href="/windows/desktop/Intl/locale-identifiers">locale identifier</a> of the current locale for the calling thread.<div class="alert"><b>Note</b>  This function can retrieve data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.</div>
<div> </div>



## -returns

Returns the <a href="/windows/desktop/Intl/locale-identifiers">locale identifier</a> of the locale associated with the current thread.

<b>Windows Vista</b>: This function can return the identifier of a <a href="/windows/desktop/Intl/custom-locales">custom locale</a>. If the current thread locale is a custom locale, the function returns <a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_DEFAULT</a>. If the current thread locale is a supplemental custom locale, the function can return <a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UNSPECIFIED</a>. All supplemental locales share this locale identifier.

## -remarks

When an application process launches, it uses the Standards and Formats variable for the locale. For more information, see <a href="/windows/desktop/Intl/nls-terminology">NLS Terminology</a>.

When a new thread is created in a process, it inherits the locale of the creating thread. This locale can be either the default Standards and Formats locale or a different locale set for the creating thread in a call to <a href="/windows/desktop/api/winnls/nf-winnls-setthreadlocale">SetThreadLocale</a>. <b>GetThreadLocale</b> and <b>SetThreadLocale</b> can be used to modify the locale of the new thread.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getsystemdefaultlcid">GetSystemDefaultLCID</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultlcid">GetUserDefaultLCID</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>



<a href="/windows/desktop/api/winnls/nf-winnls-setthreadlocale">SetThreadLocale</a>
