---
UID: NF:datetimeapi.GetTimeFormatEx
title: GetTimeFormatEx function (datetimeapi.h)
description: Formats time as a time string for a locale specified by name.
helpviewer_keywords: ["GetTimeFormatEx","GetTimeFormatEx function [Internationalization for Windows Applications]","TIME_FORCE24HOURFORMAT","TIME_NOMINUTESORSECONDS","TIME_NOSECONDS","TIME_NOTIMEMARKER","_win32_GetTimeFormatEx","datetimeapi/GetTimeFormatEx","intl.gettimeformatex"]
old-location: intl\gettimeformatex.htm
tech.root: Intl
ms.assetid: 4d63888e-4496-4315-ac87-bf60c54daa37
ms.date: 12/05/2018
ms.keywords: GetTimeFormatEx, GetTimeFormatEx function [Internationalization for Windows Applications], TIME_FORCE24HOURFORMAT, TIME_NOMINUTESORSECONDS, TIME_NOSECONDS, TIME_NOTIMEMARKER, _win32_GetTimeFormatEx, datetimeapi/GetTimeFormatEx, intl.gettimeformatex
req.header: datetimeapi.h
req.include-header: 
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
 - GetTimeFormatEx
 - datetimeapi/GetTimeFormatEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-datetime-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-DateTime-L1-1-2.dll
api_name:
 - GetTimeFormatEx
---

# GetTimeFormatEx function


## -description

Formats time as a time string for a locale specified by name. The function formats either a specified time or the local system time.<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata">GetTimeFormat</a> if designed to run only on Windows Vista and later.</div>
<div> </div>
<div class="alert"><b>Note</b>  This function can format data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.</div>
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

### -param dwFlags [in]

Flags specifying time format options. The application can specify a combination of the following values and <a href="/windows/desktop/Intl/locale-use-cp-acp">LOCALE_USE_CP_ACP</a> or <a href="/windows/desktop/Intl/locale-nouseroverride">LOCALE_NOUSEROVERRIDE</a>.

<div class="alert"><b>Caution</b>  Use of <a href="/windows/desktop/Intl/locale-nouseroverride">LOCALE_NOUSEROVERRIDE</a> is strongly discouraged as it disables user preferences.</div>
<div> </div>
<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TIME_NOMINUTESORSECONDS"></a><a id="time_nominutesorseconds"></a><dl>
<dt><b>TIME_NOMINUTESORSECONDS</b></dt>
</dl>
</td>
<td width="60%">
Do not use minutes or seconds.

</td>
</tr>
<tr>
<td width="40%"><a id="TIME_NOSECONDS"></a><a id="time_noseconds"></a><dl>
<dt><b>TIME_NOSECONDS</b></dt>
</dl>
</td>
<td width="60%">
Do not use seconds.

</td>
</tr>
<tr>
<td width="40%"><a id="TIME_NOTIMEMARKER"></a><a id="time_notimemarker"></a><dl>
<dt><b>TIME_NOTIMEMARKER</b></dt>
</dl>
</td>
<td width="60%">
Do not use a time marker.

</td>
</tr>
<tr>
<td width="40%"><a id="TIME_FORCE24HOURFORMAT"></a><a id="time_force24hourformat"></a><dl>
<dt><b>TIME_FORCE24HOURFORMAT</b></dt>
</dl>
</td>
<td width="60%">
Always use a 24-hour time format.

</td>
</tr>
</table>

### -param lpTime [in, optional]

Pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the time information to format. The application can set this parameter to <b>NULL</b> if the function is to use the current local system time.

### -param lpFormat [in, optional]

Pointer to a format picture to use to format the time string. If the application sets this parameter to <b>NULL</b>, the function formats the string according to the time format of the specified locale. If the application does not set the parameter to <b>NULL</b>, the function uses the locale only for information not specified in the format picture string, for example, the locale-specific time markers. For information about the format picture string, see the Remarks section.

### -param lpTimeStr [out, optional]

Pointer to a buffer in which this function retrieves the formatted time string.

### -param cchTime [in]

Size, in characters, for the time string buffer indicated by <i>lpTimeStr</i>. Alternatively, the application can set this parameter to 0. In this case, the function returns the required size for the time string buffer, and does not use the <i>lpTimeStr</i> parameter.

## -returns

Returns the number of characters retrieved in the buffer indicated by <i>lpTimeStr</i>. If the <i>cchTime</i> parameter is set to 0, the function returns the size of the buffer required to hold the formatted time string, including a terminating null character.

This function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
<li>ERROR_OUTOFMEMORY. Not enough storage was available to complete this operation.</li>
</ul>

## -remarks

If a time marker exists and the TIME_NOTIMEMARKER flag is not set, the function localizes the time marker based on the specified locale identifier. Examples of time markers are "AM" and "PM" for English (United States).

The time values in the structure indicated by <i>lpTime</i> must be valid. The function checks each of the time values to determine that it is within the appropriate range of values. If any of the time values are outside the correct range, the function fails, and sets the last error to ERROR_INVALID_PARAMETER.

The function ignores the date members of the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure. These include: <b>wYear</b>, <b>wMonth</b>, <b>wDayOfWeek</b>, and <b>wDay</b>.

If TIME_NOMINUTESORSECONDS or TIME_NOSECONDS is specified, the function removes the separators following the minutes and/or seconds members.

If TIME_NOTIMEMARKER is specified, the function removes the separators preceding and following the time marker.

If TIME_FORCE24HOURFORMAT is specified, the function displays any existing time marker, unless the TIME_NOTIMEMARKER flag is also set.

The function does not include milliseconds as part of the formatted time string.

The function returns no errors for a bad format string, but just forms the best possible time string. If more than two hour, minute, second, or time marker format pictures are passed in, the function defaults to two. For example, the only time marker pictures that are valid are "t" and "tt". If "ttt" is passed in, the function assumes "tt".

To obtain the time format without performing any actual formatting, the application should use the <a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoex">GetLocaleInfoEx</a> function, specifying <a href="/windows/desktop/Intl/locale-stime-constants">LOCALE_STIMEFORMAT</a>.

The application can use the following elements to construct a format picture string. If spaces are used to separate the elements in the format string, these spaces appear in the same location in the output string. The letters must be in uppercase or lowercase as shown, for example, "ss", not "SS". Characters in the format string that are enclosed in single quotation marks appear in the same location and unchanged in the output string.

<table>
<tr>
<th>Picture</th>
<th>Meaning</th>
</tr>
<tr>
<td>h</td>
<td>Hours with no leading zero for single-digit hours; 12-hour clock</td>
</tr>
<tr>
<td>hh</td>
<td>Hours with leading zero for single-digit hours; 12-hour clock</td>
</tr>
<tr>
<td>H</td>
<td>Hours with no leading zero for single-digit hours; 24-hour clock</td>
</tr>
<tr>
<td>HH</td>
<td>Hours with leading zero for single-digit hours; 24-hour clock</td>
</tr>
<tr>
<td>m</td>
<td>Minutes with no leading zero for single-digit minutes</td>
</tr>
<tr>
<td>mm</td>
<td>Minutes with leading zero for single-digit minutes</td>
</tr>
<tr>
<td>s</td>
<td>Seconds with no leading zero for single-digit seconds</td>
</tr>
<tr>
<td>ss</td>
<td>Seconds with leading zero for single-digit seconds</td>
</tr>
<tr>
<td>t</td>
<td>One character time marker string, such as A or P</td>
</tr>
<tr>
<td>tt</td>
<td>Multi-character time marker string, such as AM or PM</td>
</tr>
</table>
 

For example, to get the time string


``` syntax
"11:29:40 PM"
```

the application should use the picture string


``` syntax
"hh':'mm':'ss tt"
```

This function can retrieve data from <a href="/windows/desktop/Intl/custom-locales">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.

<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="/uwp/api/Windows.Globalization">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="/windows/desktop/api/winnls/nf-winnls-resolvelocalename">ResolveLocaleName</a>.

<b>Beginning in Windows 8: </b><b>GetTimeFormatEx</b>  is declared in Datetimeapi.h. Before Windows 8, it was declared in Winnls.h.

## -see-also

<a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex">GetDateFormatEx</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoex">GetLocaleInfoEx</a>



<a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata">GetTimeFormat</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
