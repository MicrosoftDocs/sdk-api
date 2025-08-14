---
UID: NF:winnls.GetSystemDefaultLocaleName
title: GetSystemDefaultLocaleName function (winnls.h)
description: Retrieves the system default locale name.Note  It is recommended that applications call GetUserDefaultLocaleName in preference over this function.
helpviewer_keywords: ["GetSystemDefaultLocaleName","GetSystemDefaultLocaleName function [Internationalization for Windows Applications]","_win32_GetSystemDefaultLocaleName","intl.getsystemdefaultlocalename","winnls/GetSystemDefaultLocaleName"]
old-location: intl\getsystemdefaultlocalename.htm
tech.root: Intl
ms.assetid: 1e925e41-64db-44aa-ab73-05d0f2036c8f
ms.date: 12/05/2018
ms.keywords: GetSystemDefaultLocaleName, GetSystemDefaultLocaleName function [Internationalization for Windows Applications], _win32_GetSystemDefaultLocaleName, intl.getsystemdefaultlocalename, winnls/GetSystemDefaultLocaleName
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetSystemDefaultLocaleName
 - winnls/GetSystemDefaultLocaleName
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
 - API-MS-Win-Core-Localization-Obsolete-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-Obsolete-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
 - API-MS-Win-Core-Localization-Obsolete-L1-3-0.dll
api_name:
 - GetSystemDefaultLocaleName
---

# GetSystemDefaultLocaleName function


## -description

Retrieves the system default <a href="/windows/desktop/Intl/locale-names">locale name</a>.<div class="alert"><b>Note</b>  It is recommended that applications call <a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultlocalename">GetUserDefaultLocaleName</a> in preference over this function. This is due to the user locale generally being more useful and accurate for the user than the system locale.</div>
<div> </div>
<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="/windows/desktop/api/winnls/nf-winnls-getsystemdefaultlcid">GetSystemDefaultLCID</a> if designed to run only on Windows Vista and later.</div>
<div> </div>

## -parameters

### -param lpLocaleName [out]

Pointer to a buffer in which this function retrieves the locale name.

### -param cchLocaleName [in]

Size, in characters, of the output buffer indicated by <i>lpLocaleName</i>. The maximum possible character length of a locale name (including a terminating null character) is the value of <a href="/windows/desktop/Intl/locale-name-constants">LOCALE_NAME_MAX_LENGTH</a>. This is the recommended size.

## -returns

Returns a value greater than 0 that indicates the length of the locale name, including the terminating null character, if successful.

This function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
</ul>

## -remarks

This function can retrieve data from <a href="/windows/desktop/Intl/custom-locales">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.


#### Examples

An example showing the use of this function can be found in <a href="/windows/desktop/Intl/nls--name-based-apis-sample">NLS: Name-based APIs Sample</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Intl/downlevellcidtolocalename">DownlevelLCIDToLocaleName</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoex">GetLocaleInfoEx</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultlocalename">GetUserDefaultLocaleName</a>



<a href="/windows/desktop/Intl/mapping-locale-data">Mapping Locale Data</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>