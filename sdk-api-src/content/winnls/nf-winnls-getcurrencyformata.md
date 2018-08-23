---
UID: NF:winnls.GetCurrencyFormatA
title: GetCurrencyFormatA function
author: windows-sdk-content
description: Formats a number string as a currency string for a locale specified by identifier.
old-location: intl\getcurrencyformat.htm
old-project: Intl
ms.assetid: 43c51deb-ca92-4e14-8c27-3b588b7be061
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: GetCurrencyFormat, GetCurrencyFormat function [Internationalization for Windows Applications], GetCurrencyFormatA, GetCurrencyFormatW, _win32_GetCurrencyFormat, intl.getcurrencyformat, winnls/GetCurrencyFormat, winnls/GetCurrencyFormatA, winnls/GetCurrencyFormatW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: NORM_FORM
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
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetCurrencyFormatA function


## -description


Formats a number string as a currency string for a locale specified by identifier.
<div class="alert"><b>Note</b>  For interoperability reasons, the application should prefer the <a href="https://msdn.microsoft.com/72639b31-cd5d-455c-873a-e3cf4051f4cd">GetCurrencyFormatEx</a> function to <b>GetCurrencyFormat</b> because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. Any application that runs only on Windows Vista and later should use <a href="https://msdn.microsoft.com/72639b31-cd5d-455c-873a-e3cf4051f4cd">GetCurrencyFormatEx</a>.</div><div> </div>

## -parameters




### -param Locale [in]


<a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">Locale identifier</a> that specifies the locale for which this function formats the currency string. You can use the <a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

<ul>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UI_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a41a7f55-8905-47a1-86c3-74ed40b3834c">LOCALE_CUSTOM_UNSPECIFIED</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d37df17d-8cd5-4481-bee2-062cf9d78e9b">LOCALE_INVARIANT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/57de328c-3afc-4fbb-882c-fa35d3552c13">LOCALE_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9ccb489b-24d0-42e5-a01a-2cdb7c3267eb">LOCALE_USER_DEFAULT</a>
</li>
</ul>

### -param dwFlags [in]

Flags controlling currency format. The application must set this parameter to 0 if <i>lpFormat</i> is not set to <b>NULL</b>. In this case, the function formats the string using user overrides to the default currency format for the locale. If <i>lpFormat</i> is set to <b>NULL</b>, the application can specify <a href="https://msdn.microsoft.com/ab68d16b-5e1e-4af3-b048-43975cded00a">LOCALE_NOUSEROVERRIDE</a> to format the string using the system default currency format for the specified locale.

<div class="alert"><b>Caution</b>  Use of <a href="https://msdn.microsoft.com/ab68d16b-5e1e-4af3-b048-43975cded00a">LOCALE_NOUSEROVERRIDE</a> is strongly discouraged as it disables user preferences.</div>
<div> </div>

### -param lpValue [in]

For details, see the <i>lpValue</i> parameter of <a href="https://msdn.microsoft.com/72639b31-cd5d-455c-873a-e3cf4051f4cd">GetCurrencyFormatEx</a>.


### -param lpFormat [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/026ac9e0-1f5b-4a42-9c7b-07a127422994">CURRENCYFMT</a> structure that contains currency formatting information. All members of the structure must contain appropriate values. The application can set this parameter to <b>NULL</b> if function is to use the currency format of the specified locale. If this parameter is not set to <b>NULL</b>, the function uses the specified locale only for formatting information not specified in the <a href="https://msdn.microsoft.com/026ac9e0-1f5b-4a42-9c7b-07a127422994">CURRENCYFMT</a> structure, for example, the string value for the negative sign used by the locale.


### -param lpCurrencyStr [out, optional]

Pointer to a buffer in which this function retrieves the formatted currency string.


### -param cchCurrency [in]

Size, in characters, of the <i>lpCurrencyStr</i> buffer. The application sets this parameter to 0 if the function is to return the size of the buffer required to hold the formatted currency string. In this case, the <i>lpCurrencyStr</i> parameter is not used.


## -returns



Returns the number of characters retrieved in the buffer indicated by <i>lpCurrencyStr</i> if successful. If the <i>cchCurrency</i> parameter is set to 0, the function returns the size of the buffer required to hold the formatted currency string, including a terminating null character.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



This function can retrieve data from <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="https://msdn.microsoft.com/f62402d6-31de-4ff7-9538-7925a007a089">Using Persistent Locale Data</a>.

When the ANSI version of this function is used with a Unicode-only locale identifier, the call can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark (?). 
      




## -see-also




<a href="https://msdn.microsoft.com/026ac9e0-1f5b-4a42-9c7b-07a127422994">CURRENCYFMT</a>



<a href="https://msdn.microsoft.com/72639b31-cd5d-455c-873a-e3cf4051f4cd">GetCurrencyFormatEx</a>



<a href="https://msdn.microsoft.com/acbfebed-71bd-4266-b639-66f453158442">GetNumberFormat</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

