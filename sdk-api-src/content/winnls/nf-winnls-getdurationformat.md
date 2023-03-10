---
UID: NF:winnls.GetDurationFormat
title: GetDurationFormat function (winnls.h)
description: Formats a duration of time as a time string for a locale specified by identifier.
helpviewer_keywords: ["GetDurationFormat","GetDurationFormat function [Internationalization for Windows Applications]","_win32_GetDurationFormat","intl.getdurationformat","winnls/GetDurationFormat"]
old-location: intl\getdurationformat.htm
tech.root: Intl
ms.assetid: bd3e1256-8f0c-488b-9b2f-ca93ffcbad84
ms.date: 12/05/2018
ms.keywords: GetDurationFormat, GetDurationFormat function [Internationalization for Windows Applications], _win32_GetDurationFormat, intl.getdurationformat, winnls/GetDurationFormat
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - GetDurationFormat
 - winnls/GetDurationFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - GetDurationFormat
---

# GetDurationFormat function


## -description

Formats a duration of time as a time string for a locale specified by identifier.
<div class="alert"><b>Note</b>  For interoperability reasons, the application should prefer the <a href="/windows/desktop/api/winnls/nf-winnls-getdurationformatex">GetDurationFormatEx</a> function to <b>GetDurationFormat</b> because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. Any application that runs only on Windows Vista and later should use <a href="/windows/desktop/api/winnls/nf-winnls-getdurationformatex">GetDurationFormatEx</a>.</div><div> </div>

## -parameters

### -param Locale [in]

<a href="/windows/desktop/Intl/locale-identifiers">Locale identifier</a> that specifies the locale for which this function formats the duration. You can use the <a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

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

### -param dwFlags [in]

Flags specifying function options. If <i>lpFormat</i> is not set to <b>NULL</b>, this parameter must be set to 0. If <i>lpFormat</i> is set to <b>NULL</b>, your application can specify <a href="/windows/desktop/Intl/locale-nouseroverride">LOCALE_NOUSEROVERRIDE</a> to format the string using the system default duration format for the specified locale.

<div class="alert"><b>Caution</b>  Use of LOCALE_NOUSEROVERRIDE is strongly discouraged as it disables user preferences.</div>
<div> </div>

### -param lpDuration [in, optional]

Pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the time duration information to format. If this pointer is <b>NULL</b>, the function ignores this parameter and uses <i>ullDuration</i>.

### -param ullDuration [in]

64-bit unsigned integer that represents the number of 100-nanosecond intervals in the duration. If both <i>lpDuration</i> and <i>ullDuration</i> are present, <i>lpDuration</i> takes precedence. If <i>lpDuration</i> is set to <b>NULL</b> and <i>ullDuration</i> is set to 0, the duration is zero.

### -param lpFormat [in, optional]

Pointer to the format string. For details, see the <i>lpFormat</i> parameter of <a href="/windows/desktop/api/winnls/nf-winnls-getdurationformatex">GetDurationFormatEx</a>.

### -param lpDurationStr [out, optional]

Pointer to the buffer in which the function retrieves the duration string.

Alternatively, this parameter can contain <b>NULL</b> if <i>cchDuration</i> is set to 0. In this case, the function returns the required size for the duration string buffer.

### -param cchDuration [in]

Size, in characters, of the buffer indicated by <i>lpDurationStr</i>.

Alternatively, the application can set this parameter to 0. In this case, the function retrieves <b>NULL</b> in <i>lpDurationStr</i> and returns the required size for the duration string buffer.

## -returns

Returns the number of characters retrieved in the buffer indicated by <i>lpDurationStr</i> if successful. If <i>lpDurationStr</i> is set to <b>NULL</b> and <i>cchDuration</i> is set to 0, the function returns the required size for the duration string buffer, including the null terminating character. For example, if 10 characters are written to the buffer, the function returns 11 to include the terminating null character.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

See Remarks for <a href="/windows/desktop/api/winnls/nf-winnls-getdurationformatex">GetDurationFormatEx</a>.

## -see-also

<a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata">GetDateFormat</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getdurationformatex">GetDurationFormatEx</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoa">GetLocaleInfo</a>



<a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata">GetTimeFormat</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>