---
UID: NF:winnls.EnumDateFormatsExA
title: EnumDateFormatsExA function
author: windows-sdk-content
description: Enumerates the long date, short date, or year/month formats that are available for a specified locale.Note  Any application that runs only on Windows Vista and later should use EnumDateFormatsExEx in preference to this function.
old-location: intl\enumdateformatsex.htm
tech.root: Intl
ms.assetid: 523ef50f-722a-48b9-a2ce-20786b7c79e1
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: EnumDateFormatsEx, EnumDateFormatsEx function [Internationalization for Windows Applications], EnumDateFormatsExA, EnumDateFormatsExW, _win32_EnumDateFormatsEx, intl.enumdateformatsex, winnls/EnumDateFormatsEx, winnls/EnumDateFormatsExA, winnls/EnumDateFormatsExW
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
req.unicode-ansi: EnumDateFormatsExW (Unicode) and EnumDateFormatsExA (ANSI)
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
 - API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - EnumDateFormatsEx
 - EnumDateFormatsExA
 - EnumDateFormatsExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EnumDateFormatsExA function


## -description


Enumerates the long date, short date, or year/month formats that are available for a specified locale.
<div class="alert"><b>Note</b>  Any application that runs only on Windows Vista and later should use <a href="https://msdn.microsoft.com/52bfec03-4cb3-4418-b467-f75d2900ba40">EnumDateFormatsExEx</a> in preference to this function.</div><div> </div>

## -parameters




### -param lpDateFmtEnumProcEx [in]

Pointer to an application-defined callback function. For more information, see <a href="https://msdn.microsoft.com/7c9acda6-8e8f-44ad-855b-99597bfa3fab">EnumDateFormatsProcEx</a>.


### -param Locale [in]


<a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">Locale identifier</a> that specifies the locale for which to retrieve date format information. You can use the <a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a> macro to create an identifier or use one of the following predefined values. 

<ul>
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
<b>Windows Vista and later:</b> The following custom locale identifiers are also supported.

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
</ul>

### -param dwFlags [in]

Flag specifying date formats. For detailed definitions, see the <i>dwFlags</i> parameter of <a href="https://msdn.microsoft.com/52bfec03-4cb3-4418-b467-f75d2900ba40">EnumDateFormatsExEx</a>.


## -returns



Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



The function enumerates the date formats by passing date format string pointers, one at a time, to the specified application-defined callback function. This process continues until <b>EnumDateFormatsEx</b> finds the last date format or the callback function returns <b>FALSE</b>.

This function enumerates all date formats for the specified locale, including alternate calendars, if any. However, the calendar identifier is not enumerated along with the date format, making formats for locales with alternate calendars difficult to use.

This function can enumerate data from <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="https://msdn.microsoft.com/f62402d6-31de-4ff7-9538-7925a007a089">Using Persistent Locale Data</a>.

When the ANSI version of this function is used with a Unicode-only locale identifier, the function can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark (?).

The application should use <b>EnumDateFormatsEx</b> (instead of <a href="https://msdn.microsoft.com/77b5e753-aee9-42d8-a0fa-27b065fc3b20">EnumDateFormats</a>) to enumerate date formats for locales with alternate calendars.




## -see-also




<a href="https://msdn.microsoft.com/77b5e753-aee9-42d8-a0fa-27b065fc3b20">EnumDateFormats</a>



<a href="https://msdn.microsoft.com/52bfec03-4cb3-4418-b467-f75d2900ba40">EnumDateFormatsExEx</a>



<a href="https://msdn.microsoft.com/7c9acda6-8e8f-44ad-855b-99597bfa3fab">EnumDateFormatsProcEx</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

