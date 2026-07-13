---
UID: NF:winnls.GetUserDefaultLocaleName
title: GetUserDefaultLocaleName function (winnls.h)
description: Retrieves the user default locale name.Note  The application should call this function in preference to GetUserDefaultLCID if designed to run only on Windows Vista and later.
helpviewer_keywords: ["GetUserDefaultLocaleName","GetUserDefaultLocaleName function [Internationalization for Windows Applications]","_win32_GetUserDefaultLocaleName","intl.getuserdefaultlocalename","winnls/GetUserDefaultLocaleName"]
old-location: intl\getuserdefaultlocalename.htm
tech.root: Intl
ms.assetid: 81b896de-1f06-4315-aa64-90806c0fed75
ms.date: 12/05/2018
ms.keywords: GetUserDefaultLocaleName, GetUserDefaultLocaleName function [Internationalization for Windows Applications], _win32_GetUserDefaultLocaleName, intl.getuserdefaultlocalename, winnls/GetUserDefaultLocaleName
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
 - GetUserDefaultLocaleName
 - winnls/GetUserDefaultLocaleName
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
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - GetUserDefaultLocaleName
---

# GetUserDefaultLocaleName function


## -description

Retrieves the user default <a href="/windows/desktop/Intl/locale-names">locale name</a>.<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultlcid">GetUserDefaultLCID</a> if designed to run only on Windows Vista and later.</div>
<div> </div>

## -parameters

### -param lpLocaleName [out]

Pointer to a buffer in which this function retrieves the locale name.

### -param cchLocaleName [in]

Size, in characters, of the buffer indicated by <i>lpLocaleName</i>. The maximum possible length of a locale name, including a terminating null character, is <a href="/windows/desktop/Intl/locale-name-constants">LOCALE_NAME_MAX_LENGTH</a>. This is the recommended size to supply in this parameter.

## -returns

Returns the size of the buffer containing the locale name, including the terminating null character, if successful.<div class="alert"><b>Note</b>  On single-user systems, the return value is the same as that returned by <a href="/windows/desktop/api/winnls/nf-winnls-getsystemdefaultlocalename">GetSystemDefaultLocaleName</a>.</div>
<div> </div>


The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
</ul>

## -remarks

This function can retrieve data from <a href="/windows/desktop/Intl/custom-locales">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoex">GetLocaleInfoEx</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getsystemdefaultlocalename">GetSystemDefaultLocaleName</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultlcid">GetUserDefaultLCID</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>