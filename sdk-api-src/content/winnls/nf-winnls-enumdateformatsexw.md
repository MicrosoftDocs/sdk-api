---
UID: NF:winnls.EnumDateFormatsExW
title: EnumDateFormatsExW function (winnls.h)
description: Enumerates the long date, short date, or year/month formats that are available for a specified locale.Note  Any application that runs only on Windows Vista and later should use EnumDateFormatsExEx in preference to this function. (Unicode)
helpviewer_keywords: ["EnumDateFormatsEx", "EnumDateFormatsEx function [Internationalization for Windows Applications]", "EnumDateFormatsExW", "_win32_EnumDateFormatsEx", "intl.enumdateformatsex", "winnls/EnumDateFormatsEx", "winnls/EnumDateFormatsExW"]
old-location: intl\enumdateformatsex.htm
tech.root: Intl
ms.assetid: 523ef50f-722a-48b9-a2ce-20786b7c79e1
ms.date: 12/05/2018
ms.keywords: EnumDateFormatsEx, EnumDateFormatsEx function [Internationalization for Windows Applications], EnumDateFormatsExA, EnumDateFormatsExW, _win32_EnumDateFormatsEx, intl.enumdateformatsex, winnls/EnumDateFormatsEx, winnls/EnumDateFormatsExA, winnls/EnumDateFormatsExW
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumDateFormatsExW (Unicode) and EnumDateFormatsExA (ANSI)
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
 - EnumDateFormatsExW
 - winnls/EnumDateFormatsExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Localization-l2-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - EnumDateFormatsEx
 - EnumDateFormatsExA
 - EnumDateFormatsExW
---

# EnumDateFormatsExW function


## -description

Enumerates the long date, short date, or year/month formats that are available for a specified locale.
<div class="alert"><b>Note</b>  Any application that runs only on Windows Vista and later should use <a href="/windows/desktop/api/winnls/nf-winnls-enumdateformatsexex">EnumDateFormatsExEx</a> in preference to this function.</div><div> </div>

## -parameters

### -param lpDateFmtEnumProcEx [in]

Pointer to an application-defined callback function. For more information, see <a href="/previous-versions/windows/desktop/legacy/dd317814(v=vs.85)">EnumDateFormatsProcEx</a>.

### -param Locale [in]

<a href="/windows/desktop/Intl/locale-identifiers">Locale identifier</a> that specifies the locale for which to retrieve date format information. You can use the <a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro to create an identifier or use one of the following predefined values. 

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

Flag specifying date formats. For detailed definitions, see the <i>dwFlags</i> parameter of <a href="/windows/desktop/api/winnls/nf-winnls-enumdateformatsexex">EnumDateFormatsExEx</a>.

## -returns

Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

<div class="alert"><b>Note</b>  This API is being updated to support the May 2019 Japanese era change. If your application supports the Japanese calendar, you should validate that it properly handles the new era. See <a href="/windows/uwp/design/globalizing/japanese-era-change">Prepare your application for the Japanese era change</a> for more information.</div>
<div> </div>
The function enumerates the date formats by passing date format string pointers, one at a time, to the specified application-defined callback function. This process continues until <b>EnumDateFormatsEx</b> finds the last date format or the callback function returns <b>FALSE</b>.

This function enumerates all date formats for the specified locale, including alternate calendars, if any. However, the calendar identifier is not enumerated along with the date format, making formats for locales with alternate calendars difficult to use.

This function can enumerate data from <a href="/windows/desktop/Intl/custom-locales">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.

When the ANSI version of this function is used with a Unicode-only locale identifier, the function can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark (?).

The application should use <b>EnumDateFormatsEx</b> (instead of <a href="/windows/desktop/api/winnls/nf-winnls-enumdateformatsa">EnumDateFormats</a>) to enumerate date formats for locales with alternate calendars.





> [!NOTE]
> The winnls.h header defines EnumDateFormatsEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-enumdateformatsa">EnumDateFormats</a>



<a href="/windows/desktop/api/winnls/nf-winnls-enumdateformatsexex">EnumDateFormatsExEx</a>



<a href="/previous-versions/windows/desktop/legacy/dd317814(v=vs.85)">EnumDateFormatsProcEx</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
