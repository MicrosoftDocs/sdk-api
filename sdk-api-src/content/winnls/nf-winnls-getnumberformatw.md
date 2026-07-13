---
UID: NF:winnls.GetNumberFormatW
title: GetNumberFormatW function (winnls.h)
description: Formats a number string as a number string customized for a locale specified by identifier. (Unicode)
helpviewer_keywords: ["GetNumberFormat", "GetNumberFormat function [Internationalization for Windows Applications]", "GetNumberFormatW", "_win32_GetNumberFormat", "intl.getnumberformat", "winnls/GetNumberFormat", "winnls/GetNumberFormatW"]
old-location: intl\getnumberformat.htm
tech.root: Intl
ms.assetid: acbfebed-71bd-4266-b639-66f453158442
ms.date: 10/06/2025
ms.keywords: GetNumberFormat, GetNumberFormat function [Internationalization for Windows Applications], GetNumberFormatA, GetNumberFormatW, _win32_GetNumberFormat, intl.getnumberformat, winnls/GetNumberFormat, winnls/GetNumberFormatA, winnls/GetNumberFormatW
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetNumberFormatW (Unicode) and GetNumberFormatA (ANSI)
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
 - GetNumberFormatW
 - winnls/GetNumberFormatW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Localization-Obsolete-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-Obsolete-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-Obsolete-L1-3-0.dll
 - API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - GetNumberFormat
 - GetNumberFormatA
 - GetNumberFormatW
---

# GetNumberFormatW function


## -description

Formats a number string as a number string customized for a locale specified by identifier.
<div class="alert"><b>Note</b>  For interoperability reasons, the application should prefer the <a href="/windows/desktop/api/winnls/nf-winnls-getnumberformatex">GetNumberFormatEx</a> function to <b>GetNumberFormat</b> because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. Any application that runs only on Windows Vista and later should use <b>GetNumberFormatEx</b>.</div><div> </div>

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

Flags controlling the operation of the function. The application must set this parameter to 0 if <i>lpFormat</i> is not set to <b>NULL</b>. In this case, the function formats the string using user overrides to the default number format for the locale. If <i>lpFormat</i> is set to <b>NULL</b>, the application can specify <a href="/windows/desktop/Intl/locale-nouseroverride">LOCALE_NOUSEROVERRIDE</a> to format the string using the system default number format for the specified locale.

<div class="alert"><b>Caution</b>  Use of LOCALE_NOUSEROVERRIDE is strongly discouraged as it disables user preferences.</div>
<div> </div>

### -param lpValue [in]

Pointer to a null-terminated string containing the number string to format. This string can only contain the following characters. All other characters are invalid. The function returns an error if the string indicated by <i>lpValue</i> deviates from these rules.

<ul>
<li>Characters "0" through "9".</li>
<li>One decimal point (dot) if the number is a floating-point value.</li>
<li>A minus sign in the first character position if the number is a negative value.</li>
</ul>

### -param lpFormat [in, optional]

Pointer to a <a href="/windows/desktop/api/winnls/ns-winnls-numberfmta">NUMBERFMT</a> structure that contains number formatting information, with all members set to appropriate values. If the application does not set this parameter to <b>NULL</b>, the function uses the locale formatting information.

### -param lpNumberStr [out, optional]

Pointer to a buffer in which this function retrieves the formatted number string.

### -param cchNumber [in]

Size, in TCHAR values, for the number string buffer indicated by <i>lpNumberStr</i>. Alternatively, the application can set this parameter to 0. In this case, the function returns the required size for the number string buffer, and does not use the <i>lpNumberStr</i> parameter.

## -returns

Returns the number of TCHAR values retrieved in the buffer indicated by <i>lpNumberStr</i> if successful. If the <i>cchNumber</i> parameter is set to 0, the function returns the number of characters required to hold the formatted number string, including a terminating null character.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
<li>ERROR_OUTOFMEMORY. Not enough storage was available to complete this operation.</li>
</ul>

## -remarks

This function can retrieve data from <a href="/windows/desktop/Intl/custom-locales">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.

When the ANSI version of this function is used with a Unicode-only locale identifier, the function can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark (?). 
      





> [!NOTE]
> The winnls.h header defines GetNumberFormat as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getnumberformatex">GetNumberFormatEx</a>



<a href="/windows/desktop/api/winnls/ns-winnls-numberfmta">NUMBERFMT</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
