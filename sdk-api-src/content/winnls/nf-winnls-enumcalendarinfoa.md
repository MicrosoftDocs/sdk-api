---
UID: NF:winnls.EnumCalendarInfoA
title: EnumCalendarInfoA function
author: windows-driver-content
description: Enumerates calendar information for a specified locale.Note  To receive a calendar identifier in addition to calendar information, the application should use the EnumCalendarInfoEx function.
old-location: intl\enumcalendarinfo.htm
old-project: Intl
ms.assetid: b38abdc9-6c03-4077-9d42-c7cb6d5c66ee
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: EnumCalendarInfo, EnumCalendarInfo function [Internationalization for Windows Applications], EnumCalendarInfoA, EnumCalendarInfoW, _win32_EnumCalendarInfo, intl.enumcalendarinfo, winnls/EnumCalendarInfo, winnls/EnumCalendarInfoA, winnls/EnumCalendarInfoW
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
req.unicode-ansi: EnumCalendarInfoW (Unicode) and EnumCalendarInfoA (ANSI)
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
-	kernel32.dll
-	API-MS-Win-Core-Localization-l2-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-Localization-Ansi-L1-1-0.dll
-	Kernel32Legacy.dll
api_name:
-	EnumCalendarInfo
-	EnumCalendarInfoA
-	EnumCalendarInfoW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EnumCalendarInfoA function


## -description


Enumerates calendar information for a specified locale.
<div class="alert"><b>Note</b>  To receive a calendar identifier in addition to calendar information, the application should use the <a href="https://msdn.microsoft.com/5a313af5-e595-49b1-9651-a5afc158c7a7">EnumCalendarInfoEx</a> function. Another reason for preferring this function is that Microsoft is migrating toward the use of locale names instead of locale identifiers for new locales, for interoperability reasons.</div><div> </div><div class="alert"><b>Note</b>  Any application that will be run only on Windows Vista and later should use <a href="https://msdn.microsoft.com/2aa4d5b8-9afc-4657-92f0-d5d61791b807">EnumCalendarInfoExEx</a> in preference to <b>EnumCalendarInfo</b>.</div><div> </div>

## -parameters




### -param lpCalInfoEnumProc

TBD


### -param Locale [in]


<a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">Locale identifier</a> that specifies the locale for which to retrieve calendar information. You can use the <a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

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

### -param Calendar [in]


<a href="https://msdn.microsoft.com/ba2e841e-e24e-476a-851e-a29b3af4f04d">Calendar identifier</a> that specifies the calendar for which information is requested. Note that this identifier can be ENUM_ALL_CALENDARS, to enumerate all calendars that are associated with the locale.


### -param CalType [in]

Type of calendar information. For more information, see <a href="https://msdn.microsoft.com/33361a97-0f27-477a-a0ee-3d4d3aaeaacf">Calendar Type Information</a>. Only one calendar type can be specified per call to this function, except where noted.


#### - pCalInfoEnumProc [in]

Pointer to an application-defined callback function. For more information, see <a href="https://msdn.microsoft.com/52e216cc-fa90-4937-860c-86f6e0b444b0">EnumCalendarInfoProc</a>.


## -returns



Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
</ul>



## -remarks



See Remarks for <a href="https://msdn.microsoft.com/5a313af5-e595-49b1-9651-a5afc158c7a7">EnumCalendarInfoEx</a>.




## -see-also




<a href="https://msdn.microsoft.com/33361a97-0f27-477a-a0ee-3d4d3aaeaacf">Calendar Type Information</a>



<a href="https://msdn.microsoft.com/5a313af5-e595-49b1-9651-a5afc158c7a7">EnumCalendarInfoEx</a>



<a href="https://msdn.microsoft.com/2aa4d5b8-9afc-4657-92f0-d5d61791b807">EnumCalendarInfoExEx</a>



<a href="https://msdn.microsoft.com/52e216cc-fa90-4937-860c-86f6e0b444b0">EnumCalendarInfoProc</a>



<a href="https://msdn.microsoft.com/77b5e753-aee9-42d8-a0fa-27b065fc3b20">EnumDateFormats</a>



<a href="https://msdn.microsoft.com/2f8893a0-f916-4a62-a423-e525cf281fa4">MAKELCID</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

