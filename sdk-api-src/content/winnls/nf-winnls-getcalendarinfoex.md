---
UID: NF:winnls.GetCalendarInfoEx
title: GetCalendarInfoEx function (winnls.h)
description: Retrieves information about a calendar for a locale specified by name.Note  The application should call this function in preference to GetCalendarInfo if designed to run only on Windows Vista and later. Note  This function can retrieve data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see Using Persistent Locale Data.
helpviewer_keywords: ["GetCalendarInfoEx","GetCalendarInfoEx function [Internationalization for Windows Applications]","_win32_GetCalendarInfoEx","intl.getcalendarinfoex","winnls/GetCalendarInfoEx"]
old-location: intl\getcalendarinfoex.htm
tech.root: Intl
ms.assetid: b3c2fb74-0559-4752-9bdb-36b78084aed5
ms.date: 12/05/2018
ms.keywords: GetCalendarInfoEx, GetCalendarInfoEx function [Internationalization for Windows Applications], _win32_GetCalendarInfoEx, intl.getcalendarinfoex, winnls/GetCalendarInfoEx
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - GetCalendarInfoEx
 - winnls/GetCalendarInfoEx
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
 - GetCalendarInfoEx
---

# GetCalendarInfoEx function


## -description

Retrieves information about a calendar for a locale specified by name.<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="/windows/desktop/api/winnls/nf-winnls-getcalendarinfoa">GetCalendarInfo</a> if designed to run only on Windows Vista and later.</div>
<div> </div>
<div class="alert"><b>Note</b>  This function can retrieve data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.</div>
<div> </div>

## -parameters

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

<a href="/windows/desktop/Intl/calendar-identifiers">Calendar identifier</a>.

### -param lpReserved [in, optional]

Reserved; must be <b>NULL</b>.

### -param CalType [in]

Type of information to retrieve. For more information, see <a href="/windows/desktop/Intl/calendar-type-information">Calendar Type Information</a>. 
			 

<div class="alert"><b>Note</b>  <b>GetCalendarInfoEx</b> returns only one string if this parameter specifies CAL_IYEAROFFSETRANGE or CAL_SERASTRING. In both cases the current era is returned.</div>
<div> </div>
For CAL_NOUSEROVERRIDE, the function ignores any value set by <a href="/windows/desktop/api/winnls/nf-winnls-setcalendarinfoa">SetCalendarInfo</a> and uses the database settings for the current system default locale. This type is relevant only in the combination CAL_NOUSEROVERRIDE | CAL_ITWODIGITYEARMAX. CAL_ITWODIGITYEARMAX is the only value that can be set by <b>SetCalendarInfo</b>.

### -param lpCalData [out, optional]

Pointer to a buffer in which this function retrieves the requested data as a string. If CAL_RETURN_NUMBER is specified in <i>CalType</i>, this parameter must retrieve <b>NULL</b>.

### -param cchData [in]

Size, in characters, of the <i>lpCalData</i> buffer. The application can set this parameter to 0 to return the required size for the calendar data buffer. In this case, the <i>lpCalData</i> parameter is not used. If CAL_RETURN_NUMBER is specified for <i>CalType</i>, the value of <i>cchData</i> must be 0.

### -param lpValue [out, optional]

Pointer to a variable that receives the requested data as a number. If CAL_RETURN_NUMBER is specified in <i>CalType</i>, then <i>lpValue</i> must not be <b>NULL</b>. If CAL_RETURN_NUMBER is not specified in <i>CalType</i>, then <i>lpValue</i> must be <b>NULL</b>.

## -returns

Returns the number of characters retrieved in the <i>lpCalData</i> buffer if successful. If the function succeeds, <i>cchData</i> is set to 0, and CAL_RETURN_NUMBER is not specified, the return value is the size of the buffer required to hold the locale information. If the function succeeds, <i>cchData</i> is set to 0, and CAL_RETURN_NUMBER is specified, the return value is the size of the value written to the <i>lpValue</i> parameter. This size is always 2.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

<div class="alert"><b>Note</b>  This API is being updated to support the May 2019 Japanese era change. If your application supports the Japanese calendar, you should validate that it properly handles the new era. See <a href="/windows/uwp/design/globalizing/japanese-era-change">Prepare your application for the Japanese era change</a> for more information.</div>
<div> </div>
<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="/uwp/api/Windows.Globalization">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="/windows/desktop/api/winnls/nf-winnls-resolvelocalename">ResolveLocaleName</a>.

## -see-also

<a href="/windows/desktop/Intl/calendar-type-information">Calendar Type Information</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getcalendarinfoa">GetCalendarInfo</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>



<a href="/windows/desktop/api/winnls/nf-winnls-setcalendarinfoa">SetCalendarInfo</a>