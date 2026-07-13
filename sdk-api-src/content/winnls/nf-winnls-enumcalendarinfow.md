---
UID: NF:winnls.EnumCalendarInfoW
title: EnumCalendarInfoW function (winnls.h)
description: Enumerates calendar information for a specified locale.Note  To receive a calendar identifier in addition to calendar information, the application should use the EnumCalendarInfoEx function. (Unicode)
helpviewer_keywords: ["EnumCalendarInfo", "EnumCalendarInfo function [Internationalization for Windows Applications]", "EnumCalendarInfoW", "_win32_EnumCalendarInfo", "intl.enumcalendarinfo", "winnls/EnumCalendarInfo", "winnls/EnumCalendarInfoW"]
old-location: intl\enumcalendarinfo.htm
tech.root: Intl
ms.assetid: b38abdc9-6c03-4077-9d42-c7cb6d5c66ee
ms.date: 12/05/2018
ms.keywords: EnumCalendarInfo, EnumCalendarInfo function [Internationalization for Windows Applications], EnumCalendarInfoA, EnumCalendarInfoW, _win32_EnumCalendarInfo, intl.enumcalendarinfo, winnls/EnumCalendarInfo, winnls/EnumCalendarInfoA, winnls/EnumCalendarInfoW
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumCalendarInfoW (Unicode) and EnumCalendarInfoA (ANSI)
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
 - EnumCalendarInfoW
 - winnls/EnumCalendarInfoW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-Localization-l2-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - EnumCalendarInfo
 - EnumCalendarInfoA
 - EnumCalendarInfoW
---

# EnumCalendarInfoW function


## -description

Enumerates calendar information for a specified locale.
<div class="alert"><b>Note</b>  To receive a calendar identifier in addition to calendar information, the application should use the <a href="/windows/desktop/api/winnls/nf-winnls-enumcalendarinfoexa">EnumCalendarInfoEx</a> function. Another reason for preferring this function is that Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales, for interoperability reasons.</div><div> </div><div class="alert"><b>Note</b>  Any application that will be run only on Windows Vista and later should use <a href="/windows/desktop/api/winnls/nf-winnls-enumcalendarinfoexex">EnumCalendarInfoExEx</a> in preference to <b>EnumCalendarInfo</b>.</div><div> </div>

## -parameters

### -param lpCalInfoEnumProc [in]

Pointer to an application-defined callback function. For more information, see <a href="/previous-versions/windows/desktop/legacy/dd317806(v=vs.85)">EnumCalendarInfoProc</a>.

### -param Locale [in]

<a href="/windows/desktop/Intl/locale-identifiers">Locale identifier</a> that specifies the locale for which to retrieve calendar information. You can use the <a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

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

See Remarks for <a href="/windows/desktop/api/winnls/nf-winnls-enumcalendarinfoexa">EnumCalendarInfoEx</a>.





> [!NOTE]
> The winnls.h header defines EnumCalendarInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Intl/calendar-type-information">Calendar Type Information</a>



<a href="/windows/desktop/api/winnls/nf-winnls-enumcalendarinfoexa">EnumCalendarInfoEx</a>



<a href="/windows/desktop/api/winnls/nf-winnls-enumcalendarinfoexex">EnumCalendarInfoExEx</a>



<a href="/previous-versions/windows/desktop/legacy/dd317806(v=vs.85)">EnumCalendarInfoProc</a>



<a href="/windows/desktop/api/winnls/nf-winnls-enumdateformatsa">EnumDateFormats</a>



<a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
