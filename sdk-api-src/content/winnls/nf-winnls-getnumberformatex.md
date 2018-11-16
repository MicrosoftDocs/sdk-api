---
UID: NF:winnls.GetNumberFormatEx
title: GetNumberFormatEx function
author: windows-sdk-content
description: Formats a number string as a number string customized for a locale specified by name.Note  The application should call this function in preference to GetNumberFormat if designed to run only on Windows Vista and later. Note  This function can format data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see Using Persistent Locale Data.
old-location: intl\getnumberformatex.htm
tech.root: Intl
ms.assetid: 7874bc6e-1db2-44be-aa7a-7c716d23f7a4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetNumberFormatEx, GetNumberFormatEx function [Internationalization for Windows Applications], _win32_GetNumberFormatEx, intl.getnumberformatex, winnls/GetNumberFormatEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetNumberFormatEx
: 
---

# GetNumberFormatEx function


## -description


Formats a number string as a number string customized for a locale specified by name.<div class="alert"><b>Note</b>  The application should call this function in preference to <a href="https://msdn.microsoft.com/acbfebed-71bd-4266-b639-66f453158442">GetNumberFormat</a> if designed to run only on Windows Vista and later.</div>
<div> </div>
<div class="alert"><b>Note</b>  This function can format data that changes between releases, for example, due to a custom locale. If your application must persist or transmit data, see <a href="https://msdn.microsoft.com/f62402d6-31de-4ff7-9538-7925a007a089">Using Persistent Locale Data</a>.</div>
<div> </div>



## -parameters




### -param lpLocaleName [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/221aae7b-3a7c-4995-ae78-50d97de436d8">locale name</a>, or one of the following predefined values. 

<ul>
<li>
<a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_INVARIANT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_USER_DEFAULT</a>
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

Pointer to a <a href="https://msdn.microsoft.com/cb8a7714-3777-41b4-894b-bb0c0797d51e">NUMBERFMT</a> structure that contains number formatting information, with all members set to appropriate values. If the application does not set this parameter to <b>NULL</b>, the function uses the locale only for formatting information not specified in the structure, for example, the locale string value for the negative sign.


### -param lpNumberStr [out, optional]

Pointer to a buffer in which this function retrieves the formatted number string. Alternatively, this parameter contains <b>NULL</b> if <i>cchNumber</i> is set to 0. In this case, the function returns the required size for the number string buffer.


### -param cchNumber [in]

Size, in characters, for the number string buffer indicated by <i>lpNumberStr</i>. Alternatively, the application can set this parameter to 0. In this case, the function returns the required size for the number string buffer and does not use the <i>lpNumberStr</i> parameter.


## -returns



Returns the number of characters retrieved in the buffer indicated by <i>lpNumberStr</i> if successful. If the <i>cchNumber</i> parameter is set to 0, the function returns the number of characters required to hold the formatted number string, including a terminating null character.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or  it was incorrectly set to <b>NULL</b>. </li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
<li>ERROR_OUTOFMEMORY. Not enough storage was available to complete this operation.</li>
</ul>



## -remarks



<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="https://msdn.microsoft.com/e9e566c3-e84a-44d3-980f-fe8bbd5e052a">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="https://msdn.microsoft.com/99264b22-3fb5-47e2-b0b9-42a6768e67c1">ResolveLocaleName</a>.




## -see-also




<a href="https://msdn.microsoft.com/acbfebed-71bd-4266-b639-66f453158442">GetNumberFormat</a>



<a href="https://msdn.microsoft.com/cb8a7714-3777-41b4-894b-bb0c0797d51e">NUMBERFMT</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

