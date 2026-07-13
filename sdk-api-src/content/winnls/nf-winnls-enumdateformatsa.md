---
UID: NF:winnls.EnumDateFormatsA
title: EnumDateFormatsA function (winnls.h)
description: Enumerates the long date, short date, or year/month formats that are available for a specified locale. (ANSI)
helpviewer_keywords: ["EnumDateFormatsA", "winnls/EnumDateFormatsA"]
old-location: intl\enumdateformats.htm
tech.root: Intl
ms.assetid: 77b5e753-aee9-42d8-a0fa-27b065fc3b20
ms.date: 12/05/2018
ms.keywords: EnumDateFormats, EnumDateFormats function [Internationalization for Windows Applications], EnumDateFormatsA, EnumDateFormatsW, _win32_EnumDateFormats, intl.enumdateformats, winnls/EnumDateFormats, winnls/EnumDateFormatsA, winnls/EnumDateFormatsW
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumDateFormatsW (Unicode) and EnumDateFormatsA (ANSI)
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
 - EnumDateFormatsA
 - winnls/EnumDateFormatsA
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
 - EnumDateFormats
 - EnumDateFormatsA
 - EnumDateFormatsW
---

# EnumDateFormatsA function


## -description

Enumerates the long date, short date, or year/month formats that are available for a specified locale.
<div class="alert"><b>Note</b>  To receive a calendar identifier in addition to date format information, the application should use the <a href="/windows/desktop/api/winnls/nf-winnls-enumdateformatsexa">EnumDateFormatsEx</a> function. Another reason for preferring this function is that Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales, for interoperability reasons.</div><div> </div><div class="alert"><b>Note</b>  Any application that will be run only on Windows Vista or later should use <a href="/windows/desktop/api/winnls/nf-winnls-enumdateformatsexex">EnumDateFormatsExEx</a> in preference to <b>EnumDateFormats</b>.</div><div> </div>

## -parameters

### -param lpDateFmtEnumProc [in]

Pointer to an application-defined callback function. For more information, see <a href="/previous-versions/windows/desktop/legacy/dd317813(v=vs.85)">EnumDateFormatsProc</a>.

### -param Locale [in]

<a href="/windows/desktop/Intl/locale-identifiers">Locale identifier</a> that specifies the locale for which to retrieve date format information. You can use the <a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro to create an identifier or use one of the following predefined values. 

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
For details of operation of this function, see Remarks in <a href="/windows/desktop/api/winnls/nf-winnls-enumdateformatsexa">EnumDateFormatsEx</a>.

<div class="alert"><b>Note</b>  To enumerate the date formats for locales with alternate calendars, the application should use <a href="/windows/desktop/api/winnls/nf-winnls-enumdateformatsexa">EnumDateFormatsEx</a>.</div>
<div> </div>




> [!NOTE]
> The winnls.h header defines EnumDateFormats as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-enumdateformatsexa">EnumDateFormatsEx</a>



<a href="/windows/desktop/api/winnls/nf-winnls-enumdateformatsexex">EnumDateFormatsExEx</a>



<a href="/previous-versions/windows/desktop/legacy/dd317813(v=vs.85)">EnumDateFormatsProc</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
