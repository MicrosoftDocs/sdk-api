---
UID: NF:winnls.SetCalendarInfoA
title: SetCalendarInfoA function (winnls.h)
description: Sets an item of locale information for a calendar. For more information, see Date and Calendar. (ANSI)
helpviewer_keywords: ["SetCalendarInfoA", "winnls/SetCalendarInfoA"]
old-location: intl\setcalendarinfo.htm
tech.root: Intl
ms.assetid: 3599f68f-5b7c-4bf9-9c42-452047c0731f
ms.date: 12/05/2018
ms.keywords: SetCalendarInfo, SetCalendarInfo function [Internationalization for Windows Applications], SetCalendarInfoA, SetCalendarInfoW, _win32_SetCalendarInfo, intl.setcalendarinfo, winnls/SetCalendarInfo, winnls/SetCalendarInfoA, winnls/SetCalendarInfoW
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetCalendarInfoW (Unicode) and SetCalendarInfoA (ANSI)
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
 - SetCalendarInfoA
 - winnls/SetCalendarInfoA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Localization-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
 - API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - SetCalendarInfo
 - SetCalendarInfoA
 - SetCalendarInfoW
---

# SetCalendarInfoA function


## -description

Sets an item of locale information for a calendar. For more information, see <a href="/windows/desktop/Intl/date-and-calendar">Date and Calendar</a>.

## -parameters

### -param Locale [in]

<a href="/windows/desktop/Intl/locale-identifiers">Locale identifier</a> that specifies the locale. You can use the <a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values.

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
The following custom locale identifiers are also supported.

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

<a href="/windows/desktop/Intl/calendar-identifiers">Calendar identifier</a> for the calendar for which to set information.

### -param CalType [in]

Type of calendar information to set. Only the following CALTYPE values are valid for this function. The CAL_USE_CP_ACP constant is only meaningful for the ANSI version of the function.

<ul>
<li>CAL_USE_CP_ACP</li>
<li>CAL_ITWODIGITYEARMAX</li>
</ul>
The application can specify only one calendar identifier per call to this function. An exception can be made if the application uses the binary OR operator to combine CAL_USE_CP_ACP with any valid CALTYPE value defined in <a href="/windows/desktop/Intl/calendar-type-information">Calendar Type Information</a>.

### -param lpCalData [in]

Pointer to a null-terminated calendar information string. The information must be in the format of the specified calendar type.

## -returns

Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INTERNAL_ERROR. An unexpected error occurred in the function.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

This function only affects the user override portion of the calendar settings. It does not set the system defaults.

Calendar information is always passed as a null-terminated Unicode string in the Unicode version of this function, and as a null-terminated ANSI string in the ANSI version. No integers are allowed by this function. Any numeric values must be specified as either Unicode or ANSI text.

When the ANSI version of this function is used with a Unicode-only locale identifier, the function can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark (?). 

CAL_ITWODIGITYEARMAX can be used with any calendar, even if the calendar is not supported for the specified locale. To avoid complications, the application should call <a href="/windows/desktop/api/winnls/nf-winnls-enumcalendarinfoa">EnumCalendarInfo</a> to ensure that the calendar is supported for the locale of interest.





> [!NOTE]
> The winnls.h header defines SetCalendarInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-enumcalendarinfoa">EnumCalendarInfo</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getcalendarinfoa">GetCalendarInfo</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
