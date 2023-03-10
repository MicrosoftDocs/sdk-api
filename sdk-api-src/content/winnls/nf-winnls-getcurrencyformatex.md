---
UID: NF:winnls.GetCurrencyFormatEx
title: GetCurrencyFormatEx function (winnls.h)
description: Formats a number string as a currency string for a locale specified by name.Note  The application should call this function in preference to GetCurrencyFormat if designed to run only on Windows Vista and later. Note  This function can format data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see Using Persistent Locale Data.
helpviewer_keywords: ["GetCurrencyFormatEx","GetCurrencyFormatEx function [Internationalization for Windows Applications]","_win32_GetCurrencyFormatEx","intl.getcurrencyformatex","winnls/GetCurrencyFormatEx"]
old-location: intl\getcurrencyformatex.htm
tech.root: Intl
ms.assetid: 72639b31-cd5d-455c-873a-e3cf4051f4cd
ms.date: 12/05/2018
ms.keywords: GetCurrencyFormatEx, GetCurrencyFormatEx function [Internationalization for Windows Applications], _win32_GetCurrencyFormatEx, intl.getcurrencyformatex, winnls/GetCurrencyFormatEx
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
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
 - GetCurrencyFormatEx
 - winnls/GetCurrencyFormatEx
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
api_name:
 - GetCurrencyFormatEx
---

# GetCurrencyFormatEx function


## -description

Formats a number string as a currency string for a locale specified by name.<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="/windows/desktop/api/winnls/nf-winnls-getcurrencyformata">GetCurrencyFormat</a> if designed to run only on Windows Vista and later.</div>
<div> </div>
<div class="alert"><b>Note</b>  This function can format data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see <a href="/windows/desktop/Intl/using-persistent-locale-data">Using Persistent Locale Data</a>.</div>
<div> </div>

## -parameters

### -param lpLocaleName [in, optional]

Pointer to a <a href="/windows/desktop/Intl/locale-names">locale name</a> or one of the following predefined values. 

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

Flags controlling the operation of the function. The application must set this parameter to 0 if <i>lpFormat</i> is not set to <b>NULL</b>. In this case, the function formats the string using user overrides to the default currency format for the locale. If <i>lpFormat</i> is set to <b>NULL</b>, the application can specify <a href="/windows/desktop/Intl/locale-nouseroverride">LOCALE_NOUSEROVERRIDE</a> to format the string using the system default currency format for the specified locale.

<div class="alert"><b>Caution</b>  Use of <a href="/windows/desktop/Intl/locale-nouseroverride">LOCALE_NOUSEROVERRIDE</a> is strongly discouraged as it disables user preferences.</div>
<div> </div>

### -param lpValue [in]

Pointer to a null-terminated string containing the number string to format. This string can contain only the following characters. All other characters are invalid. The function returns an error if the string deviates from these rules.

<ul>
<li>Characters "0" through "9"</li>
<li>One decimal point (dot) if the number is a floating-point value</li>
<li>A minus sign in the first character position if the number is a negative value</li>
</ul>

### -param lpFormat [in, optional]

Pointer to a <a href="/windows/desktop/api/winnls/ns-winnls-currencyfmta">CURRENCYFMT</a> structure that contains currency formatting information. All members of the structure must contain appropriate values. The application can set this parameter to <b>NULL</b> if function is to use the currency format of the specified locale. If this parameter is not set to <b>NULL</b>, the function uses the specified locale only for formatting information not specified in the <b>CURRENCYFMT</b> structure, for example, the string value for the negative sign used by the locale.

### -param lpCurrencyStr [out, optional]

Pointer to a buffer in which this function retrieves the formatted currency string.

### -param cchCurrency [in]

Size, in characters, of the <i>lpCurrencyStr</i> buffer. The application can set this parameter to 0 to return the size of the buffer required to hold the formatted currency string. In this case, the buffer indicated by <i>lpCurrencyStr</i> is not used.

## -returns

Returns the number of characters retrieved in the buffer indicated by <i>lpCurrencyStr</i> if successful. If the <i>cchCurrency</i> parameter is 0, the function returns the size of the buffer required to hold the formatted currency string, including a terminating null character.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>

## -remarks

<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="/uwp/api/Windows.Globalization">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="/windows/desktop/api/winnls/nf-winnls-resolvelocalename">ResolveLocaleName</a>.

## -see-also

<a href="/windows/desktop/api/winnls/ns-winnls-currencyfmta">CURRENCYFMT</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getcurrencyformata">GetCurrencyFormat</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getnumberformatex">GetNumberFormatEx</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>