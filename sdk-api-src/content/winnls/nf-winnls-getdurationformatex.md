---
UID: NF:winnls.GetDurationFormatEx
title: GetDurationFormatEx function (winnls.h)
description: Formats a duration of time as a time string for a locale specified by name.
helpviewer_keywords: ["GetDurationFormatEx","GetDurationFormatEx function [Internationalization for Windows Applications]","_win32_GetDurationFormatEx","d","f","h or H","hh or HH","intl.getdurationformatex","m","mm","s","ss","winnls/GetDurationFormatEx"]
old-location: intl\getdurationformatex.htm
tech.root: Intl
ms.assetid: 82027deb-ffaa-43ec-981e-ffbedb204bcb
ms.date: 12/05/2018
ms.keywords: GetDurationFormatEx, GetDurationFormatEx function [Internationalization for Windows Applications], _win32_GetDurationFormatEx, d, f, h or H, hh or HH, intl.getdurationformatex, m, mm, s, ss, winnls/GetDurationFormatEx
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
 - GetDurationFormatEx
 - winnls/GetDurationFormatEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-DateTime-L1-1-2.dll
 - KernelBase.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetDurationFormatEx
---

# GetDurationFormatEx function


## -description

Formats a duration of time as a time string for a locale specified by name.
<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="/windows/desktop/api/winnls/nf-winnls-getdurationformat">GetDurationFormat</a> if designed to run only on Windows Vista and later.</div><div> </div><div class="alert"><b>Note</b>  This function can format data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.</div><div> </div>

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

Flags specifying function options. If <i>lpFormat</i> is not set to <b>NULL</b>, this parameter must be set to 0. If <i>lpFormat</i> is set to <b>NULL</b>, your application can specify <a href="/windows/desktop/Intl/locale-nouseroverride">LOCALE_NOUSEROVERRIDE</a> to format the string using the system default duration format for the specified locale.

<div class="alert"><b>Caution</b>  Use of <b>LOCALE_NOUSEROVERRIDE</b> is strongly discouraged as it disables user preferences.</div>
<div> </div>

### -param lpDuration [in, optional]

Pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the time duration information to format. The application sets this parameter to <b>NULL</b> if the function is to ignore it and use <i>ullDuration</i>.

### -param ullDuration [in]

64-bit unsigned integer that represents the number of 100-nanosecond intervals in the duration. If both <i>lpDuration</i> and <i>ullDuration</i> are set, the <i>lpDuration</i> parameter takes precedence. If <i>lpDuration</i> is set to <b>NULL</b> and <i>ullDuration</i> is set to 0, the duration is 0.

### -param lpFormat [in, optional]

Pointer to the format string with characters as shown below. The application can set this parameter to <b>NULL</b> if the function is to format the string according to the duration format for the specified locale. If <i>lpFormat</i> is not set to <b>NULL</b>, the function uses the locale only for information not specified in the format picture string.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="d"></a><a id="D"></a><dl>
<dt><b>d</b></dt>
</dl>
</td>
<td width="60%">
days

</td>
</tr>
<tr>
<td width="40%"><a id="h_or_H"></a><a id="h_or_h"></a><a id="H_OR_H"></a><dl>
<dt><b>h or H</b></dt>
</dl>
</td>
<td width="60%">
hours

</td>
</tr>
<tr>
<td width="40%"><a id="hh_or_HH"></a><a id="hh_or_hh"></a><a id="HH_OR_HH"></a><dl>
<dt><b>hh or HH</b></dt>
</dl>
</td>
<td width="60%">
hours; if less than ten,  prepend a leading zero

</td>
</tr>
<tr>
<td width="40%"><a id="m"></a><a id="M"></a><dl>
<dt><b>m</b></dt>
</dl>
</td>
<td width="60%">
minutes

</td>
</tr>
<tr>
<td width="40%"><a id="mm"></a><a id="MM"></a><dl>
<dt><b>mm</b></dt>
</dl>
</td>
<td width="60%">
minutes; if less than ten, prepend a leading zero

</td>
</tr>
<tr>
<td width="40%"><a id="s"></a><a id="S"></a><dl>
<dt><b>s</b></dt>
</dl>
</td>
<td width="60%">
seconds

</td>
</tr>
<tr>
<td width="40%"><a id="ss"></a><a id="SS"></a><dl>
<dt><b>ss</b></dt>
</dl>
</td>
<td width="60%">
seconds; if less than ten, prepend a leading zero

</td>
</tr>
<tr>
<td width="40%"><a id="f"></a><a id="F"></a><dl>
<dt><b>f</b></dt>
</dl>
</td>
<td width="60%">
fractions of a second


<div class="alert"><b>Note</b>  The character "f" can occur up to nine consecutive times (fffffffff), although support for frequency timers is limited to 100 nanoseconds. Thus, if nine characters are present, the last two digits are always 0.</div>
<div> </div>


</td>
</tr>
</table>

### -param lpDurationStr [out, optional]

Pointer to the buffer in which the function retrieves the duration string.

Alternatively, this parameter retrieves <b>NULL</b> if <i>cchDuration</i> is set to 0. In this case, the function returns the required size for the duration string buffer.

### -param cchDuration [in]

Size, in characters, of the buffer indicated by <i>lpDurationStr</i>.

Alternatively, the application can set this parameter to 0. In this case, the function retrieves <b>NULL</b> in <i>lpDurationStr</i> and returns the required size for the duration string buffer.

## -returns

Returns the number of characters retrieved in the buffer indicated by <i>lpDurationStr</i> if successful. If <i>lpDurationStr</i> is set to <b>NULL</b> and <i>cchDuration</i> is set to 0, the function returns the required size for the duration string buffer, including the terminating null character. For example, if 10 characters are written to the buffer, the function returns 11 to include the terminating null character.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li><b>ERROR_INSUFFICIENT_BUFFER</b>. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>.</li>
<li><b>ERROR_INVALID_PARAMETER</b>. Any of the parameter values was invalid.</li>
</ul>

## -remarks

This function can be used with multimedia applications that display file time and sporting event applications that display finish times.

The function ignores the first three members of the [SYSTEMTIME](https://learn.microsoft.com/en-us/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure: **wYear**, **wMonth**, and **wDayOfWeek**.

This function can retrieve data from <a href="/windows/desktop/Intl/custom-locales">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.

The following are characteristics of duration format strings:

<ul>
<li>
Formatting characters are lowercase.

<div class="alert"><b>Note</b>  An exception is made for (H) to be consistent with <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex">GetTimeFormatEx</a>.</div>
<div> </div>
</li>
<li>Two-digit format strings for hours, minutes, and seconds prepend a leading zero if the value is less than 10.</li>
<li>The first output field is not subject to any bounds testing (hours&lt;24, minutes&lt;60, seconds&lt;60, milliseconds&lt;1000). Days are not subject to bounds testing.</li>
<li>The function assumes that all format strings are in decreasing field size, for example, hours, minutes, seconds, milliseconds.</li>
<li>The first field to be displayed is normalized, as defined by the format string. For example, if the application specifies 310 seconds and the format string is m:ss, the output is 5:10. However, if the format string specifies minutes and seconds but the application specifies hours, the minutes field is adjusted accordingly.</li>
<li>If fractions are not the first field, the number of "f" characters in the format string indicates the number of decimals to show (limit of 9). If fractions are the first field, the number of "f" characters indicates the number of significant digits below one second.</li>
<li>Round-off occurs by truncation, not by the rule of five rounds up and four rounds down.</li>
<li>Single quotes are used to escape characters.</li>
</ul>
<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="/uwp/api/Windows.Globalization">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="/windows/desktop/api/winnls/nf-winnls-resolvelocalename">ResolveLocaleName</a>.

<b>Examples</b>

Following are examples of duration formats and corresponding outputs for specified time durations.

<b>SYSTEMTIME = 14 days, 2 hours, 45 minutes, 12 seconds, and 247 milliseconds</b>

<table>
<tr>
<th>Format</th>
<th>Output</th>
</tr>
<tr>
<td>d:hh:mm:ss</td>
<td>14:02:45:12</td>
</tr>
<tr>
<td>hh:mm:ss:ff</td>
<td>338:45:12:24</td>
</tr>
<tr>
<td>hh:mm:ss:fff</td>
<td>338:45:12:247</td>
</tr>
<tr>
<td>h' h 'mm' m 'ss' s'</td>
<td>338 h 45 m 12 s</td>
</tr>
</table>
 

<b>SYSTEMTIME = 345 seconds</b>

<table>
<tr>
<th>Format</th>
<th>Output</th>
</tr>
<tr>
<td>hh:mm:ss</td>
<td>00:05:45</td>
</tr>
<tr>
<td>h:mm:ss</td>
<td>0:05:45</td>
</tr>
<tr>
<td>mm:ss</td>
<td>05:45</td>
</tr>
<tr>
<td>m:ss</td>
<td>5:45</td>
</tr>
<tr>
<td>mm' m 'ss' s'</td>
<td>05 m 45 s</td>
</tr>
<tr>
<td>ss</td>
<td>345</td>
</tr>
<tr>
<td>ss' seconds'</td>
<td>345 seconds</td>
</tr>
</table>
 

<b>uulDuration = 51234567 (5.1234567 seconds)</b>

<table>
<tr>
<th>Format</th>
<th>Output</th>
</tr>
<tr>
<td>s.fff</td>
<td>5.123</td>
</tr>
<tr>
<td>s.ffffff</td>
<td>5.123456</td>
</tr>
<tr>
<td>s.fffffffff</td>
<td>5.123456700 (add trailing zeros)</td>
</tr>
<tr>
<td>fff 'ms'</td>
<td>5123 ms</td>
</tr>
<tr>
<td>ffffff 'microseconds'</td>
<td>5123456 microseconds</td>
</tr>
<tr>
<td>fffffffff 'ns'</td>
<td>5123456700 ns</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex">GetDateFormatEx</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getdurationformat">GetDurationFormat</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoex">GetLocaleInfoEx</a>



<a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex">GetTimeFormatEx</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
