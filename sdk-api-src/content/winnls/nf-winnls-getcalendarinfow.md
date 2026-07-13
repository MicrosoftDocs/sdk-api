---
UID: NF:winnls.GetCalendarInfoW
title: GetCalendarInfoW function (winnls.h)
description: Retrieves information about a calendar for a locale specified by identifier. (Unicode)
helpviewer_keywords: ["GetCalendarInfo", "GetCalendarInfo function [Internationalization for Windows Applications]", "GetCalendarInfoW", "_win32_GetCalendarInfo", "intl.getcalendarinfo", "winnls/GetCalendarInfo", "winnls/GetCalendarInfoW"]
old-location: intl\getcalendarinfo.htm
tech.root: Intl
ms.assetid: f32ca0d0-8fa2-41e5-9835-76cf51426c3b
ms.date: 12/05/2018
ms.keywords: GetCalendarInfo, GetCalendarInfo function [Internationalization for Windows Applications], GetCalendarInfoA, GetCalendarInfoW, _win32_GetCalendarInfo, intl.getcalendarinfo, winnls/GetCalendarInfo, winnls/GetCalendarInfoA, winnls/GetCalendarInfoW
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetCalendarInfoW (Unicode) and GetCalendarInfoA (ANSI)
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
 - GetCalendarInfoW
 - winnls/GetCalendarInfoW
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
 - API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - GetCalendarInfo
 - GetCalendarInfoA
 - GetCalendarInfoW
---

# GetCalendarInfoW function


## -description

Retrieves information about a calendar for a locale specified by identifier.
<div class="alert"><b>Note</b>  For interoperability reasons, the application should prefer the <a href="/windows/desktop/api/winnls/nf-winnls-getcalendarinfoex">GetCalendarInfoEx</a> function to <b>GetCalendarInfo</b> because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. Any application that runs only on Windows Vista and later should use <a href="/windows/desktop/api/winnls/nf-winnls-getcalendarinfoex">GetCalendarInfoEx</a>.</div><div> </div>

## -parameters

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

<a href="/windows/desktop/Intl/calendar-identifiers">Calendar identifier</a>.

### -param CalType [in]

Type of information to retrieve. For more information, see <a href="/windows/desktop/Intl/calendar-type-information">Calendar Type Information</a>. 

<div class="alert"><b>Note</b>  <b>GetCalendarInfo</b> returns only one string if this parameter specifies CAL_IYEAROFFSETRANGE or CAL_SERASTRING. In both cases the current era is returned.</div>
<div> </div>
CAL_USE_CP_ACP is relevant only for the ANSI version of this function.

For CAL_NOUSEROVERRIDE, the function ignores any value set by <a href="/windows/desktop/api/winnls/nf-winnls-setcalendarinfoa">SetCalendarInfo</a> and uses the database settings for the current system default locale. This type is relevant only in the combination CAL_NOUSEROVERRIDE | CAL_ITWODIGITYEARMAX. CAL_ITWODIGITYEARMAX is the only value that can be set by <b>SetCalendarInfo</b>.

### -param lpCalData [out, optional]

Pointer to a buffer in which this function retrieves the requested data as a string. If CAL_RETURN_NUMBER is specified in <i>CalType</i>, this parameter must retrieve <b>NULL</b>.

### -param cchData [in]

Size, in characters, of the <i>lpCalData</i> buffer. The application can set this parameter to 0 to return the required size for the calendar data buffer. In this case, the <i>lpCalData</i> parameter is not used. If CAL_RETURN_NUMBER is specified for <i>CalType</i>, the value of <i>cchData</i> must be 0.

### -param lpValue [out, optional]

Pointer to a variable that receives the requested data as a number. If CAL_RETURN_NUMBER is specified in <i>CalType</i>, then <i>lpValue</i> must not be <b>NULL</b>. If CAL_RETURN_NUMBER is not specified in <i>CalType</i>, then <i>lpValue</i> must be <b>NULL</b>.

## -returns

Returns the number of characters retrieved in the <i>lpCalData</i> buffer, with <i>cchData</i> set to a nonzero value, if successful. If the function succeeds, <i>cchData</i> is set to 0, and CAL_RETURN_NUMBER is not specified, the return value is the size of the buffer required to hold the calendar information. If the function succeeds, <i>cchData</i> is set 0, and CAL_RETURN_NUMBER is specified, the return value is the size of the value retrieved in <i>lpValue</i>, that is, 2 for the Unicode version of the function or 4 for the ANSI version.

This function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

<div class="alert"><b>Note</b>  This API is being updated to support the May 2019 Japanese era change. If your application supports the Japanese calendar, you should validate that it properly handles the new era. See <a href="/windows/uwp/design/globalizing/japanese-era-change">Prepare your application for the Japanese era change</a> for more information.</div>
<div> </div>
When the ANSI version of this function is used with a Unicode-only locale identifier, the function can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark (?). 





> [!NOTE]
> The winnls.h header defines GetCalendarInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Intl/calendar-type-information">Calendar Type Information</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getcalendarinfoex">GetCalendarInfoEx</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>



<a href="/windows/desktop/api/winnls/nf-winnls-setcalendarinfoa">SetCalendarInfo</a>
