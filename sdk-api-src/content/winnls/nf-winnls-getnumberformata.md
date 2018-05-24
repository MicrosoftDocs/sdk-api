---
UID: NF:winnls.GetNumberFormatA
title: GetNumberFormatA function
author: windows-driver-content
description: Formats a number string as a number string customized for a locale specified by identifier.
old-location: intl\getnumberformat.htm
old-project: Intl
ms.assetid: acbfebed-71bd-4266-b639-66f453158442
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: GetNumberFormat, GetNumberFormat function [Internationalization for Windows Applications], GetNumberFormatA, GetNumberFormatW, _win32_GetNumberFormat, intl.getnumberformat, winnls/GetNumberFormat, winnls/GetNumberFormatA, winnls/GetNumberFormatW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: NORM_FORM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-Localization-Obsolete-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-Localization-Obsolete-l1-2-0.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
-	API-MS-Win-Core-Localization-Obsolete-L1-3-0.dll
-	API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
-	Kernel32Legacy.dll
api_name:
-	GetNumberFormat
-	GetNumberFormatA
-	GetNumberFormatW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetNumberFormatA function


## -description


Formats a number string as a number string customized for a locale specified by identifier.
<div class="alert"><b>Note</b>  For interoperability reasons, the application should prefer the <a href="https://msdn.microsoft.com/7874bc6e-1db2-44be-aa7a-7c716d23f7a4">GetNumberFormatEx</a> function to <b>GetNumberFormat</b> because Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales. Any application that runs only on Windows Vista and later should use <b>GetNumberFormatEx</b>.</div><div> </div>

## -parameters




### -param Locale [in]


<a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">Locale identifier</a> that specifies the locale. You can use the <a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

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

Flags controlling the operation of the function. The application must set this parameter to 0 if <i>lpFormat</i> is not set to <b>NULL</b>. In this case, the function formats the string using user overrides to the default number format for the locale. If <i>lpFormat</i> is set to <b>NULL</b>, the application can specify <a href="https://msdn.microsoft.com/ab68d16b-5e1e-4af3-b048-43975cded00a">LOCALE_NOUSEROVERRIDE</a> to format the string using the system default number format for the specified locale.

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

Pointer to a <a href="https://msdn.microsoft.com/cb8a7714-3777-41b4-894b-bb0c0797d51e">NUMBERFMT</a> structure that contains number formatting information, with all members set to appropriate values. If this parameter does is not set to <b>NULL</b>, the function uses the locale only for formatting information not specified in the structure, for example, the locale-specific string value for the negative sign.


### -param lpNumberStr [out, optional]

Pointer to a buffer in which this function retrieves the formatted number string.


### -param cchNumber [in]

Size, in TCHAR values, for the number string buffer indicated by <i>lpNumberStr</i>. Alternatively, the application can set this parameter to 0. In this case, the function returns the required size for the number string buffer, and does not use the <i>lpNumberStr</i> parameter.


## -returns



Returns the number of TCHAR values retrieved in the buffer indicated by <i>lpNumberStr</i> if successful. If the <i>cchNumber</i> parameter is set to 0, the function returns the number of characters required to hold the formatted number string, including a terminating null character.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
<li>ERROR_OUTOFMEMORY. Not enough storage was available to complete this operation.</li>
</ul>



## -remarks



This function can retrieve data from <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="https://msdn.microsoft.com/f62402d6-31de-4ff7-9538-7925a007a089">Using Persistent Locale Data</a>.

When the ANSI version of this function is used with a Unicode-only locale identifier, the function can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark (?). 
      




## -see-also




<a href="https://msdn.microsoft.com/7874bc6e-1db2-44be-aa7a-7c716d23f7a4">GetNumberFormatEx</a>



<a href="https://msdn.microsoft.com/cb8a7714-3777-41b4-894b-bb0c0797d51e">NUMBERFMT</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

