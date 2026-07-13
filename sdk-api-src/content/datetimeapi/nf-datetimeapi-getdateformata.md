---
UID: NF:datetimeapi.GetDateFormatA
title: GetDateFormatA function (datetimeapi.h)
description: Formats a date as a date string for a locale specified by the locale identifier. (ANSI)
helpviewer_keywords: ["GetDateFormatA", "datetimeapi/GetDateFormatA"]
old-location: intl\getdateformat.htm
tech.root: Intl
ms.assetid: 546cede1-1702-403a-bba3-b5cd3b35a1bf
ms.date: 12/05/2018
ms.keywords: GetDateFormat, GetDateFormat function [Internationalization for Windows Applications], GetDateFormatA, GetDateFormatW, _win32_GetDateFormat, datetimeapi/GetDateFormat, datetimeapi/GetDateFormatA, datetimeapi/GetDateFormatW, intl.getdateformat
req.header: datetimeapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetDateFormatW (Unicode) and GetDateFormatA (ANSI)
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
 - GetDateFormatA
 - datetimeapi/GetDateFormatA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-datetime-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-datetime-l1-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-DateTime-L1-1-2.dll
api_name:
 - GetDateFormat
 - GetDateFormatA
 - GetDateFormatW
---

# GetDateFormatA function


## -description

Formats a date as a date string for a locale specified by the locale identifier. The function formats either a specified date or the local system date.
      <div class="alert"><b>Note</b>  For interoperability reasons, the application should prefer the <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex">GetDateFormatEx</a> function to <b>GetDateFormat</b> because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. Any application that will be run only on Windows Vista and later should use <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex">GetDateFormatEx</a>.</div>
<div> </div>

## -parameters

### -param Locale [in]

<a href="/windows/desktop/Intl/locale-identifiers">Locale identifier</a> that specifies the locale this function formats the date string for. You can use the <a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

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

### -param dwFlags [in]

Flags specifying date format options. For detailed definitions, see the <i>dwFlags</i> parameter of <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex">GetDateFormatEx</a>.

### -param lpDate [in, optional]

Pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the date information to format. The application sets this parameter to <b>NULL</b> if the function is to use the current local system date.

### -param lpFormat [in, optional]

Pointer to a format picture string that is used to form the date. Possible values for the format picture string are defined in <a href="/windows/desktop/Intl/day--month--year--and-era-format-pictures">Day, Month, Year, and Era Format Pictures</a>.

The function uses the specified locale only for information not specified in the format picture string, for example, the day and month names for the locale. The application can set this parameter to <b>NULL</b> to format the string according to the date format for the specified locale.

### -param lpDateStr [out, optional]

Pointer to a buffer in which this function retrieves the formatted date string.

### -param cchDate [in]

Size, in characters, of the <i>lpDateStr</i> buffer. The application can set this parameter to 0 to return the buffer size required to hold the formatted date string. In this case, the buffer indicated by <i>lpDateStr</i> is not used.

## -returns

Returns the number of characters written to the <i>lpDateStr</i> buffer if successful. If the <i>cchDate</i> parameter is set to 0, the function returns the number of characters required to hold the formatted date string, including the terminating null character.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

<div class="alert"><b>Note</b>  This API is being updated to support the May 2019 Japanese era change. If your application supports the Japanese calendar, you should validate that it properly handles the new era. See <a href="/windows/uwp/design/globalizing/japanese-era-change">Prepare your application for the Japanese era change</a> for more information.</div>
<div> </div>
See Remarks for <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex">GetDateFormatEx</a>.

When the ANSI version of this function is used with a Unicode-only locale identifier, the function can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark ("?"). 
      

<b>Starting with Windows 8: </b><b>GetDateFormat</b>  is declared in Datetimeapi.h. Before Windows 8, it was declared in Winnls.h.





> [!NOTE]
> The datetimeapi.h header defines GetDateFormat as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Intl/day--month--year--and-era-format-pictures">Day, Month, Year, and Era Format Pictures</a>



<a href="/windows/desktop/api/winnls/nf-winnls-enumcalendarinfoa">EnumCalendarInfo</a>



<a href="/windows/desktop/api/winnls/nf-winnls-enumdateformatsexa">EnumDateFormatsEx</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getcalendarinfoa">GetCalendarInfo</a>



<a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex">GetDateFormatEx</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoa">GetLocaleInfo</a>



<a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata">GetTimeFormat</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
