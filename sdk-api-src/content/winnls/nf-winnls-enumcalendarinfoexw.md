---
UID: NF:winnls.EnumCalendarInfoExW
title: EnumCalendarInfoExW function
author: windows-driver-content
description: Enumerates calendar information for a locale specified by identifier.Note  Any application that runs only on Windows Vista and later should use EnumCalendarInfoExEx in preference to this function.
old-location: intl\enumcalendarinfoex.htm
old-project: Intl
ms.assetid: 5a313af5-e595-49b1-9651-a5afc158c7a7
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: EnumCalendarInfoEx, EnumCalendarInfoEx function [Internationalization for Windows Applications], EnumCalendarInfoExA, EnumCalendarInfoExW, _win32_EnumCalendarInfoEx, intl.enumcalendarinfoex, winnls/EnumCalendarInfoEx, winnls/EnumCalendarInfoExA, winnls/EnumCalendarInfoExW
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
req.unicode-ansi: EnumCalendarInfoExW (Unicode) and EnumCalendarInfoExA (ANSI)
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
-	API-MS-Win-Core-Localization-l2-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
-	Kernel32Legacy.dll
api_name:
-	EnumCalendarInfoEx
-	EnumCalendarInfoExA
-	EnumCalendarInfoExW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EnumCalendarInfoExW function


## -description


Enumerates calendar information for a locale specified by identifier.
<div class="alert"><b>Note</b>  Any application that runs only on Windows Vista and later should use <a href="https://msdn.microsoft.com/2aa4d5b8-9afc-4657-92f0-d5d61791b807">EnumCalendarInfoExEx</a> in preference to this function.</div><div> </div>

## -parameters




### -param lpCalInfoEnumProcEx

TBD


### -param Locale [in]


<a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">Locale identifier</a> that specifies the locale for which to retrieve calendar information. You can use the <a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a> macro to create an identifier or use one of the following predefined values. 

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

### -param Calendar [in]


<a href="https://msdn.microsoft.com/ba2e841e-e24e-476a-851e-a29b3af4f04d">Calendar identifier</a> that specifies the calendar for which information is requested. Note that this identifier can be ENUM_ALL_CALENDARS, to enumerate all calendars that are associated with the locale.


### -param CalType [in]

Type of calendar information. For more information, see <a href="https://msdn.microsoft.com/33361a97-0f27-477a-a0ee-3d4d3aaeaacf">Calendar Type Information</a>. Only one calendar type can be specified per call to this function, except where noted.


#### - pCalInfoEnumProcEx [in]

Pointer to an application-defined callback function. For more information, see <a href="https://msdn.microsoft.com/983c527d-f7dc-4771-ba3d-30ad763171a0">EnumCalendarInfoProcEx</a>.


## -returns



Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



This function enumerates calendar information for all applicable calendars for the specified locale, or for a single requested calendar, depending on the value of the <i>Calendar</i> parameter. The function enumerates the calendar information by calling the specified application-defined callback function. It passes the callback function a pointer to a buffer containing the requested calendar information. This process continues until <b>EnumCalendarInfoEx</b> finds the last applicable calendar or the callback function returns <b>FALSE</b>.

This function can enumerate data from <a href="https://msdn.microsoft.com/110efeab-c02f-4244-8950-a975cfc91e8a">custom locales</a>. Data is not guaranteed to be the same from computer to computer or between runs of an application. If your application must persist or transmit data, see <a href="https://msdn.microsoft.com/f62402d6-31de-4ff7-9538-7925a007a089">Using Persistent Locale Data</a>.

When the ANSI version of this function is used with a Unicode-only locale identifier, the function can succeed because the operating system uses the system code page. However, characters that are undefined in the system code page appear in the string as a question mark (?).




## -see-also




<a href="https://msdn.microsoft.com/33361a97-0f27-477a-a0ee-3d4d3aaeaacf">Calendar Type Information</a>



<a href="https://msdn.microsoft.com/b38abdc9-6c03-4077-9d42-c7cb6d5c66ee">EnumCalendarInfo</a>



<a href="https://msdn.microsoft.com/2aa4d5b8-9afc-4657-92f0-d5d61791b807">EnumCalendarInfoExEx</a>



<a href="https://msdn.microsoft.com/983c527d-f7dc-4771-ba3d-30ad763171a0">EnumCalendarInfoProcEx</a>



<a href="https://msdn.microsoft.com/77b5e753-aee9-42d8-a0fa-27b065fc3b20">EnumDateFormats</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

