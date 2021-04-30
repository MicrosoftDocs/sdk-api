---
UID: NF:winnls.EnumCalendarInfoExEx
title: EnumCalendarInfoExEx function (winnls.h)
description: Enumerates calendar information for a locale specified by name.Note  The application should call this function in preference to EnumCalendarInfo or EnumCalendarInfoEx if designed to run only on Windows Vista and later. Note  This function can enumerate data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see Using Persistent Locale Data.
helpviewer_keywords: ["EnumCalendarInfoExEx","EnumCalendarInfoExEx function [Internationalization for Windows Applications]","_win32_EnumCalendarInfoExEx","intl.enumcalendarinfoexex","winnls/EnumCalendarInfoExEx"]
old-location: intl\enumcalendarinfoexex.htm
tech.root: Intl
ms.assetid: 2aa4d5b8-9afc-4657-92f0-d5d61791b807
ms.date: 12/05/2018
ms.keywords: EnumCalendarInfoExEx, EnumCalendarInfoExEx function [Internationalization for Windows Applications], _win32_EnumCalendarInfoExEx, intl.enumcalendarinfoexex, winnls/EnumCalendarInfoExEx
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
 - EnumCalendarInfoExEx
 - winnls/EnumCalendarInfoExEx
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
 - EnumCalendarInfoExEx
---

# EnumCalendarInfoExEx function


## -description

Enumerates calendar information for a locale specified by name.<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="/windows/desktop/api/winnls/nf-winnls-enumcalendarinfoa">EnumCalendarInfo</a> or <a href="/windows/desktop/api/winnls/nf-winnls-enumcalendarinfoexa">EnumCalendarInfoEx</a> if designed to run only on Windows Vista and later.</div>
<div> </div>
<div class="alert"><b>Note</b>  This function can enumerate data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.</div>
<div> </div>

## -parameters

### -param pCalInfoEnumProcExEx [in]

Pointer to an application-defined callback function. For more information, see <a href="/previous-versions/windows/desktop/legacy/dd317808(v=vs.85)">EnumCalendarInfoProcExEx</a>.

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

### -param Calendar [in]

<a href="/windows/desktop/Intl/calendar-identifiers">Calendar identifier</a> that specifies the calendar for which information is requested. Note that this identifier can be ENUM_ALL_CALENDARS, to enumerate all calendars that are associated with the locale.

### -param lpReserved [in, optional]

Reserved; must be <b>NULL</b>.

### -param CalType [in]

Type of calendar information. For more information, see <a href="/windows/desktop/Intl/calendar-type-information">Calendar Type Information</a>. Only one calendar type can be specified per call to this function, except where noted.

### -param lParam [in]

Application-provided parameter to pass to the callback function. This value is especially useful for multi-threaded applications.

## -returns

Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

This function enumerates calendar information for all applicable calendars for the specified locale, or for a single requested calendar, depending on the value of the <i>Calendar</i> parameter. The function enumerates the calendar information by calling the specified application-defined callback function. It passes the callback function a pointer to a buffer containing the requested calendar information, a calendar identifier, and an application-defined parameter that is useful for multi-threaded applications. This process continues until <b>EnumCalendarInfoExEx</b> finds the last applicable calendar or the callback function returns <b>FALSE</b>.

<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="/uwp/api/Windows.Globalization">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="/windows/desktop/api/winnls/nf-winnls-resolvelocalename">ResolveLocaleName</a>.

## -see-also

<a href="/windows/desktop/Intl/calendar-type-information">Calendar Type Information</a>



<a href="/windows/desktop/api/winnls/nf-winnls-enumcalendarinfoa">EnumCalendarInfo</a>



<a href="/windows/desktop/api/winnls/nf-winnls-enumcalendarinfoexa">EnumCalendarInfoEx</a>



<a href="/previous-versions/windows/desktop/legacy/dd317808(v=vs.85)">EnumCalendarInfoProcExEx</a>



<a href="/windows/desktop/api/winnls/nf-winnls-enumdateformatsexex">EnumDateFormatsExEx</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>