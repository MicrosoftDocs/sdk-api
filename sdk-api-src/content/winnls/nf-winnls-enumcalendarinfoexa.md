---
UID: NF:winnls.EnumCalendarInfoExA
title: EnumCalendarInfoExA function (winnls.h)
description: Enumerates calendar information for a locale specified by identifier.Note  Any application that runs only on Windows Vista and later should use EnumCalendarInfoExEx in preference to this function. (ANSI)
helpviewer_keywords: ["EnumCalendarInfoExA", "winnls/EnumCalendarInfoExA"]
old-location: intl\enumcalendarinfoex.htm
tech.root: Intl
ms.assetid: 5a313af5-e595-49b1-9651-a5afc158c7a7
ms.date: 12/05/2018
ms.keywords: EnumCalendarInfoEx, EnumCalendarInfoEx function [Internationalization for Windows Applications], EnumCalendarInfoExA, EnumCalendarInfoExW, _win32_EnumCalendarInfoEx, intl.enumcalendarinfoex, winnls/EnumCalendarInfoEx, winnls/EnumCalendarInfoExA, winnls/EnumCalendarInfoExW
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumCalendarInfoExW (Unicode) and EnumCalendarInfoExA (ANSI)
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
 - EnumCalendarInfoExA
 - winnls/EnumCalendarInfoExA
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
 - API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - EnumCalendarInfoEx
 - EnumCalendarInfoExA
 - EnumCalendarInfoExW
---

# EnumCalendarInfoExA function


## -description

Enumerates calendar information for a locale specified by identifier.
<div class="alert"><b>Note</b>  Any application that runs only on Windows Vista and later should use <a href="/windows/desktop/api/winnls/nf-winnls-enumcalendarinfoexex">EnumCalendarInfoExEx</a> in preference to this function.</div><div> </div>

## -parameters

### -param lpCalInfoEnumProcEx [in]

Pointer to an application-defined callback function. For more information, see <a href="/previous-versions/windows/desktop/legacy/dd317807(v=vs.85)">EnumCalendarInfoProcEx</a>.

### -param Locale [in]

<a href="/windows/desktop/Intl/locale-identifiers">Locale identifier</a> that specifies the locale for which to retrieve calendar information. You can use the <a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro to create an identifier or use one of the following predefined values. 

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

### -param Calendar [in]

<a href="/windows/desktop/Intl/calendar-identifiers">Calendar identifier</a> that specifies the calendar for which information is requested. Note that this identifier can be ENUM_ALL_CALENDARS, to enumerate all calendars that are associated with the locale.

### -param CalType [in]

Type of calendar information. For more information, see <a href="/windows/desktop/Intl/calendar-type-information">Calendar Type Information</a>. Only one calendar type can be specified per call to this function, except where noted.

## -returns

Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

This function enumerates calendar information for all applicable calendars for the specified locale, or for a single requested calendar, depending on the value of the <i>Calendar</i> parameter. The function enumerates the calendar information by calling the specified application-defined callback function. It passes the callback function a pointer to a buffer containing the requested calendar information. This process continues until <b>EnumCalendarInfoEx</b> finds the last applicable calendar or the callback function returns <b>FALSE</b>.

This function can enumerate data from <a href="/windows/desktop/Intl/custom-locales">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.

When the ANSI version of this function is used with a Unicode-only locale identifier, the function can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark (?).





> [!NOTE]
> The winnls.h header defines EnumCalendarInfoEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Intl/calendar-type-information">Calendar Type Information</a>



<a href="/windows/desktop/api/winnls/nf-winnls-enumcalendarinfoa">EnumCalendarInfo</a>



<a href="/windows/desktop/api/winnls/nf-winnls-enumcalendarinfoexex">EnumCalendarInfoExEx</a>



<a href="/previous-versions/windows/desktop/legacy/dd317807(v=vs.85)">EnumCalendarInfoProcEx</a>



<a href="/windows/desktop/api/winnls/nf-winnls-enumdateformatsa">EnumDateFormats</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
