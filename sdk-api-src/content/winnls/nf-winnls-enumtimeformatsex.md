---
UID: NF:winnls.EnumTimeFormatsEx
title: EnumTimeFormatsEx function (winnls.h)
description: Enumerates the time formats that are available for a locale specified by name.Note  The application should call this function in preference to EnumTimeFormats if designed to run only on Windows Vista and later. Note  This function can enumerate data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see Using Persistent Locale Data.
helpviewer_keywords: ["EnumTimeFormatsEx","EnumTimeFormatsEx function [Internationalization for Windows Applications]","_win32_EnumTimeFormatsEx","intl.enumtimeformatsex","winnls/EnumTimeFormatsEx"]
old-location: intl\enumtimeformatsex.htm
tech.root: Intl
ms.assetid: db2e297e-98db-4e34-b44c-c0ddcddf2a6e
ms.date: 12/05/2018
ms.keywords: EnumTimeFormatsEx, EnumTimeFormatsEx function [Internationalization for Windows Applications], _win32_EnumTimeFormatsEx, intl.enumtimeformatsex, winnls/EnumTimeFormatsEx
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
 - EnumTimeFormatsEx
 - winnls/EnumTimeFormatsEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Localization-l2-1-0.dll
 - KernelBase.dll
api_name:
 - EnumTimeFormatsEx
---

# EnumTimeFormatsEx function


## -description

Enumerates the time formats that are available for a locale specified by name.
<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="/windows/desktop/api/winnls/nf-winnls-enumtimeformatsa">EnumTimeFormats</a> if designed to run only on Windows Vista and later.</div><div> </div><div class="alert"><b>Note</b>  This function can enumerate data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.</div><div> </div>

## -parameters

### -param lpTimeFmtEnumProcEx [in]

Pointer to an application-defined callback function. For more information, see <a href="/previous-versions/windows/desktop/legacy/dd317833(v=vs.85)">EnumTimeFormatsProcEx</a>.

### -param lpLocaleName [in, optional]

Pointer to a <a href="/windows/desktop/Intl/locale-names">locale name</a>, or one of the following predefined values. 

<ul>
<li>
<a href="/windows/desktop/Intl/locale-name-constants">LOCALE_NAME_INVARIANT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-name-constants">LOCALE_NAME_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-name-constants">LOCALE_NAME_USER_DEFAULT</a>
</li>
</ul>

### -param dwFlags [in]

The time format. Set to 0 to use the current user's long time format, or TIME_NOSECONDS (starting with Windows 7) to use the short time format.

### -param lParam [in]

An application-provided parameter to be passed to the callback function. This is especially useful for multi-threaded applications.

## -returns

Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

This function enumerates the time formats by passing time format string pointers, one at a time, to the specified application-defined callback function, along with an application-defined constant that is useful for multi-threaded applications. The first value in the enumeration is always the user default (override) value. The function continues enumeration until the last time format is found or the callback function returns <b>FALSE</b>. 

<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="/uwp/api/Windows.Globalization">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="/windows/desktop/api/winnls/nf-winnls-resolvelocalename">ResolveLocaleName</a>.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-enumtimeformatsa">EnumTimeFormats</a>



<a href="/previous-versions/windows/desktop/legacy/dd317833(v=vs.85)">EnumTimeFormatsProcEx</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>