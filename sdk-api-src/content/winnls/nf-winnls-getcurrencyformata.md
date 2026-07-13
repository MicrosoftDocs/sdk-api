---
UID: NF:winnls.GetCurrencyFormatA
title: GetCurrencyFormatA function (winnls.h)
description: Formats a number string as a currency string for a locale specified by identifier. (ANSI)
helpviewer_keywords: ["GetCurrencyFormatA", "winnls/GetCurrencyFormatA"]
old-location: intl\getcurrencyformat.htm
tech.root: Intl
ms.assetid: 43c51deb-ca92-4e14-8c27-3b588b7be061
ms.date: 12/05/2018
ms.keywords: GetCurrencyFormat, GetCurrencyFormat function [Internationalization for Windows Applications], GetCurrencyFormatA, GetCurrencyFormatW, _win32_GetCurrencyFormat, intl.getcurrencyformat, winnls/GetCurrencyFormat, winnls/GetCurrencyFormatA, winnls/GetCurrencyFormatW
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetCurrencyFormatW (Unicode) and GetCurrencyFormatA (ANSI)
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
 - GetCurrencyFormatA
 - winnls/GetCurrencyFormatA
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
 - GetCurrencyFormat
 - GetCurrencyFormatA
 - GetCurrencyFormatW
---

# GetCurrencyFormatA function


## -description

Formats a number string as a currency string for a locale specified by identifier.
<div class="alert"><b>Note</b>  For interoperability reasons, the application should prefer the <a href="/windows/desktop/api/winnls/nf-winnls-getcurrencyformatex">GetCurrencyFormatEx</a> function to <b>GetCurrencyFormat</b> because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. Any application that runs only on Windows Vista and later should use <a href="/windows/desktop/api/winnls/nf-winnls-getcurrencyformatex">GetCurrencyFormatEx</a>.</div><div> </div>

## -parameters

### -param Locale [in]

<a href="/windows/desktop/Intl/locale-identifiers">Locale identifier</a> that specifies the locale for which this function formats the currency string. You can use the <a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

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

Flags controlling currency format. The application must set this parameter to 0 if <i>lpFormat</i> is not set to <b>NULL</b>. In this case, the function formats the string using user overrides to the default currency format for the locale. If <i>lpFormat</i> is set to <b>NULL</b>, the application can specify <a href="/windows/desktop/Intl/locale-nouseroverride">LOCALE_NOUSEROVERRIDE</a> to format the string using the system default currency format for the specified locale.

<div class="alert"><b>Caution</b>  Use of <a href="/windows/desktop/Intl/locale-nouseroverride">LOCALE_NOUSEROVERRIDE</a> is strongly discouraged as it disables user preferences.</div>
<div> </div>

### -param lpValue [in]

For details, see the <i>lpValue</i> parameter of <a href="/windows/desktop/api/winnls/nf-winnls-getcurrencyformatex">GetCurrencyFormatEx</a>.

### -param lpFormat [in, optional]

Pointer to a <a href="/windows/desktop/api/winnls/ns-winnls-currencyfmta">CURRENCYFMT</a> structure that contains currency formatting information. All members of the structure must contain appropriate values. The application can set this parameter to <b>NULL</b> if function is to use the currency format of the specified locale. If this parameter is not set to <b>NULL</b>, the function uses the specified locale only for formatting information not specified in the <a href="/windows/desktop/api/winnls/ns-winnls-currencyfmta">CURRENCYFMT</a> structure, for example, the string value for the negative sign used by the locale.

### -param lpCurrencyStr [out, optional]

Pointer to a buffer in which this function retrieves the formatted currency string.

### -param cchCurrency [in]

Size, in characters, of the <i>lpCurrencyStr</i> buffer. The application sets this parameter to 0 if the function is to return the size of the buffer required to hold the formatted currency string. In this case, the <i>lpCurrencyStr</i> parameter is not used.

## -returns

Returns the number of characters retrieved in the buffer indicated by <i>lpCurrencyStr</i> if successful. If the <i>cchCurrency</i> parameter is set to 0, the function returns the size of the buffer required to hold the formatted currency string, including a terminating null character.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

This function can retrieve data from <a href="/windows/desktop/Intl/custom-locales">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.

When the ANSI version of this function is used with a Unicode-only locale identifier, the call can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark (?). 
      





> [!NOTE]
> The winnls.h header defines GetCurrencyFormat as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnls/ns-winnls-currencyfmta">CURRENCYFMT</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getcurrencyformatex">GetCurrencyFormatEx</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getnumberformata">GetNumberFormat</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
