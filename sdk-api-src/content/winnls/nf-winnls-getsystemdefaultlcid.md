---
UID: NF:winnls.GetSystemDefaultLCID
title: GetSystemDefaultLCID function (winnls.h)
description: Returns the locale identifier for the system locale.Note  Any application that runs only on Windows Vista and later should use GetSystemDefaultLocaleName in preference to this function.
helpviewer_keywords: ["GetSystemDefaultLCID","GetSystemDefaultLCID function [Internationalization for Windows Applications]","_win32_GetSystemDefaultLCID","intl.getsystemdefaultlcid","winnls/GetSystemDefaultLCID"]
old-location: intl\getsystemdefaultlcid.htm
tech.root: Intl
ms.assetid: 67d73d88-6a6c-439b-a321-1b1bd05fe268
ms.date: 12/05/2018
ms.keywords: GetSystemDefaultLCID, GetSystemDefaultLCID function [Internationalization for Windows Applications], _win32_GetSystemDefaultLCID, intl.getsystemdefaultlcid, winnls/GetSystemDefaultLCID
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
 - GetSystemDefaultLCID
 - winnls/GetSystemDefaultLCID
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
 - GetSystemDefaultLCID
---

# GetSystemDefaultLCID function


## -description

Returns the <a href="/windows/desktop/Intl/locale-identifiers">locale identifier</a> for the system locale.<div class="alert"><b>Note</b>  Any application that runs only on Windows Vista and later should use <a href="/windows/desktop/api/winnls/nf-winnls-getsystemdefaultlocalename">GetSystemDefaultLocaleName</a> in preference to this function.</div>
<div> </div>



## -returns

Returns the locale identifier for the system default locale, identified by <a href="/windows/desktop/Intl/locale-system-default">LOCALE_SYSTEM_DEFAULT</a>.

## -remarks

This function can retrieve data from <a href="/windows/desktop/Intl/custom-locales">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-convertdefaultlocale">ConvertDefaultLocale</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoa">GetLocaleInfo</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getsystemdefaultlocalename">GetSystemDefaultLocaleName</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultlcid">GetUserDefaultLCID</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
