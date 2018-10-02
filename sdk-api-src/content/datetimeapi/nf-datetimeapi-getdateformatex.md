---
UID: NF:datetimeapi.GetDateFormatEx
title: GetDateFormatEx function
author: windows-sdk-content
description: Formats a date as a date string for a locale specified by name.
old-location: intl\getdateformatex.htm
tech.root: Intl
ms.assetid: 791fb386-3cc5-410e-bfce-52598fdb10c9
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: DATE_AUTOLAYOUT, DATE_LONGDATE, DATE_LTRREADING, DATE_MONTHDAY, DATE_RTLREADING, DATE_SHORTDATE, DATE_USE_ALT_CALENDAR, DATE_YEARMONTH, GetDateFormatEx, GetDateFormatEx function [Internationalization for Windows Applications], _win32_GetDateFormatEx, datetimeapi/GetDateFormatEx, intl.getdateformatex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - GetDateFormatEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetDateFormatEx function


## -description


Formats a date as a date string for a locale specified by name. The function formats either a specified date or the local system date.<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="https://msdn.microsoft.com/546cede1-1702-403a-bba3-b5cd3b35a1bf">GetDateFormat</a> if designed to run only on Windows Vista and later.</div>
<div> </div>
<div class="alert"><b>Note</b>  This function can format data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see <a href="https://msdn.microsoft.com/f62402d6-31de-4ff7-9538-7925a007a089">Using Persistent Locale Data</a>.</div>
<div> </div>



## -parameters




### -param lpLocaleName [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/221aae7b-3a7c-4995-ae78-50d97de436d8">locale name</a>, or one of the following predefined values. 

<ul>
<li>
<a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_INVARIANT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_USER_DEFAULT</a>
</li>
</ul>

### -param dwFlags [in]

Flags specifying various function options that can be set if <i>lpFormat</i> is set to <b>NULL</b>. The application can specify a combination of the following values and <a href="https://msdn.microsoft.com/686ca9f2-515d-449f-8871-77c78ab5c31a">LOCALE_USE_CP_ACP</a> or <a href="https://msdn.microsoft.com/ab68d16b-5e1e-4af3-b048-43975cded00a">LOCALE_NOUSEROVERRIDE</a>.

<div class="alert"><b>Caution</b>  Use of <a href="https://msdn.microsoft.com/ab68d16b-5e1e-4af3-b048-43975cded00a">LOCALE_NOUSEROVERRIDE</a> is strongly discouraged as it disables user preferences.</div>
<div> </div>
<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DATE_AUTOLAYOUT"></a><a id="date_autolayout"></a><dl>
<dt><b>DATE_AUTOLAYOUT</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows 7 and later:</b> Detect the need for right-to-left and left-to-right reading layout using the locale and calendar information, and add marks accordingly. This value cannot be used with DATE_LTRREADING or DATE_RTLREADING. DATE_AUTOLAYOUT is preferred over DATE_LTRREADING and DATE_RTLREADING because it uses the locales and calendars to determine the correct addition of marks.

</td>
</tr>
<tr>
<td width="40%"><a id="DATE_LONGDATE"></a><a id="date_longdate"></a><dl>
<dt><b>DATE_LONGDATE</b></dt>
</dl>
</td>
<td width="60%">
Use the long date format. This value cannot be used with DATE_MONTHDAY, DATE_SHORTDATE, or DATE_YEARMONTH.

</td>
</tr>
<tr>
<td width="40%"><a id="DATE_LTRREADING"></a><a id="date_ltrreading"></a><dl>
<dt><b>DATE_LTRREADING</b></dt>
</dl>
</td>
<td width="60%">
Add marks for left-to-right reading layout. This value cannot be used with DATE_RTLREADING.

</td>
</tr>
<tr>
<td width="40%"><a id="DATE_RTLREADING"></a><a id="date_rtlreading"></a><dl>
<dt><b>DATE_RTLREADING</b></dt>
</dl>
</td>
<td width="60%">
Add marks for right-to-left reading layout. This value cannot be used with DATE_LTRREADING

</td>
</tr>
<tr>
<td width="40%"><a id="DATE_SHORTDATE"></a><a id="date_shortdate"></a><dl>
<dt><b>DATE_SHORTDATE</b></dt>
</dl>
</td>
<td width="60%">
Use the short date format. This is the default. This value cannot be used with DATE_MONTHDAY, DATE_LONGDATE, or DATE_YEARMONTH.

</td>
</tr>
<tr>
<td width="40%"><a id="DATE_USE_ALT_CALENDAR"></a><a id="date_use_alt_calendar"></a><dl>
<dt><b>DATE_USE_ALT_CALENDAR</b></dt>
</dl>
</td>
<td width="60%">
Use the alternate calendar, if one exists, to format the date string. If this flag is set, the function uses the default format for that alternate calendar, rather than using any user overrides. The user overrides will be used only in the event that there is no default format for the specified alternate calendar.

</td>
</tr>
<tr>
<td width="40%"><a id="DATE_YEARMONTH"></a><a id="date_yearmonth"></a><dl>
<dt><b>DATE_YEARMONTH</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista:</b> Use the year/month format. This value cannot be used with DATE_MONTHDAY, DATE_SHORTDATE, or DATE_LONGDATE.

</td>
</tr>
<tr>
<td width="40%"><a id="DATE_MONTHDAY"></a><a id="date_monthday"></a><dl>
<dt><b>DATE_MONTHDAY</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows 10:</b> Use the combination of month and day formats appropriate for the specified locale. This value cannot be used with DATE_YEARMONTH, DATE_SHORTDATE, or DATE_LONGDATE.

</td>
</tr>
</table>
 

If  the application does not specify DATE_YEARMONTH, DATE_MONTHDAY, DATE_SHORTDATE, or DATE_LONGDATE, and <i>lpFormat</i> is set to <b>NULL</b>, DATE_SHORTDATE is the default.


### -param lpDate [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains the date information to format. The application can set this parameter to <b>NULL</b> if the function is to use the current local system date.


### -param lpFormat [in, optional]

Pointer to a format picture string that is used to form the date. Possible values for the format picture string are defined in <a href="https://msdn.microsoft.com/c18868a9-6912-46fd-93f5-d8021937b049">Day, Month, Year, and Era Format Pictures</a>.

For example, to get the date string "Wed, Aug 31 94", the application uses the picture string "ddd',' MMM dd yy".

The function uses the specified locale only for information not specified in the format picture string, for example, the day and month names for the locale. The application can set this parameter to <b>NULL</b> to format the string according to the date format for the specified locale.


### -param lpDateStr [out, optional]

Pointer to a buffer in which this function retrieves the formatted date string.


### -param cchDate [in]

Size, in characters, of the <i>lpDateStr</i> buffer. The application can set this parameter to 0 to return the buffer size required to hold the formatted date string. In this case, the buffer indicated by <i>lpDateStr</i> is not used.


### -param lpCalendar [in, optional]

Reserved; must set to <b>NULL</b>.


## -returns



Returns the number of characters written to the <i>lpDateStr</i> buffer if successful. If the <i>cchDate</i> parameter is set to 0, the function returns the number of characters required to hold the formatted date string, including the terminating null character.

This function returns 0 if it does not succeed. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



The earliest date supported by this function is January 1, 1601.

The day name, abbreviated day name, month name, and abbreviated month name are all localized based on the locale identifier.

The date values in the structure indicated by <i>lpDate</i> must be valid. The function checks each of the date values: year, month, day, and day of week. If the day of the week is incorrect, the function uses the correct value, and returns no error. If any of the other date values are outside the correct range, the function fails, and sets the last error to ERROR_INVALID_PARAMETER.

The function ignores the time members of the <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure indicated by <i>lpDate</i>. These include <b>wHour</b>, <b>wMinute</b>, <b>wSecond</b>, and <b>wMilliseconds</b>.

If the <i>lpFormat</i> parameter contains a bad format string, the function returns no errors, but just forms the best possible date string. For example, the only year pictures that are valid are L"yyyy" and L"yy", where the "L" indicates a Unicode (16-bit characters) string. If L"y" is passed in, the function assumes L"yy". If L"yyy" is passed in, the function assumes L"yyyy". If more than four date (L"dddd") or four month (L"MMMM") pictures are passed in, the function defaults to L"dddd" or L"MMMM".

The application should enclose any text that should remain in its exact form in the date string within single quotation marks in the date format picture. The single quotation mark can also be used as an escape character to allow the single quotation mark itself to be displayed in the date string. However, the escape sequence must be enclosed within two single quotation marks. For example, to display the date as "May '93", the format string is: L"MMMM ''''yy". The first and last single quotation marks are the enclosing quotation marks. The second and third single quotation marks are the escape sequence to allow the single quotation mark to be displayed before the century.

When the date picture contains both a numeric form of the day (either d or dd) and the full month name (MMMM), the genitive form of the month name is retrieved in the date string.

To obtain the default short and long date format without performing any actual formatting, the application should use <a href="https://msdn.microsoft.com/20294ff2-b783-41a2-92a8-41cd974a2ccb">GetLocaleInfoEx</a> with the <a href="https://msdn.microsoft.com/55333a53-1205-42eb-aa1a-c248c52a8a3f">LOCALE_SSHORTDATE</a> or <a href="https://msdn.microsoft.com/1b72cd57-819e-4b1f-bbb0-b600a9e8631c">LOCALE_SLONGDATE</a> constant. To get the date format for an alternate calendar, the application uses <a href="https://msdn.microsoft.com/20294ff2-b783-41a2-92a8-41cd974a2ccb">GetLocaleInfoEx</a> with the <a href="https://msdn.microsoft.com/a944bdfc-6c07-4e78-b4d2-a26d66f18327">LOCALE_IOPTIONALCALENDAR</a> constant. To get the date format for a particular calendar, the application uses <a href="https://msdn.microsoft.com/b3c2fb74-0559-4752-9bdb-36b78084aed5">GetCalendarInfoEx</a>, passing the appropriate <a href="https://msdn.microsoft.com/ba2e841e-e24e-476a-851e-a29b3af4f04d">Calendar Identifier</a>. It can call <a href="https://msdn.microsoft.com/5a313af5-e595-49b1-9651-a5afc158c7a7">EnumCalendarInfoEx</a> or <a href="https://msdn.microsoft.com/523ef50f-722a-48b9-a2ce-20786b7c79e1">EnumDateFormatsEx</a> to retrieve date formats for a particular calendar.

This function can retrieve data from <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="https://msdn.microsoft.com/f62402d6-31de-4ff7-9538-7925a007a089">Using Persistent Locale Data</a>.

The DATE_LONGDATE format includes two kinds of date patterns: patterns that include the day of the week and patterns that do not include the day of the week. For example, "Tuesday, October 18, 2016" or "October 18, 2016".  If your application needs to ensure that dates use one of these kinds of patterns and not the other kind, your application should perform the following actions:<ol>
<li>Call the <a href="https://msdn.microsoft.com/52bfec03-4cb3-4418-b467-f75d2900ba40">EnumDateFormatsExEx</a> function to get all of the date formats for the DATE_LONGDATE format.</li>
<li>Look for the first date format passed to the callback function that you specified for  <a href="https://msdn.microsoft.com/52bfec03-4cb3-4418-b467-f75d2900ba40">EnumDateFormatsExEx</a> that matches your requested calendar identifier and has a date format string that matches the requirements of your application. For example, look for the first date format that includes "dddd" if your application requires that the date include the full name of the day of the week, or look for the first date format that includes neither "ddd" nor "dddd" if your application requires that the date includes nether the abbreviated name nor the full name of the day of the week.</li>
<li>Call the <b>GetDateFormatEx</b> function with the  <i>lpFormat</i> parameter set to the date format string that you identified as the appropriate format in the callback function.</li>
</ol>


If the presence or absence of the day of the week in the long date format does not matter to your application, your application can call <b>GetDateFormatEx</b> directly without first enumerating all of the long date formats by calling <a href="https://msdn.microsoft.com/52bfec03-4cb3-4418-b467-f75d2900ba40">EnumDateFormatsExEx</a>.

<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="https://msdn.microsoft.com/e9e566c3-e84a-44d3-980f-fe8bbd5e052a">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="https://msdn.microsoft.com/99264b22-3fb5-47e2-b0b9-42a6768e67c1">ResolveLocaleName</a>.

<b>Beginning in Windows 8: </b><b>GetDateFormatEx</b>  is declared in Datetimeapi.h. Before Windows 8, it was declared in Winnls.h.




## -see-also




<a href="https://msdn.microsoft.com/c18868a9-6912-46fd-93f5-d8021937b049">Day, Month, Year, and Era Format Pictures</a>



<a href="https://msdn.microsoft.com/52bfec03-4cb3-4418-b467-f75d2900ba40">EnumDateFormatsExEx</a>



<a href="https://msdn.microsoft.com/b3c2fb74-0559-4752-9bdb-36b78084aed5">GetCalendarInfoEx</a>



<a href="https://msdn.microsoft.com/546cede1-1702-403a-bba3-b5cd3b35a1bf">GetDateFormat</a>



<a href="https://msdn.microsoft.com/0502dba0-a26f-4238-b68e-bb41ef17ff08">NLS: Name-based APIs Sample</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

