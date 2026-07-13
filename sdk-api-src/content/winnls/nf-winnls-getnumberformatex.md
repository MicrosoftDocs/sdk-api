---
UID: NF:winnls.GetNumberFormatEx
title: GetNumberFormatEx function (winnls.h)
description: Formats a number string as a number string customized for a locale specified by name.Note  The application should call this function in preference to GetNumberFormat if designed to run only on Windows Vista and later. Note  This function can format data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see Using Persistent Locale Data.
helpviewer_keywords: ["GetNumberFormatEx","GetNumberFormatEx function [Internationalization for Windows Applications]","_win32_GetNumberFormatEx","intl.getnumberformatex","winnls/GetNumberFormatEx"]
old-location: intl\getnumberformatex.htm
tech.root: Intl
ms.assetid: 7874bc6e-1db2-44be-aa7a-7c716d23f7a4
ms.date: 10/06/2025
ms.keywords: GetNumberFormatEx, GetNumberFormatEx function [Internationalization for Windows Applications], _win32_GetNumberFormatEx, intl.getnumberformatex, winnls/GetNumberFormatEx
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
 - GetNumberFormatEx
 - winnls/GetNumberFormatEx
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
 - GetNumberFormatEx
---

# GetNumberFormatEx function


## -description

Formats a number string as a number string customized for a locale specified by name.<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="/windows/desktop/api/winnls/nf-winnls-getnumberformata">GetNumberFormat</a> if designed to run only on Windows Vista and later.</div>
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

Pointer to a buffer in which this function retrieves the formatted number string. Alternatively, this parameter contains <b>NULL</b> if <i>cchNumber</i> is set to 0. In this case, the function returns the required size for the number string buffer.

### -param cchNumber [in]

Size, in characters, for the number string buffer indicated by <i>lpNumberStr</i>. Alternatively, the application can set this parameter to 0. In this case, the function returns the required size for the number string buffer and does not use the <i>lpNumberStr</i> parameter.

## -returns

Returns the number of characters retrieved in the buffer indicated by <i>lpNumberStr</i> if successful. If the <i>cchNumber</i> parameter is set to 0, the function returns the number of characters required to hold the formatted number string, including a terminating null character.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
<li>ERROR_OUTOFMEMORY. Not enough storage was available to complete this operation.</li>
</ul>

## -remarks

<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="/uwp/api/Windows.Globalization">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="/windows/desktop/api/winnls/nf-winnls-resolvelocalename">ResolveLocaleName</a>.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getnumberformata">GetNumberFormat</a>



<a href="/windows/desktop/api/winnls/ns-winnls-numberfmta">NUMBERFMT</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>
