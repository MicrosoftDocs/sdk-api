---
UID: NF:datetimeapi.GetTimeFormatA
title: GetTimeFormatA function (datetimeapi.h)
description: Formats time as a time string for a locale specified by identifier. The function formats either a specified time or the local system time. (ANSI)
helpviewer_keywords: ["GetTimeFormatA", "datetimeapi/GetTimeFormatA"]
old-location: intl\gettimeformat.htm
tech.root: Intl
ms.assetid: 3db91d29-df97-4660-b3cd-0db5b42cfd01
ms.date: 12/05/2018
ms.keywords: GetTimeFormat, GetTimeFormat function [Internationalization for Windows Applications], GetTimeFormatA, GetTimeFormatW, _win32_GetTimeFormat, datetimeapi/GetTimeFormat, datetimeapi/GetTimeFormatA, datetimeapi/GetTimeFormatW, intl.gettimeformat
req.header: datetimeapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetTimeFormatW (Unicode) and GetTimeFormatA (ANSI)
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
 - GetTimeFormatA
 - datetimeapi/GetTimeFormatA
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
 - GetTimeFormat
 - GetTimeFormatA
 - GetTimeFormatW
---

# GetTimeFormatA function


## -description

Formats time as a time string for a locale specified by identifier. The function formats either a specified time or the local system time.
<div class="alert"><b>Note</b>  For interoperability reasons, the application should prefer the <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex">GetTimeFormatEx</a> function to <b>GetTimeFormat</b> because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. Any application that will be run only on Windows Vista and later should use <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex">GetTimeFormatEx</a>.</div><div> </div>

## -parameters

### -param Locale [in]

<a href="/windows/desktop/Intl/locale-identifiers">Locale identifier</a> that specifies the locale. You can use the <a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

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

Flags specifying time format options. For detailed definitions see the <i>dwFlags</i> parameter of <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex">GetTimeFormatEx</a>.

### -param lpTime [in, optional]

Pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the time information to format. The application can set this parameter to <b>NULL</b> if the function is to use the current local system time.

### -param lpFormat [in, optional]

Pointer to a format picture to use to format the time string. If the application sets this parameter to <b>NULL</b>, the function formats the string according to the time format of the specified locale. If the application does not set the parameter to <b>NULL</b>, the function uses the locale only for information not specified in the format picture string, for example, the locale-specific time markers. For information about the format picture string, see the Remarks section.

### -param lpTimeStr [out, optional]

Pointer to a buffer in which this function retrieves the formatted time string.

### -param cchTime [in]

Size, in TCHAR values, for the time string buffer indicated by <i>lpTimeStr</i>. Alternatively, the application can set this parameter to 0. In this case, the function returns the required size for the time string buffer, and does not use the <i>lpTimeStr</i> parameter.

## -returns

Returns the number of TCHAR values retrieved in the buffer indicated by <i>lpTimeStr</i>. If the <i>cchTime</i> parameter is set to 0, the function returns the size of the buffer required to hold the formatted time string, including a terminating null character.

This function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
<li>ERROR_OUTOFMEMORY. Not enough storage was available to complete this operation.</li>
</ul>

## -remarks

See Remarks for <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex">GetTimeFormatEx</a>.

When the ANSI version of this function is used with a Unicode-only locale identifier, the function can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark (?). 
      

<b>Starting with Windows 8: </b><b>GetTimeFormat</b>  is declared in Datetimeapi.h. Before Windows 8, it was declared in Winnls.h.





> [!NOTE]
> The datetimeapi.h header defines GetTimeFormat as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata">GetDateFormat</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getlocaleinfoa">GetLocaleInfo</a>



<a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex">GetTimeFormatEx</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
